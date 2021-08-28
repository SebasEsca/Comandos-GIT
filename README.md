# Comandos GIT - GitHub - Configuración - Alias - Tips

## Comandos GIT y GitHub

### git add
* Añadir archivos, seguimientos a archivos
* Añadir todos los archivos

        git add --.

* Añadir todos los archivos con extensión .html dentro de la ruta raiz

        git add *.

* Añadir todos los archivos que se encuentran dentro de la carpeta mencionada, este caso "css"

        git add css/

### git reset
* Reset archivos al último commit.
* Reset todos los archivos al último commit.

        git reset --.

* Ir a un commit específico, el HEAD^ puede ser reemplazado por el ID del commit a regresar, cuando se usa el HEDA^ se refuiere al último commit.

        git reset --soft HEAD^
        git reset --soft "Id del commit a regresar"

### git commit
* Realiza un commit.
* Realiza un commit con un mensaje que debe ser específico.

        git commit -m "mensaje específico"

* Realiza un add y commit.

        git commit -am "mensaje específico"


* Realiza una modificacion del texto al último commit

        git commit -amend -m "nuevo mensaje"

### git status
* Devuelve una respuesta de los cambios actuales, branch, archivos modificados, borrados, etc.

        git status

### git log
* Devuelve los logs realizados por los comandos de GIT, los commits, la fecha, el mensaje, quién lo realizo, etc.

        git log

* Devuelve los logs sin tantos detalles

        git log --oneline

### git branch
* Revisa las ramas/branch que existen y marca en la que se encuentra.
        
        git branch

* Cambia el nombre de la rama
        
        git branch -m master main

* Crea una nueva rama
        
        git branch "nombre de la branch"

### git checkout
* Cambia de rama a la nombrada

        git checkout "rama a cambiar"

* Reconstruye el proyecto al último commit 

        git checkout --.

* Crea una nueva rama y se cambia a esa rama

        git checkout -b "nueva rama"

* Regresa el archivo al inicio del commit 

        git checkout --README.md

### git diff
* Enseña los cambios entre ramas 

        git diff

### git reflog
* Enseña TODOS los logs, ya que no se borran

        git reflog

### git mv
* Cambia el nombre del archivo o carpeta

        git mv "nombre anterior" "nuevo nombre"

### git merge
* Unir ramas, se lo realiza dentro de la rama y se menciona la rama que quiero unir

        git merge "rama a unir"

### git tag
* Permite versionar el repositorio o proyecto

        git tag "nombre de la version"

* Permite versionar el repositorio o proyecto con amotated

        git tag -a v1.0.0 -m "version 1 lista"
        
        
### git shaw
*  Por definir

        git shaw v1.0.0

### git stash
* Usar cuando no se esta utilizando branches ya que STASH se usa para cambios temporales y urgentes, no es recomendable usar.

        git stash

### git rebase
* Función similar a la del merge pero es menos recomendable, actualiza la rama en la que se encuentra

        git rebase

### git rebase -i 
* Función rebase pero interactiva
* Regresar a los 4 commits anteriores

        git rebase --interactive HEAD~4

    ### Squash ó s
    * Chocar y unir commits
    ### Reward ó r
    * Cambiar mensaje del commit
    ### Edit ó e
    * Editar el commit
        ### git rebase --continue 
        * Salir del edit del rebase





## Configuración

### git config --global user.name "Sebas"
* Setear el nombre del usuario Sebas

        git config --global user.name "Sebas"

### git config --global user.email "andre-sebas@hotmail.com"
* Setear el correo del usuario andre-sebas@hotmail.com

        git config --global user.email "andre-sebas@hotmail.com"

### git config --global -e
* Revisar toodas las configuraciones de GIT

        git config --global -e

### git config --global alias.s "status --short"
* Crear un alias/atajos
* Crear un alias que reemplace "status --short" con la letra s

        git config --global alias.s "status --short"


## Alias

### git status -> git s

    git config --global alias.s "status --short"

### git log 

    git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"



## Tips

### "--"
* El "--" se usa con palabras completas.

        --global

### "-"
* El "-" se usa con abreviaturas de palabras.
* "-a" significa add

        -a

### "--."
* El "--." se usa para referirse a todos los archivos o documentos.

        --.

### ":wq!"
* "w" es para write.
* "q" es para quit.
* "!" es para salir

### .gitkeep
* Archivo que se crea con el nombre ".gitkeep" para dar seguimiento a la carpeta en GIT

### "--oneline"
* Se usa para tener la respuesta en una sola línea

        --oneline

### "--soft"
* Se usa en el reset, no borra los commits siguientes

        --soft

### "--mixed"
* Se usa en el reset, no borra los commits siguientes

        --mixed

### "--hard"
* Se usa en el reset, borra los commits siguientes

        --hard

### "HEAD^"
* Se usa para referirse a los commits

        --hard

### "v1.0.2"
* "1" Cambios o mejoras notables de funcionalidad como visual, nuevas funcionalidades.
* "0" Mejoras de funcionalidad no tan notables.
* "2" Correcciones de bugs.
