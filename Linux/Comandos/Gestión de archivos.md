
## Creación y modificación de directorios

| **Comandos** | **Significado**  | **Descripción**                                                                                                                   |
| ------------ | ---------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **`mkdir`**  | make directory   | El comando `mkdir` crea un nuevo directorio.                                                                                      |
| **`rmdir`**  | remove directory | El comando `rmdir` elimina un directorio. **Nota**: para eliminar carpetas con archivos en su interior utilice el parámetro `-rf` |
## Creación y modificación de archivos

| **Comando** | **Significado** | **Descripción**                                |
| ----------- | --------------- | ---------------------------------------------- |
| **`touch`** | touch           | El comando `touch` crea un nuevo archivo.      |
| **`rm`**    | remove          | El comando `rm` elimina, o borra, un archivo.  |

| **Comando** | **Significado** | **Descripción**                                                       |
| ----------- | --------------- | --------------------------------------------------------------------- |
| **`mv`**    | move            | El comando `mv` mueve un archivo o directorio a una nueva ubicación.  |
| **`cp`**    | copy            | El comando `cp` copia un archivo o directorio en una nueva ubicación. |

## Redirección de la salida estándar

Hay una forma adicional de escribir en archivos. Además de la tubería (`|`), también puede utilizar los operadores corchete de ángulo recto (`>`) y doble corchete de ángulo recto (`>>`) para redirigir la salida estándar.

Cuando se utilizan con `echo`, los operadores `>` y `>>` pueden emplearse para enviar la salida de echo a un archivo especificado en lugar de a la pantalla. 

La diferencia entre ambos es que `>` sobrescribe el archivo existente, y `>>` añade su contenido al final del archivo existente en lugar de sobrescribirlo. 

El operador `>` debe utilizarse con cuidado, porque no es fácil recuperar los archivos sobrescritos.