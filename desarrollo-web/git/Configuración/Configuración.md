## Nombre de usuario

```shell
git config --global user.name "juliannGabrielDev"
```

## Email

```shell
git config --global user.email "julian.alejandro.gabriel@gmail.com"
```

## Editor de texto predeterminado 

```shell
git config --global core.editor "code --wait"
```

## Configurar la rama principal

```shell
git config --global init.defaultBranch main
```

## Configurar los finales de línea

Windows:

```shell
git config --global core.autocrlf true
```

Linux/MacOS:

```shell
git config --global core.autocrlf input
```

---

## Verificar tu configuración 

```shell
git config --list
```