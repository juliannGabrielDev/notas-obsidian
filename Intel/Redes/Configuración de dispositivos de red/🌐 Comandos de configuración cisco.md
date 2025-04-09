## 🔧 Modo Usuario

```
enable                  # Entrar a modo privilegiado
disable                 # Salir del modo privilegiado
exit                    # Salir del modo actual
show running-config     # Mostrar configuración actual
show startup-config     # Mostrar configuración de inicio
```

## ⚙️ Modo Configuración Global

```
configure terminal      # Entrar a modo configuración
hostname [nombre]       # Configurar nombre del dispositivo
enable secret [clave]   # Establecer contraseña cifrada
no shutdown            # Activar una interfaz
shutdown               # Desactivar una interfaz

```

## 🔌 Configuración de Interfaces

```
interface [tipo][número]          # Entrar a configuración de interfaz
ip address [IP] [máscara]        # Asignar dirección IP
description [descripción]         # Agregar descripción a interfaz
duplex [auto/full/half]          # Configurar modo duplex
speed [velocidad]                 # Configurar velocidad

```

## 🔒 Configuración de Seguridad

```
line console 0                    # Configurar línea de consola
line vty 0 4                     # Configurar líneas VTY
password [contraseña]            # Establecer contraseña
login                           # Habilitar autenticación
access-list [número] [reglas]    # Crear lista de acceso

```

## 🌐 Configuración de Routing

```
router [protocolo]               # Configurar protocolo de routing
network [red]                    # Anunciar red
ip route [red] [máscara] [siguiente-salto]  # Ruta estática

```

## 💾 Guardar Configuración

```
copy running-config startup-config    # Guardar configuración actual
write memory                         # Guardar configuración (alternativo)
erase startup-config                 # Borrar configuración de inicio
reload                              # Reiniciar dispositivo

```

## 📡 Configuración VLAN

```
vlan [número]                    # Crear VLAN
name [nombre]                    # Nombrar VLAN
switchport mode [access/trunk]   # Configurar modo de puerto
switchport access vlan [número]  # Asignar puerto a VLAN
```

---

### **1. Modos de operación en Cisco**

|Modo|Comando para acceder|Descripción|
|---|---|---|
|Modo Usuario|`>` (símbolo en el prompt)|Modo básico con acceso limitado.|
|Modo Privilegiado|`enable` (`en`)|Accede a comandos avanzados y configuraciones.|
|Modo Configuración Global|`configure terminal` (`conf t`)|Permite realizar cambios en la configuración del dispositivo.|
|Modo de Configuración de Interfaz|`interface <tipo> <número>`|Configura interfaces de red.|
|Modo de Configuración de Línea|`line <tipo> <número>`|Configura acceso por consola, Telnet o SSH.|

---

### **2. Configuración Básica del Dispositivo**

|Comando|Abreviación|Descripción|
|---|---|---|
|`enable`|`en`|Accede al modo privilegiado.|
|`disable`|No tiene|Vuelve al modo usuario.|
|`configure terminal`|`conf t`|Entra al modo de configuración global.|
|`hostname <nombre>`|No tiene|Asigna un nombre al dispositivo.|
|`enable secret <contraseña>`|No tiene|Configura una contraseña encriptada para el acceso al modo privilegiado.|
|`banner motd "<mensaje>"`|No tiene|Muestra un mensaje antes del inicio de sesión.|
|`no ip domain-lookup`|No tiene|Evita que el dispositivo interprete comandos incorrectos como nombres de dominio.|
|`clock set <hora> <día> <mes> <año>`|No tiene|Configura la fecha y hora del dispositivo.|
|`copy running-config startup-config`|`wr` (en algunos dispositivos)|Guarda la configuración en la memoria de arranque.|
|`reload`|No tiene|Reinicia el dispositivo.|

---

### **3. Configuración de Interfaces**

| Comando                               | Abreviación          | Descripción                                       |
| ------------------------------------- | -------------------- | ------------------------------------------------- |
| `interface <tipo> <número>`           | `int <tipo><número>` | Accede a la configuración de una interfaz.        |
| `ip address <dirección IP> <máscara>` | No tiene             | Asigna una IP y máscara a la interfaz.            |
| `no shutdown`                         | `no shut`            | Activa la interfaz.                               |
| `shutdown`                            | `shut`               | Desactiva la interfaz.                            |
| `description <texto>`                 | No tiene             | Asigna una descripción a la interfaz.             |
| `show ip interface brief`             | `sh ip int br`       | Muestra un resumen de las interfaces y su estado. |

---

### **4. Configuración de Seguridad**

|Comando|Abreviación|Descripción|
|---|---|---|
|`enable secret <contraseña>`|No tiene|Configura la contraseña encriptada para el modo privilegiado.|
|`line console 0`|`line con 0`|Accede a la configuración de la línea de consola.|
|`line vty 0 4`|No tiene|Accede a la configuración de Telnet/SSH.|
|`password <contraseña>`|No tiene|Establece una contraseña para la línea de acceso.|
|`login`|No tiene|Habilita la autenticación por contraseña en la línea de acceso.|
|`transport input ssh`|No tiene|Restringe el acceso a solo SSH en la línea VTY.|
|`service password-encryption`|No tiene|Encripta las contraseñas en el archivo de configuración.|

---

### **5. Comandos de Verificación y Diagnóstico**

| Comando                     | Abreviación    | Descripción                                                  |
| --------------------------- | -------------- | ------------------------------------------------------------ |
| `show running-config`       | `sh run`       | Muestra la configuración actual en uso.                      |
| `show startup-config`       | `sh start`     | Muestra la configuración guardada en la memoria de arranque. |
| `show ip interface brief`   | `sh ip int br` | Muestra un resumen del estado de las interfaces.             |
| `show version`              | `sh ver`       | Muestra información del hardware y software del dispositivo. |
| `show interfaces`           | `sh int`       | Muestra información detallada de todas las interfaces.       |
| `show users`                | No tiene       | Muestra los usuarios conectados al dispositivo.              |
| `show history`              | No tiene       | Muestra los últimos comandos ejecutados.                     |
| `ping <dirección IP>`       | No tiene       | Prueba la conectividad con otro dispositivo.                 |
| `traceroute <dirección IP>` | `tracert`      | Muestra la ruta que sigue un paquete hasta su destino.       |

---

### **6. Configuración de VLANs**

|Comando|Abreviación|Descripción|
|---|---|---|
|`vlan <ID>`|No tiene|Crea una VLAN con el ID especificado.|
|`name <nombre>`|No tiene|Asigna un nombre a la VLAN.|
|`interface vlan <ID>`|`int vlan <ID>`|Accede a la configuración de una VLAN.|
|`switchport mode access`|No tiene|Configura el puerto en modo acceso.|
|`switchport access vlan <ID>`|No tiene|Asigna la VLAN a un puerto en modo acceso.|
|`switchport mode trunk`|No tiene|Configura el puerto en modo troncal.|
|`show vlan brief`|`sh vlan br`|Muestra un resumen de las VLANs configuradas.|

---

### **7. Configuración de Rutas Estáticas y Dinámicas**

|Comando|Abreviación|Descripción|
|---|---|---|
|`ip route <red_destino> <máscara> <puerta_de_enlace>`|No tiene|Configura una ruta estática.|
|`router rip`|No tiene|Activa el protocolo RIP.|
|`network <red>`|No tiene|Agrega una red al proceso de enrutamiento.|
|`router ospf <ID>`|No tiene|Activa el protocolo OSPF con el ID especificado.|
|`show ip route`|`sh ip ro`|Muestra la tabla de enrutamiento.|
