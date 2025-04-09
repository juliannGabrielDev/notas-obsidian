## 🔧 Instalación

```bash
sudo dnf install tftp-server
```

## ⚙️ Configurar el servidor TFTP

Abrir el archivo de configuración

```bash
sudo nano /etc/systemd/system/tftp.service
```

Modifica y asegúrate de que tenga lo siguiente:

```bash
[Unit]
Description=TFTP Server
After=network.target

[Service]
ExecStart=/usr/sbin/in.tftpd -s /var/lib/tftpboot
StandardInput=socket
User=nobody
Group=nogroup

[Install]
WantedBy=multi-user.target
```

## 📂 **3. Crear la carpeta TFTP y asignar permisos**

```bash
sudo mkdir -p /var/lib/tftpboot
sudo chmod -R 777 /var/lib/tftpboot
sudo chown -R nobody:nobody /var/lib/tftpboot
```

## 🚀 **4. Habilitar y arrancar el servicio**

Usar lo siguiente:

```bash
sudo systemctl enable --now tftp.socket
sudo systemctl status tftp.socket

echo Para reiniciar usar:
sudo systemctl restart tftp.socket
```

Los comandos seleccionados son:

**sudo systemctl daemon-reload**

Este comando recarga todos los archivos de configuración de systemd. Es necesario ejecutarlo después de crear o modificar un archivo de servicio para que el sistema reconozca los cambios.

**sudo systemctl enable --now tftp**

Este comando tiene dos funciones:

- enable: Configura el servicio TFTP para que se inicie automáticamente cuando arranque el sistema
- --now: Inicia el servicio inmediatamente, sin necesidad de ejecutar un comando adicional de start

## 🔥 **5. Abrir el firewall**

```bash
sudo firewall-cmd --add-service=tftp --permanent
sudo firewall-cmd --reload
```

---

## 🔥 **Ajustar permisos y SELinux (si está activo)**

```bash
sudo chown -R nobody:nobody /var/lib/tftpboot
sudo chmod -R 777 /var/lib/tftpboot
sudo restorecon -Rv /var/lib/tftpboot
```

Si **SELinux** está bloqueando el servicio, prueba:

```bash
sudo setsebool -P tftp_home_dir 1

getenforce
echo Si responde Enforcing, prueba desactivarlo temporalmente y vuelve a intentar la descarga:
sudo setenforce 0
```

---

## 🛠 **Prueba la conexión desde Fedora**

```bash
tftp localhost
get prueba.txt
```

---

## Encender y apagar

```bash
sudo systemd start tftpServ.socket

sudo systemctl stop tftpServ.service
sudo systemctl stop tftpServ.socket
```