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

![3](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/96ff3585-e267-4d6d-a421-c867d72f9cc2)
![4](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/0dc432d9-ce5b-49a6-b5bc-1d15f5199dde)
  
### Comando git log --oneline vemos yalos archivos creados

![5](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/3cb1a8e5-0aca-4d1b-96f7-c3387134a321)

### Todo esto lo realice dentro de la rama creada ( desarrolloRebase)
### Ahora viene la situacion que hay que reparar en master
### entro dentro de la rama master (git checkout master) y una ves dentro..

![6](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/cad8a0cc-6e57-40ee-b00d-73a2f636d868)

### Creo otro archivo, el cual este va a resolver el problema que tengamos
### chequeo que el archivo3.txt se haya creado en la rama master.

![8](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/89be84c2-ec0d-4049-a898-41e35087e2b8)

### Ahora voy a la rama ya creada ( desarrolloRebase) y vuelvo a crear otro archivo, este seria archivo4.txt 

![9](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/216700f2-e986-4a10-96ff-2d5bc3844a95)

### tenemos archivo1,archivo2,archivo4 en la rama desarrolloRebase y archivo3 en la rama master

![10](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/bcc52ab6-57d3-492f-8625-fcdded1cbf6b)

### Ahora tengo que traer el cambio de la rama master ( archivo3 ) a la rama desarrollo
### aca es donde uso el comando git Rabase
### Ej:
### Git rabase master

![11](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/c859314e-9476-4c16-8cb1-99b8b842c18c)

### uso git log --oneline
### veo que no solo tengo los archivos 1,2 y 4 sino tambien veo que tengo el archivo 3 que viene de master
### Luego hago un git checkout master para hacer el merge de la rama desarrolloRebase

![12](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/f5435d25-ac5a-44ab-8d5b-199e6781b927)

### ya tengo los cambio realizados los cambios en la rama desarrolloRebase
![13](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/4f636dbb-795c-438b-a411-0d6a74a8281c)

### Comnaod LS veo que todos los archivos estan en la rama master
![14](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/c8f39b9b-23dc-45aa-b542-c2f0196f9767)

----------------------------------------------------------------------------------------------------------------------------

### Comando Git Reset ( soft - mixed - hard)
### el comando Reset actua alterando y modificando el historial de commits.
### Se le indica primero el commit donde quiero volver y lo que va hacer es borrar los commits que se hayan 
### hecho despues del commit donde quiero llegar.
### hay 3 tipos de reset 
* Soft
* Mixed ( este seria por defecto)
* Hard
### todas las opciones eliminan los commits pero de distinta manera

### Ej:
### git log --oneline
### para ver los commits que tengo y asi poder elegir donde volver

![log de los commits](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/b59cd1e2-e592-47cf-a2fc-0bf522e6ffb7)

### usando el comando git reset --soft y el numero del commit que elija, ese hara un cambio y se movera al area de staging 
### ya con los cambios hechos.
### elijo llegar hasta usuario con telefono

![2](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/7f49d072-0e62-4bbe-8b29-5174a4e4837a)

### ahi veo que los cambios se modificaron correctamente y tambien se pueden ver en el workingdirectory

### y en le caso de usar el comando git reset --hard y el numero de commit que en este caso me dirijo hasta el 
### ususario con telefono.

![3](https://github.com/danielgallo78/practicandoEnComandosGit/assets/130160711/6b7277e6-2ec7-4b45-aff3-d573840aca7c)

### ahora en la imagen anterior se ve que desaparecio el usuario con direccion y usuario con localidad y tambien si 
### hizo un git log y tampoco esta en el repositorio de Git.








 













