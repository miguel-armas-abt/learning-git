# MEZCLAR CAMBIOS DE DOS RAMAS

[← Regresar a notas](../../README.md) <br>

----

- Un merge es la creación de un nuevo commit a partir de la combinación de una rama con otra.
- Debemos situarnos con `checkout` sobre la rama absorbedora, y a continuación absorber `merge` los commits de la otra rama absorbida.

<img src="resources/git-merge.png" width="700" height="250">

> 📌 Hay dos tipos de merge:
> > ✅ **Fast forward** 
> > - Consiste en un <u>reemplazo automático</u> del código.
> > - Se suele apreciar cuando las ramas tienen cambios en líneas de código diferentes.
> 
> > **⚠️ Manual merge**: 
> > - Consiste en un <u>reemplazo manual</u> del código.
> > - Se suele apreciar cuando las ramas tienen conflicto sobre las mismas líneas de código.

----

> ### ▶️ Merge
> Crear nuevo commit tras la combinación de dos ramas
> ```shell script
> git merge <absorbed-branch>
> ```

----

> ### ▶️ Abortar merge con conflictos
> ```shell script
> git merge --abort
> ```

----

> ### ▶️ Finalizar merge manual
> Nos solicitará confirmar el mensaje del commit mediante el editor de texto VIM.
>   - **Opcional**: Edite el mensaje de commit presionando `ESC` seguido de `i`
>   - Guarde el commit presionando `ESC` seguido de `shift` + `z` + `z`
> ```shell script
> git merge --continue
> ```

----
