El comando `git show` se utiliza para mostrar información detallada sobre un objeto de Git específico, generalmente un commit. Proporciona datos como el mensaje del commit, el autor, la fecha y los cambios realizados en dicho commit.

Cuando ejecutas `git show`, verás:
- El hash del commit.
- El nombre y correo del autor.
- La fecha en que se realizó el commit.
- El mensaje del commit.
- Un resumen de las diferencias (diff) introducidas en ese commit.

```bash
git show <hash-del-commit>
```