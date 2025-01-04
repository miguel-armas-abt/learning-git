# RESERVAR CAMBIOS TEMPORALES

[← Regresar a notas](../../README.md) <br>

----

- Git stash permite reservar temporalmente los cambios que has realizado en tu `working directory` sin realizar un commit. 
- Es útil cuando necesitas cambiar de rama o actualizar el repositorio sin llevar los cambios en progreso (`WIP`, work in progress).
- Si obtienes un `WIP` que fue stasheado desde otra rama, probablemente genere conflictos.⚠️

----

> ### ▶️ Guardar / Mostrar / Eliminar stash
> ```shell script
> git stash -m "<description>"
> git stash list
> git stash drop <index>
> ```

----

> ### ▶️ Recoger cambios del stash
> Puedes especificar el índice del stash que deseas recuperar. Si no lo indicas, por defecto recuperará el último stash apilado.
> ```shell script
> git stash pop
> git stash pop <index>
> ```

----

> ### ▶️ Guardar los cambios del stash en una rama aparte
> ```shell script
> git stash branch <branch-name>
> ```

----