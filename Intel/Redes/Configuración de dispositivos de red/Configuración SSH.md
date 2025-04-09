```
# Establecer nombre de dominio al dispositivo
ip domain name {nombre}

# SSH requiere una clave para la autenticación segura
crypto key generate rsa

# 1024 bits
1024

# Crear usuario con máximos privilegios
username {nombre} privilege 15 secret {contraseña}

# Configurar las líneas virtuales que permiten accesos remotos
# 0 4: Se refiere a las 5 primeras líneas VTY
line vty 0 4

# Deshabilita Telnet (inseguro) y permite solo ssh para conexiones remotas
transport input ssh

# Obliga a los usuarios a autenticarse
login local
```

## Añadir IP al Switch

```
# vlan 1 es la vlan por defecto en los switches cisco
# Se usa para gestionar el dispositivo y permitir comunicación en la red
interface vlan 1

# Define IP para que el dispositivo pueda comunicarse en la red
ip address {ip} {máscara de subred}

# Por defecto las interfaces vlan están apagadas en los switches
no shut
```