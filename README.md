# Comandos de Git y GitHub
## Pasos para inicializar Git
En Git, es necesario inicializar algunas cosas que permitiran guardar los cambios realizados a los archivos y ramas en el computador.
```Git
git config --global user.name "Adrian Bayona"
git config --global user.email "adrianbayona325@gmail.com"
```
Esta funcion permite crear un usuario y escribe la cuenta gmail para este, hay que recordar que despues de especificar user.name o email, si alguna de las caracteristicas que se van a escribir requiere de un espacio, entonces es necesario el uso de comillas (""), asi que practicamente user.email podria guardarse correctamente sin las comillas
```Git
git config --global user.email adrianbayona325@gmail.com
```
tambien hay que inicializar un "init.defaultBranch" para especificar cual sera el nombre de la rama principal que se utilizara y un "core.editor" tambien, aunque para ser sincero no lo entiendo por completo
```Git
git config --global init.defaultBranch main
git config --global core.editor "code --wait"
```
## Cerrar inicializacion Git
Para cerrar toda inicializacion git, es necesario agregar --unset antes de especificar la inicializacion y no se le debe dar un valor despues de esta
```Git
git config --global --unset user.name
git config --global --unset user.email
git config --global --unset init.defaultBranch
git config --global --unset core.editor
```
## Crear y eliminar una rama externa o aparte
Para crear una rama se tiende a utilizar la siguiente funcion:
```Git
git checkout -b {nombre de la rama}
```
Mientra que para borrar una rama ya existente se tiende a utilizar la siguiente funcion:
```Git
git branch -d {nombre de la rama existente}
```
## Ver ramas locales
Si en algun momento queremos saber en que rama estamos ubicados y de paso saber cuales son las ramas existentes, el uso de esta linea es la necesaria:
```Git
git branch
```
o bien se puede utilizar
```Git
git branch -l
```
## Ver ramas remotas
Para poder ver las ramas que ya estan subidas en un repositorio GitHub, se hace uso de la siguiente linea:
```Git
git branch -r
```
## Ver todas las ramas (Remotas y locales)
Para poder ver las ramas que ya estan subidas en un repositorio GitHub y de paso ver las ramas que estan localmente, se hace uso de la siguiente linea:
```Git
git branch -a
```
## Para cambiar entre ramas
El cambio entre ramas es posible haciendo uso de la misma funcion para crearlas o borrarlas pero sin especificar que se quiere crear la rama o eliminarla al colocar -b o -D
```Git
git checkout {nombre de la rama existente}
```
La otra forma es mi preferida, por que segun como lo entiendo, fue creada principalmente para eso
```Git
git switch {nombre de la rama existente}
```
## Salir de la carpeta de trabajo y abrir nueva ventana de Visual Studio
Para salir de la carpeta en la cual se esta trabajando, se hace uso de
```Git
cd ..
```
Si, literalmente es eso, pero bueno, en el caso de querer crear una carpeta para despues ingresar a ella, entonces se hace uso de mkdir, a la cual le especificas el nombre de la nueva carpeta que quieres
```Git
mkdir Ejemplo
```
con esto la carpeta ya fue creada, pero no estas dentro de esta nueva carpeta, por ende es necesario ingresar a ella de la siguiente forma
```Git
cd Ejemplo
```
ojo, para ingresar a la carpeta de forma correcta es necesario escribir el nombre de la carpeta tal cual como la nombraste al crearla, con sus mayusculas y minusculas, pero si quieres ingresar a la carpeta y abrir una nueva ventana de Visual Studio, entonces, en vez de escribir el cd Ejemplo, seria de la siguiente forma:
```Git
code Ejemplo
```
de esta forma se abre una nueva venta de Visual Studio, debo recordar que esto funciona asi con linux, en el caso de ser de Windows, es necesario colocar ".\Ejemplo"
```Git
code .\Ejemplo
```
## Clonar una rama de un repositorio de GitHub a una carpeta local
En este caso se hace uso del comando clone, especificando la rama que se quiere clonar junto con la URL del repositorio
```Git
git clone -b {nombre de la rama} --single-branch https://github.com/{Cuenta GitHub}/{nombre del repositorio}.git
```
## Colocar commits a la rama
Para darle un commit a la rama que se desea, primero hay que inicializar la rama
```Git
git init
```
despues de eso, se selecciona lo que que se quiere subir utilizando add
```Git
git add {nombre del archivo deseado}
```
en el caso de que se quiera subir todos los archivos propios de la rama, despues del add se agrega un punto
```Git
git add .
```
con ello especificas que deseas seleccionar todo lo que se encuentre en la rama, y con esto listo, ya es posible el uso de la linea commit
```Git
git commit -m "docs: :memo: Se a creado algo"
```
recuerde hacer uso de docs o el tipo de especificacion que se desee para ello, tambien seria mejor hacer uso de un emoji, el cual, en este caso es ":memo:", mas detalles abrir Gitemoji-Camper.md

Tambien cabe recordar, que el "-m" necesario para agregar el commit hace referencia a que lo que se va agregar es un mensaje.
## Fusionar ramas
se utiliza desde la rama que quiere tomar los datos de las otras ramas para agregarlos asi mismo
```Git
git merge
```
## Ver historial de commit
para ver el historial de commits, es necesario hacer uso de la siguiente linea
```Git
git log
```
Y en el caso de querer verlo contraido se utiliza
```Git
git log --oneline
```
## Ver historial de ejecucion de lineas
Para ver cada ejecucion que se ha hecho
```Git
history
```
## Para borrar historial
Para borrar el historial de ejecuciones
```Git
history -c
```
## Borrar consola
Para borrar consola, se hace uso de clear o bien se puede utilizar CTRL + L.
## llamar desde local archivos de GitHub
Se llama el repositorio que se quiere
```Git
git clone https://github.com/Bayona325/NombreRepositorio.git
```
Despues de llamado se llama un pull
```Git
git pull
```
Recuerde, si quiere viajar entre distintas ramas del repositorio de GitHub llame normalmente
```Git
git checkout {nombre de la rama existente}
```
## Inializacion de GitHub
