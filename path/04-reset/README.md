# REESTABLECER CAMBIOS

[← Regresar a notas](../../README.md) <br>

----

> 📌 **Notas**
> - `HEAD~1` se refiere al commit anterior al commit actual.
> - Considere que los flags `--hard` y `--soft` se comportan distinto para cada uno de los siguientes casos.


## 1. Reset hard
⚠️️ `--hard` en conjunto con `git reset` descarta de forma irreversible los commits, así como los cambios en el `working directory`. 

---

> ### ▶️ Deshacer el último commit
> Utilice `--hard` para descartar todos los cambios realizados en el <u>último commit</u> y eliminarlos del historial de Git.
> ```shell script
> git reset --hard HEAD~1
> ```

----

> ### ▶️ Reestablecer el repositorio a un commit específico
> Utilice `--hard` para eliminar todos los <u>commits posteriores al comit seleccionado</u> y eliminarlos del historial de Git.
> ```shell script
> git reset <commit-id> --hard
> ```

----

## 2. Reset Soft
⚠️ `--soft` en conjunto con `git reset` descarta de forma irreversible los commits, pero los cambios del commit especificado son enviados al `staging area`.

> ### ▶️ Deshacer el último commit
> Utilice `--soft` para deshacer el <u>último commit</u> y conservar en el `staging area` los cambios realizados en este commit.
> ```shell script
> git reset --soft HEAD~1
> ```

---

> ### ▶️ Reestablecer el repositorio a un commit específico
> Utilice `--soft` para deshacer todos los <u>commits posteriores al comit seleccionado</u> y conservar los cambios en el `staging area`.
> ```shell script
> git reset <commit-id> --soft
> ```

--- 

## 3. Regresar cambios al stage anterior

> ### ▶️ **Regresar cambios al working directory**
> Los cambios se regresan desde el `staging area` hacia el `working directory`.
> ```shell script
> git rm --cached <filename>
> ```

----