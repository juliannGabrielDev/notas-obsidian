Puede utilizar `sudo` con muchas tareas de gestión de autenticación y autorización. 

## useradd

El comando `useradd` añade un usuario al sistema. 

```shell
sudo useradd fgarcia
```

Existen opciones adicionales que puede utilizar con `useradd`:

- -**g**: Establece el grupo por defecto del usuario, también llamado su grupo primario

```shell
sudo useradd -g security fgarcia
```

- **-G**: Añade al usuario a grupos adicionales, también llamados grupos suplementarios o secundarios.

```shell
sudo useradd -G finance,admin fgarcia
```

## usermod

El comando `usermod` modifica las cuentas de usuario existentes. Las mismas opciones `-g` y `-G` del comando `useradd` pueden utilizarse con `usermod` si ya existe un usuario.

Para cambiar el grupo primario de un usuario existente, necesita la opción `-g`. 

```shell
sudo usermod -g executive fgarcia
```

Para añadir un grupo suplementario para un usuario existente, necesita la opción `-G`. También necesita la opción `-a`, que añade el usuario a un grupo existente y sólo se utiliza con la opción `-G`.

```shell
sudo usermod -a -G marketing fgarcia
```

**Nota:** Al cambiar el grupo suplementario de un usuario existente, si no incluye la opción `-a, -G` sustituirá cualquier grupo suplementario existente por los grupos especificados después de `usermod`. El uso de `-a` con `-G` garantiza que se añadan los nuevos grupos pero que no se sustituyan los grupos existentes.

Existen otras opciones que puede utilizar con `usermod` para especificar cómo desea modificar el usuario, entre las que se incluyen:

- **`-d`**: Cambia el Directorio personal del usuario.

- **`-l`**: Cambia el nombre de usuario.

- **`-L`**: Bloquea la cuenta para que el usuario no pueda registrarse.

## userdel

El comando `userdel` borra un usuario del sistema. 

El comando `userdel` no borra los archivos del directorio personal del usuario a menos que utilice la opción `-r`. 

```shell
sudo userdel -r fgarcia
```

**Nota**: En lugar de borrar al usuario, podría considerar desactivar su cuenta con `usermod -L`.

## chown

El comando `chown` cambia la propiedad de un archivo o directorio. Puede utilizar `chown` para cambiar la propiedad del usuario o del grupo.

```shell
sudo chown fgarcia access.txt

sudo chown :security access.txt
```