## COMANDOS

### **_En nuestra terminal interactuamos con los siguientes comandos:_**
+ __ls__ muestra la lista de archivos que se  contienen en el documento
+ __ls -a__ muestra archivos asi esten ocultos, muestra tambien . ..
+ __ls -l__ muestra  permisos  de directorio, propietario, peso y fecha de modificacion, nos indica que es un directorio porque inicia con la letra _d_.
+ __ls -la__ lista permisos de directorio, propietario, peso y fecha de modificacion y archivos ocultos
+ __ls- lat__ organiza archivos segun fecha de modificacion
+ __ls -x__ Ordena los archivos por extensión
+ __ls -lh__ Muestra la misma información que ls -l pero con las unidades de tamaño en KB, MB
+ __ls -r__ Muestra el contenido de todos los subdirectorios de forma recursiva
+ __ls -s__ Ordena los resultados por tamaño de archivo

### **_Crear y cambio de directorio_**

+ __pwd__ nos indica donde estamos es ruta absoluta
+ __mkdir__ crea carpeta 
+ __cd__ permite abrir carpeta y ubicarnos 
+ __- cd /__ Permite ir a la ruta principal
+ __cd ~__ ir a la ruta de tu usuario
+ __cd carpeta/subcarpeta__ Navegar a una ruta dentro de la carpeta donde estamos ahora mismo.
+ __cd .. (cd + dos puntos)__ Regresar una carpeta hacia atrás.
+ __..__ devuelve a carpeta padre 
+ __.__ nos permite saber donde estamos 
+ __cd ~/__ para ir a home
+ __cp__ copia un archivo _nombre de archivo que se copia directorio al que va/_

__History__ muestra el historico de comandos que se han hecho con un numero que lo identifica, para llamarlo ponemos el __!__ y __numero que indica el codigo__

## **_crear editar mover y eliminar un archivos_**

+ __touch nombre de archivo__ crea el archivo
+ __nano nombre del archivo__ edita el archivo, salimos con control x,  guardamos con _"y"_ y salimos con enter
+ movemos la carpeta de una a otra con __mv/nombre del archivo/ubicacion__
+ __rm dir__ elimina directorio
+ __rm nombre de archivo__ elimina el archivo
+ __rm-rf nombre de la carpeta__ eliminar folder
__clear:__ Para limpiar la terminal. También podemos usar los atajos de teclado Ctrl + L o Command + L.

## **_Comandos de archivo_**

+ __CAT nombre del archivo__ nos muestra el contenido de ese mismo
+ __more nombre de archivo__ muestra una parte del archivo, podemos navegar con las flechas, salimos con _"q"_
+ __tail nombre de archivo__ muestra 10 lineas del archivo
+ __cat nombre de archivo > nombre de copia de archivo__, genera copia para mac open, abre archivo con programa que trae por defecto

__Todos estos comandos tiene una función de autocompletado, o sea, puedes escribir la primera parte y presionar la tecla Tab para que la terminal nos muestre todas las posibles carpetas o comandos que podemos ejecutar. Si presionas la tecla Arriba puedes ver el último comando que ejecutamos.__

__Recuerda que podemos descubrir todos los argumentos de un comando con el argumento --help (por ejemplo, cat --help).__  
_tomado de john freddy vega_

## **_llaves ssh_**

Son formas seguras para conectarnos con servidores,la llave publica se puede compartir en internet, la privada no se debe compartir, sirve para asegurar commits y despliegues en produccion.

las creamos en el home de la terminal con _ssh-keygen -t rsa -b 4096 -C "this is a key"_
guardamos _.ssh/id_rsa_  damos enter
 te pide un password o passphrase confirmandolo despues 

 Para comprobar que tu llave este creada en windows o linux debes escibir  _$ eval $(ssh-agent -s)_ esto te debe mostrar una informacion como _agent pid 4724_ o algo similar a este codigo donde se confirma que ya tienes tus llaves tanto como publica y privada.

 cd ~/.ssh/ muestra las llaves, __nunca debes mostrar tu llave privada__
 
 ls -al te muestra de manera mas especifica donde estan ubicadas las llaves 

 con _~/.ssh/id_rsa_ escogemos esta llave para agregarla a nuestro sistema no la publica, por que la publica es la que ligas con el github en este caso.

 Para agregar el correo en windows o linux el correo debo ejecutar el comando _git config --global user.email "email@gmail.com"_ , la llave es unica en cada computador por el nombre.

 Luego de crear nuestras llaves SSH podemos entregarle la llave pública a GitHub para comunicarnos de forma segura y sin necesidad de escribir nuestro usuario y contraseña todo el tiempo.

Para esto debes entrar a la Configuración de Llaves SSH en GitHub, crear una nueva llave con el nombre que le quieras dar y el contenido de la llave pública de tu computadora.

Ahora podemos actualizar la URL que guardamos en nuestro repositorio remoto, solo que, en vez de guardar la URL con HTTPS, vamos a usar la URL con SSH:

~~~
git remote set-url origin url-ssh-del-repositorio-en-github
~~~

## **_Configuracion de la terminal para crear nuestro shell_**

Debemos ir a __hyper.is__ ,descargamos, abrimos y se arrastra a las aplicaciones, al abrir no se nota mucho cambio en la terminal, este paso es opcional.

 Para descargar oh my zsh:  vamos a https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH 
Antes debemos ir  a la terminal y verificar la version que tenemos copiando en la terminal zsh --version y lo ejecutamos en la terminal, si no se tiene instalado debe copiarse __brew install zsh zsh-completions__
debemos verificarlo nuevamente con __zsh --version__

__ohmyzsh__ permite configurar y personalizar la terminal, vamos a https://ohmyz.sh/ copiamos el comando $ sh -c "$ (curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"en la terminal
afirmamos con __y__  y colocamos contraseña del usuario 

## **_Temas personalizados_**
  __~/.zshrc__ Vamos a el archivo dentro del _home_ donde estan  las configuraciones debemos cambiar el tema con la variable __ZSH_THEME__

vamos a la terminal __ls -la__
hacemos __nano.zshrc__
muestra la variable de tema, eliminamos __robbyrussell__ y agregamos  por ejemplo __af-magic__ y guardamos
hacemos __source.zshrc__
y cambia nuestro tema 

## **_Cambiar desde windows 10 tema_**
Vamos a cambios de configuracion ,  setting,update & security, developer , developer mode 
open con powershell , ejecuta  y se reinicia.

En marketplace buscar linux e instalar ubuntu, 
inserta username y contraseña en la terminal 
creas folder _mkdir folder_

Debemos ir a __hyper.is__ descargamos, abrimos se arrastra a las aplicaciones y se abre,
con _dir_ muestras listas. 
__sudo apt-get install zsh__
vamos a la pagina  https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH  

## **_Instalar editor de codigo_** 
Vamos a la direccion de visual code https://code.visualstudio.com/, ir a dowland y y descargar moviendo a la carpeta de las aplicaciones, con _open folder_ abrimos proyectos 




[volver al indice](./README.md)