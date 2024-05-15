# practicandoEnComandosGit
esta es una carpeta de practica de algunos de los tantos comandos de Git. hecha solo en un readme como informacion de ayuda

# Comandos Git - Rebase - Reset - Fetch - Checkout
----------------------------------------------------------------------------------
### Este documento cubre los conceptos básicos y ejemplos prácticos de los siguientes comandos de Git:

* git fetch
* git rebase
* git reset
* git checkout
----------------------------------------------------------------------------------
#### Comando Fetch
### El comando git fetch se utiliza para descargar objetos y referencias desde otro repositorio.
### git fetch actualiza la copia local del repositorio remoto que fue clonada sin aplicar los cambios a la rama actual.
### ej:
### Hago una clonacion de archivo.


![1](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/d6b75a73-bea4-4841-b145-de19aab24c5b)

### una ves clonado.

![b](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/a7b39f4a-639a-4fbd-9541-5fa6fe21bdff)

### Luego agrego un archivo o realizo un cambio desde el repositorio remoto
### Archivo ya creado.

![c](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/a8f21444-cd7c-4152-8af2-1bf5178df24a)

### Desde la terminal veo que el archivo no me lo muestra ya que es una rama oculta la cual se trae con el comando git Fetch.

![d](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/fcc8c1d2-108d-4c87-9bc5-2c76e0d93d7c)

### Uso los comando git fetch.

![f](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/a955970a-bf76-49f7-b242-738e447daa8d)

![h](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/09b0626b-e245-41aa-920a-cceac82e8429)

### y con el comando git checkout fetch_head me permite moverme entre la rama.

### Con el comando git Switch lo que me permite es hacer una clonacion de esta rama oculta y tambien poder realizar cambios sin perjudicar a este mismo archivo.

----------------------------------------------------------------------------------------------------------------------------------

#### Comando Git Rebase
### Trae los cambios de la rama principal hasta mi rama de desarrollo
### permite integrar cambios desde una rama a otra reescribiendo el historial de commits.
### ej:
### dentro de la terminal creo una rama con Git Branch y le doy de nombre desarrolloRebase 
### git branch desarrolloRebase

![1](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/67c6ff5e-5bce-444e-9c58-e446359e7947)

### luego git checkout desarrolloRebase para meterme dentro de la rama creada
### una ves dentro.

![2](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/a7094cb4-a0de-4a47-8049-d2005853082a)
### lo que hago es crear unos archivos( archivo1 y archivo2) con el siguiente comando abreviado
### touch archivo1.txt && git add archivo1.txt && git commit -m " archivo1.txt"
### touch archivo2.txt && git add archivo2.txt && git commit -m " archivo2.txt"
### de esta manera le digo que me cree archivo1.txt y luego agregue el archivo y luego que haga el commit + el msj

 ![4](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/0dc432d9-ce5b-49a6-b5bc-1d15f5199dde) 
 
### Comando git log --oneline vemos yalos archivos creados

![5](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/3cb1a8e5-0aca-4d1b-96f7-c3387134a321)

### Todo esto lo realice dentro de la rama creada ( desarrolloRebase)
### Ahora viene la situacion que hay que reparar en master
### entro dentro de la rama master (git checkout master) y una ves dentro..

![6](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/cad8a0cc-6e57-40ee-b00d-73a2f636d868)

### Creo otro archivo, el cual este va a resolver el problema que tengamos
### chequeo que el archivo3.txt se haya creado en la rama master.

![7](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/15f5872b-aad4-4af4-a3fa-75608ba691c4)
![8](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/89be84c2-ec0d-4049-a898-41e35087e2b8)








 













