# GIT STAGES

[← Regresar a notas](../../README.md) <br>

---

| #   | Stage               | Descripción                                                           |
|-----|---------------------|-----------------------------------------------------------------------|
| 1   | `Working Directory` | Carpeta de trabajo donde están los archivos sin rastrear (untracked). |
| 2   | `Staging Area`      | Espacio en memoria ram donde se guaradan los cambios (tracked).       |
| 3   | `Local Repository`  | Copia del repositorio de Git que reside en tu máquina local.          |                                             |
| 4   | `Remote Repository` | Versión centralizada del repositorio de Git.                          |                                             |

![Texto alternativo](../../images/git_stages.png)

----

## ▶️ Clonar un repositorio remoto (clone)
> - Podemos especificar el nombre de la 📁carpeta en la que se descargará el repositorio.
> - Podemos utilizar `-b` para especificar la rama que queremos clonar.
> ```shell script
> git clone <url-repository>
> git clone <url-repository> <directory-name>
> git clone -b <branch-name> <url-repository> <directory-name>
> ```

---

## ▶️ Inicializar repositorio (init)
> Este comando genera un subdirectorio `📁.git` que permite gestionar el historial de versiones del proyecto.
> ```shell script
> git init
> ```

---

## ▶️ Enviar archivos al staging area (add)
> Podemos especificar cada archivo a la vez o podemos utilizar `.` para enviar todo. 
> ```shell script
> git add <filename>
> git add .
> ```

---

## ▶️ Enviar archivos al repositorio local (commit)
> - Podemos utilizar `-am` para realizar en un solo paso `add` y `commit` sobre los archivos que ya están trackeados.
> - Si no ingresamos ningún argumento después de `commit`, nos solicitará ingresar un mensaje mediante el editor de texto VIM. 
>   - Edite el mensaje de commit presionando `ESC` seguido de `i`
>   - Guarde el commit presionando `ESC` seguido de `shift` + `z` + `z`
> ```shell script
> git commit -m "<my-message>"
> git commit -am "<my-message>"
> git commit
> ```

---

## ▶️ Vincular al repositorio remoto (remote)
> Establece el repositorio remoto llamado `origin` y le asigna la URL.
> ```shell script
> git remote add origin <url.git>
> ```

---

## ▶️ Enviar archivos al repositorio remoto (push)
> ```shell script
> git push -u origin <branch-name>
> ```

----

## ▶️ Descargar cambios del repositorio remoto (pull)
> - El `git pull` funciona como un `git fetch` en combinación con `git merge`.
> - Puede utilizar `origin` para especificar la rama de la que quiere descargar los cambios.
> ```shell script
> git pull
> git pull origin <branch-name>
> ```

----