# ORGANIZAR CON LA TERMINAL Y LINEA DE COMANDOS

La terminal  es la mejor amiga del programador y la herramienta para crear cosas increibles! 

Nos sirve para generar mas eficacia, se entendera nuestro codigo de una manera sencilla _comando parametro modificadores_.

__Los modificadores alteran lo que el programa realiza y los parametros son informacion que hace que se desarrolle efectivamente__ 

Podemos probar comandos como _Date_, nos mostrara la fecha actual, si queremos estos datos mas detallados podemos escribir _man date_. Tambien podemos indicar el comando que se escribio anteriormente con la flecha hacia arriba para no reescribir el codigo. Dado el caso podemos escribir las dos primeras letras del comando que queremos usar y oprimir tab, nos mostrara los comandos que inician con esas letras. Con el comando _history_ puedo ver los comandos que he usado con un numero al lado, para llamar ese comando colocamos _! numero_ de esta manera traemos el codigo que mostro en la lista _history_.


__¿Cómo Organizamos la información en la computadora?__

"Archivos, directorios y subdirectorios"

Cada archivo tiene un nombre e identificación:

_Directorio/Subdirectorio/Archivo_

 + No puede llamarse igual un archivo dentro de un mismo directorio, se limitan los caracteres

  + Para ver los archivos en un directorio  usamos ls

  + Para ver todos los archivos listados usamos ls -a ,los archivos nuevos se indican con un punto 

  + Hay dos archivos que siempre se ven ..  es directorio padre y . hace referencia al directorio actual, usando pwd nos lleva al sitio actual en que estamos

  + cd nos mueve a la ubicacion que queremos llegar 

  ## **_compresión Y descompresión de archivos_**

Para bajar el tamaño de los archivos podemos usar el comando _gzip nombre de archivo_
para descomprimir usamos _gzip -d nombre del archivo_

## **_combinacion de archivos_**

Con la herramienta _tar cf nombre del archivo_ combinamos nuestros archivos que estan dentro del directorio señalado, para sacarlo del agrupamiento _tar xf nombre del archivo_

En este proceso no se comprime se esta agrupando y desagrupando.

_tar czf nombre del archivo/*_ comprime todos los archivos 
_tar xzf nombre del archivo_ descomprime todos los archivos

  ## **_Archivo de texto y utilidades interactivas_**

  * Binarios: son programas ejecutables y archivos de datos  
  + cd ~ nos lleva al home o raiz 
  + cd  - lleva al ultimo directorio 

  __vim:__ permite editar texto, se usa de la siguiente manera _vim nombre de archivo_, con la letra _i_ se activa el texto ,con _esc_ salimos de la edicion de texto, guardamos _:w _y salimos de texto con _:q_

  permite crear un nuevo archivo  _vim archivo nuevo_, con _i_ ingresa texto, con _esc_ salimos de texto _:x_ graba y sale a la terminal.

  __nano:__ permite editar texto, ingresa con _nano nombre del archivo_, permite editar inmediatamente, con _control x_ sale de programa , confirma guardar los cambios ejecutados diciendo que si  y sale con los indicadores de la parte inferior. 

## **_utilidades batch y batch avanzadas_**

Son herramientas a las que se e pasa toda la informacion y luego arroja resultados 

+ __cat__  muestra el contenido completo de un archivo

+ __head__ muestra las primeras lineas del archivo, _head  -n_ nos permite mirar el numero de lineas que quiero ver iniciando  por ejemplo _head -n 5_ nos muetsra las primeras 5 lineas del texto , con el comando _tail -n 5_ nos muestra lo inverso, es decir muestra las ultimas lineas en este caso las ultimas 5.

por defecto si escribimos _head  nombre del archivo_, nos muestra las primeras 10 lineas de texto, al igual que si usamos _tail nombre del archivo_ nos muestra las ultimas diez lineas de texto 

* __grep__ es una busqueda por expresiones regulares, con el comando _grep la palabra buscar nombre de archivo_, trae la palabra que buscamos de ese archivo, si escribimos _grep -i palabra a buscar nombre del archivo_, nos muestra la palabra sin tomar en cuenta mayusculas

+ __sed__ _- string editor_ es un tratamiento de flujos de caracteres,El comando _sed_ es un editor de texto no interactivo. El comando _sed_ de Linux edita datos basado en las reglas que tú le proporciones, por ejemplo si yo quiero cambiar dentro del archivo de texto una palabra seria  _'s/palabra a cambiar/palabra nueva/g' nombre del archivo de texto_  "la última g indica que es global, que esta mirando todo el archivo"

Esto no guarda ni cambia el archivo, se modifica el flujo mas no el texto.

_sed '$d' nombre del archivo_, esto elimina la ultima linea en el flujo 

+ __awk__ tratamiento de texto delimitado _awk -f ';' '{print $1}_ archivo  muestra la primera columna de ese archivo


## herramientas de busqueda de archivos

+ __locate__ permite buscar archivos con solo nombrarlo, debe estar actualizada la base de daos para no tener incomvenientes, _locate nombre de archivo_

+ __whereis__ busca archivos binarios, comandos , _whereis comando_   

+ __find__ buscar en un arbol de directorios ejemplo _find nombre de archivo permiso_ con  _find . -type f -mtime +7_  va  a pedir que devuelva archivos que sean modifiicados hace mas de siet dias 
Para ejecutarlos escribes _find . -type f -mtime +7 -exec cp {} ,/nombrearchivo/\;_





[volver al indice](./README.md)