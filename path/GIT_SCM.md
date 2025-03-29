## 9. Clave SSH
> Algunas notas en el proceso de creación de clave SSH:
- Ubicarse en la ruta de usuario.
- Mantener el directorio por defecto.
- Una passhphrase es una contraseña con espacios (para más seguridad).

- `$ ssh-keygen -t rsa -b 5096 -C "<my-email>"`
- `$ eval $(ssh-agent -s)` : Verificar que el servidor de llaves esté corriendo.
- `$ ssh-add ~/.ssh/id_rsa` : Añadir clave privada al usuario del entorno local.

> **Observación**: Si tienes 3 laptops, tienes que tener 3 llaves (privada y pública) conectadas al repositorio remoto por cada computadora.

- `$ git remote set-url origin <url-ssh>` : Cambiar la url (de http hacia ssh) del repositorio asociado a origin.

## 10. Tags y versiones en GIT SCM y GitHub
- `$ alias tree="git log --all --graph --decorate --oneline"` : Crear alias para los comandos.
- `$ git tag -a <version> -m "<message>" <commit-id>` : Crear tag o release.
> $ git tag -a v0.1 -m "Primera versión" 218d6fa

- `$ git tag` : Mostrar tags.
- `$ git show-ref --tags` : Mostrar detalle del tag por commit.
- `$ git push origin --tags` : Subir tags al repositorio remoto.
- `$ git tag -d <tag-name>` : Eliminar tag local.
- `$ git push origin :refs/tags/<tag-name>` : Eliminar tag remoto.

## 11. Rebase
> El comando rebase es una mala práctica, nunca se debe usar. Con rebase puedes recoger todos los cambios confirmados en una rama y ponerlos sobre otra.

- `$ git checkout <branch-from-rebase>` : Cambiar a la rama sobre la que queremos agregar los cambios confirmados.

- `$ git rebase <branch-to-rebase>` : Aplicar rebase para recoger los cambios de la rama que queremos.

## 13. Git Clean
- `$ git clean --dry-run` : Mostrar los archivos que se borrarán, que no forman parte importante del proyecto.
- `$ git clean -f` : Borrar los archivos listados al ejecutar `$ git clean --dry-run`.

## 16. Git Reset y Reflog
- `$ git reflog` : Mostrar los HEAD del historial de cambios hasta ahora (copiamos el commit-id o hash).
- `$ git reset --hard <commit-id>` Retornar a la confirmación (commit) del hisotrial que indiquemos.

## 18. Comandos y recursos colaborativos
- `git shortlog` : Ver cuántos commits a hecho los miembros del equipo.
- `git shortlog -sn` : Las personas que han hecho ciertos commits.
- `git shortlog -sn --all` : Todos los commits (también los borrados).
- `git shortlog -sn --all --no-merges` : Mostrar las estadísticas de los commits del repositorio donde estoy.
- `git config --global alias.stats “shortlog -sn --all --no-merges”` : Configura el comando `“shortlog -sn --all --no-merges”` en un alias en las configuraciones globales de git del ordenador.
- `git blame -c blogpost.html` : Mostrar quién ha hecho cambios en dicho archivo identado.
- `git blame --help` : Mostrar en el navegador el uso del comando.
- `git blame archivo -L 35, 60 -c`: Mostrar quién escribió el código con información de la línea 35 a la 60, EJ: git blame css/estilos.css -L 35, 60 -c
