# TERMINAL Y LINEA DE COMANDOS

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

  ## **_Archivo de texto y utilidades interactivas_**

  * Binarios: son programas ejecutables y archivos de datos  
  + cd ~ nos lleva al home o raiz 
  + cd  - lleva al ultimo directorio 

  __vim:__permite editar texto, se usa de la siguiente manera _vim nombre de archivo_, con la letra _i_ se activa el texto ,con _esc_ salimos de la edicion de texto, guardamos _:w _y salimos de texto con _:q_

  permite crear un nuevo archivo  _vim archivo nuevo_, con _i_ ingresa texto, con _esc_ salimos de texto _:x_ graba y sale a la terminal.

__nano:__ permite editar texto, ingresa con _nano nombre del archivo_, permite editar inmediatamente, con _control x_ sale de programa , confirma guardar los cambios ejecutados diciendo que si  y sale con los indicadores de la parte inferior. 

## **_ utilidades batch y batch avanzadas_**

Son herramientas a las que se e pasa toda la informacion y luego arroja resultados 

cat  muestra el contenido completo de un archivo

head muestra las primeras lineas del archivo, head  -n nos permite mirar el numero de lineas que quiero ver iniciando  por ejemplo head -n 5 nos muetsra las primeras 5 lineas del texto , con el comando tail -n 5 nos muestra lo inverso, es decir muestra las ultimas lineas en este caso las ultimas 5.

por defecto si escribimos head  nombre del archivo, nos muestra las primeras 10 lineas de texto, al igual que si usamos tail nombre del archivo nos muestra las ultimas diez lineas de texto 

grep busqueda por expresiones regulares, con el comando grep la palabraa buscar nombre de archivo, trae la palabra que buscamos de ese archivo, si escribimos grep -i palabra a buscar nombre del archivo, nos muestra la palabra sin tomar en cuenta mayusculas

sed - string editor es un tratamiento de flujos de caracteres,El comando sed es un editor de texto no interactivo. El comando sed de Linux edita datos basado en las reglas que tú le proporciones, por ejemplo si yo quiero cambiar dentro del archivo de texto una palabra seria  's/palabra a cambiar/palabra nueva/g' nombre del archivo de texto  "la última g indica que es global, que esta mirando todo el archivo"

esto no guarda ni cambia el archivo, se modifica el flujo mas no el texto.

sed '$d' nombre del archivo, esto elimina la ultima linea en el flujo 

awk tratamiento de texto delimitado awk -f ';' '{print $1} archivo  muestra la primera columna de ese archivo





[volver al indice](./README.md)