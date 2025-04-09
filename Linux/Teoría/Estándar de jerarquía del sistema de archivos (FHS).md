- [[#Directorio raíz|Directorio raíz]]
- [[#Directorios FHS estándar|Directorios FHS estándar]]
- [[#Subdirectorios específicos de usuario|Subdirectorios específicos de usuario]]

**Estándar de jerarquía del sistema de archivos** (FHS) es el componente de Linux que organiza los datos. El FHS es importante porque define cómo se organizan los directorios, el contenido de los directorios y otros tipos de almacenamiento en el sistema operativo.

## Directorio raíz

El **directorio raíz** es el ==directorio de más alto nivel en Linux==, y siempre se representa con una barra oblicua (`/`). Todos los subdirectorios se ramifican a partir del directorio raíz. Los subdirectorios pueden continuar ramificándose hasta tantos niveles como sea necesario.

## Directorios FHS estándar

Directamente debajo del directorio raíz, encontrará los directorios FHS estándar. 

- **/home:** Cada usuario del sistema tiene su propio directorio personal.

- /**bin:** Este directorio significa "binario" y contiene archivos binarios y otros ejecutables. Los ejecutables son archivos que contienen una serie de órdenes que una computadora debe seguir para ejecutar programas y realizar otras funciones.

- **/etc:** Directorio que almacena los archivos de configuración del sistema.

- **/tmp:** Este Directorio almacena muchos archivos temporales. El directorio /tmp es utilizado habitualmente por los atacantes porque cualquier persona del sistema puede modificar los datos de estos archivos.

- **/mnt:** Este Directorio significa "montar" y almacena soportes, como unidades USB y discos duros.

**Consejo profesional**: Puede utilizar el comando `man hier` para obtener más información sobre el FHS y sus directorios estándar.

## Subdirectorios específicos de usuario

Bajo `home` hay subdirectorios para usuarios específicos. En el diagrama, estos usuarios son **analyst** y **analyst2**. Cada usuario tiene sus propios subdirectorios personales, como `projects`, `logs` o `reports`.