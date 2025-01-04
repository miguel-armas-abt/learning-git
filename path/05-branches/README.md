# MANIPULAR RAMAS

[← Regresar a notas](../../README.md) <br>

----


Una rama es una bifurcación del estado de nuestro código, en la cual podemos experimentar cambios sin alterar la 
 rama que tiene la versión estable de nuestro proyecto.

<img src="../../images/git-branch.png" width="600" height="200">


> 📌 `HEAD` es un puntero que apunta al último commit de la rama actual sobre la que estás trabajando. 

----

> ### ▶️ Mostrar ramas
> - Utilice `-a` para mostrar las ramas locales y remotas
> - Utilice `-r` para mostrar las ramas remotas
> ```shell script 
> git branch
> ```

----

> ### ▶️ Cambiar / Crear / Eliminar rama
> - **Cambiar**: Utilice `checkout` para cambiar de rama
> - **Crear**: Utilice `-b` para crear una nueva rama
> - **Eliminar local**: Utilice `-D` para eliminar una rama local
> - **Eliminar remoto**: Utilice `push origin --delete` para eliminar una rama remota
> ```shell script
> git checkout <branch-name>
> git checkout -b <branch-name>
> git branch -D <branch-name>
> git push origin --delete <branch-name>
> ```

----

> ### ▶️ Mostrar el historial de commits de las ramas
> - Utilice `--all` para mostrar ramas locales y remotas
> ```shell script
> git show-branch
> ```

----

> ### ▶️ Mostrar en una UI el historial de commits de las ramas
> - Utilice `--all` para mostrar ramas locales y remotas
> ```shell script
> gitk
> ```

----

