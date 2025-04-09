- [[#Permisos de lectura|Permisos de lectura]]
- [[#Exploración de los permisos existentes|Exploración de los permisos existentes]]
- [[#Uso de chmod|Uso de chmod]]

## Permisos de lectura

En Linux, los permisos se representan con una cadena de 10 caracteres(**drwxrwxrwx**) . Los permisos incluyen:

- **leer (r)**: para archivos, esta es la capacidad de leer el contenido del archivo; para directorios, esta es la capacidad de leer todo el contenido en el directorio incluyendo tanto archivos como subdirectorios

- **escribir (w)**: para archivos, esta es la capacidad de hacer modificaciones en el contenido del archivo; para directorios, esta es la capacidad de crear nuevos archivos en el directorio

- **ejecutar (x)**: para los archivos, es la capacidad de ejecutar el archivo si se trata de un programa; para los directorios, es la capacidad de entrar en el directorio y acceder a sus archivos.

Estos permisos se otorgan a estos tipos de propietarios:

- **usuario**: el propietario del archivo
- **grupo**: un grupo mayor del que forma parte el propietario
- **otro**: todos los demás usuarios del sistema.

## Exploración de los permisos existentes

Puede utilizar el comando `ls` para investigar quién tiene permisos sobre archivos y directorios. 

Existen opciones adicionales que puede añadir al comando `ls` para que su comando sea más específico. 

- `ls -a`: Muestra los archivos ocultos. Los archivos ocultos comienzan con un punto (.) al principio.

- `ls -l`: Muestra los permisos de archivos y directorios. También muestra otra información adicional, como el nombre del propietario, el grupo, el tamaño del archivo y la hora de la última modificación.

- `ls -la`: Muestra los permisos de archivos y directorios, incluidos los archivos ocultos. Es una combinación de las otras dos opciones.

## Uso de chmod

El comando `chmod` requiere dos argumentos. El primer argumento indica cómo cambiar los permisos, y el segundo argumento indica el archivo o directorio. 

```shell
chmod u+rwx,g+rwx,o+rwx login_sessions.txt
```

Si quisiera quitar todos los permisos, podría utilizar

```shell
chmod u-rwx,g-rwx,o-rwx login_sessions.txt
```

Otra forma de asignar estos permisos es utilizar el signo igual `(=)` en este primer argumento. 

```shell
chmod u=r,g=r,o=r login_sessions.txt
```

Este Comando sobrescribe los permisos existentes. 

>[! IMPORTANT]
>No debe añadir espacios después de las comas.

La siguiente tabla repasa cómo se utiliza cada carácter dentro del primer argumento de `chmod`:

| **Carácter** | **Descripción**                                             |
| ------------ | ----------------------------------------------------------- |
| **`u`**      | Indica que se realizarán cambios en los permisos de usuario |
| **`g`**      | Indica que se realizarán cambios en los permisos de grupo   |
| **`o`**      | Indica que se realizarán cambios en otros permisos          |
| **`+`**      | Añade permisos al usuario, grupo u otro                     |
| **`-`**      | Elimina permisos del usuario, grupo u otro                  |
| **`=`**      | Asigna permisos al usuario, grupo u otro.                   |
