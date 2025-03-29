# MANIPULAR CAMBIOS

[← Regresar a notas](../../README.md) <br>

----

> ### ▶️ Mostrar el historial de commits
> - Utilice `--all` para mostrar todos los detalles del commit.
> - Utilice `--oneline` para mostrar solo el hash y el mensaje.
> - Utilice `--graph` para mostrar la bifurcación de las ramas.
> - Utilice `--stat` para mostrar los archivos que fueron modificados en cada commit.
> - Utilice `-S` para filtrar los commits que contengan una palabra en los mensajes de confirmación.
> - Puede indicar un archivo específico.
> ```shell script
> git log
> git log --oneline --graph
> git log --stat
> git log <filename.txt>
> git log -S "<match-word>"
> ```
----

> ### ▶️ Mostrar información de un commit
> - Incluye autor, fecha, mensaje de confirmación y las diferencias de los archivos modificados.
> - Si no se indica el `commit-id`, se mostrará la información del último commit.
> ```shell script
> git show
> git show <commit-id>
> ```
----

> ### ▶️ Mostrar las diferencias entre dos commits
> ```shell script
> git diff <commit-id1> <commit-id2>
> ```
----

> ### ▶️ Regresar el estado de un archivo a un commit específico
> ```shell script
> git checkout <commit-id> <filename.txt>
> ```
----

> ### ▶️ Enmendar commit
> - Utilice `amend` para modificar el último commit con nuestros cambios más recientes en lugar de crear un nuevo commit.
> - Utilice `--no-edit` para conservar el mensaje del commit original.
> ```shell script
> git commit --amend -m "<my-message>"
> git commit --amend --no-edit
> git commit --amend
> ```
> 💡 Recuerde subir sus nuevos cambios al staging area antes de enmendar el commit.

----

> ### ▶️ Traer un commit de otra rama y modificar el historial de la rama actual
> ```
> git cherry-pick <commit-id>
> ```
----