Como instalar, desistalar y encontrar rutas y nombres de los programas.

- [[#Instalar y eliminar paquetes|Instalar y eliminar paquetes]]
- [[#Reinstalar paquetes|Reinstalar paquetes]]
- [[#Listar paquetes instalados|Listar paquetes instalados]]
- [[#Encontrar el nombre de un paquete específico|Encontrar el nombre de un paquete específico]]
- [[#Ver actualizaciones disponibles|Ver actualizaciones disponibles]]

---
## Instalar y eliminar paquetes

-Un paquete:

```bash
sudo dnf install nombre-paquete

sudo dnf remove nombre-paquete
```

- Varios paquetes al mismo tiempo:

```bash
sudo dnf install paquete1 paquete2

sudo dnf remove paquete1 paquete2
```

## Reinstalar paquetes

```bash
sudo dnf reinstall nombre-paquete
```

## Listar paquetes instalados

```bash
sudo dnf list installed
```

## Encontrar el nombre de un paquete específico

```bash
sudo dnf list installed | grep palabra-clave
```

## Ver actualizaciones disponibles

```bash
sudo dnf check-update
```

## Buscar archivos ejecutables

El comando `whereis` en Linux se utiliza para localizar los archivos binarios (ejecutables), de configuración y de documentación de un programa. Es útil cuando deseas saber en qué ubicación se encuentran estos archivos en tu sistema.

```bash
whereis nombre-programa
```
