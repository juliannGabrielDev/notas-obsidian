 ## Instalación

```shell
sudo dnf install putty
```

## Lista los dispositivos

```shell
lsusb
ls /dev/tty*
```

## Modifica los permisos del archivo de dispositivo `/dev/ttyUSB0`

```shell
sudo chmod 666 /dev/ttyUSB0
```