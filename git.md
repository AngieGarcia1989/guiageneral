# Git Y GitHub

En nuestra terminal usamos git para guardar nuestros proyectos, github nos permite tener un flujo de trabajo practico, con git podemos hacer ramas, remotos, fuciones y mucho mas, a continuacion vamos a ver todo lo que podemos ver en git ygithub, podemos trabajar muchas versionaes sin dañar ninguna, y trabajar de manera eficiente en equipo.

__sistema de control de veriones__

 Git, creado por linux , guarda los cambios sin importar cuantos sean 

Algunos comandos y sus funciones:

+ __git init :__ Empieza en tu carpeta un repositorio para guardar los cambios.
+ __git add “nombre del archivo” :__ Agrega ese archivo o cambio al "Staging Area"
+ __git commit -m “Versión 1” :__ Agrega finalmente el cambio realizado y le agrega un mensaje con -m
+ __git add . :__ Agrega todos los archivos a ese Staging Area
+ __git commit -m “Cambios a v1” :__ Aplica los cambios realizados.
+ __git status :__ Muestra el estado de tu respositorio
+ __git show :__ Muestra el historico de los cambios hechos
+ __git log “nombre del archivo” :__ Muestra el historial de ese archivo
+ __git push :__ Envia hacia un repositorio remoto
+ __git pull :__ Trae de un repositorio remoto a tu local

## **_¿Cómo instalar git en windows?_**

Buscamos en google __git__ y lo descargamos, en la parte de __git bash__ debemos asegurarnos que sea asi, solo damos next, estas opciones son debido a que normalmente no se usa en windows el desarrollo, se usa mas que todo linux o sistemas basados en unix, pero con git bash podemos trabajar en windows, de esta manera trabajamos en una terminal emulada de windows.

Debemos asegurarnos de indicar __git from the command line and also from 3rd-party software__

Dando next llegamos a la libreria que debemos usar es __use the OpenSSLlibrary__, damos next y usamos la primera version __checkout windows style-commit unix style-line ending__,next y usamos __sistema use MinTTY__, seguimos dando next  hasta llegar a __install__.Escojemos la siguiemte pantalla __Launch git bash__ y posteriormente nos abre una consola interna  parecida a la de linux, podemos empezar a interactuar con comandos como _ls ,pwd, cd_. Para buscarla vamos  a nuestro inicio y bucamos _Git Bash_ , alli abrira nuestra terminal.

## **_¿Cómo intalar git en Mac?_**

Ingresamos  anuestro safari y buscamos __git__, lo descargamos y una vez vemos una cajita que contiene nuestro programa ,le damos doble click a este paquete para abrir , en ocaciones nos niega la apertura ya que dice ser de un desarrollador no identificado, si te aparece asi solo das __ok__, __clik derecho y open, open__ y abres , colocas __continue, install, contraseña__ y se permite la instalacion. 

Para abrirla solo das en el buscador _terminal_ y enter, alli vas abrir tu ventana de terminal, alli puedes escribir comandos como _git_, que te va a mostrar la informacion de git, asi vas a confirmar que tu descarga fue efectiva y correcta  o _git --version_ y te muestra la version exacta que tienes.


## **_¿Cómo intalar git en Linux?_**
__sudo apt-get update__ es actualizar todos los archivos. 
__sudo apt-get install git__ y de esta manera ya instalamos nuestro git, podemos verificarlo en _git --version_ y te muestra la version exacta que tienes.


## **_Editores de código, archivos binarios y de texto plano_**

"_Un editor de código es una herramienta que nos brinda muchas ayudas para escribir código, algo así como un bloc de notas muy avanzado. Los editores más populares son VSCode, Sublime Text y Atom, pero no necesariamente debes usar alguno de estos para continuar con el curso._

_Tipos de archivos y sus diferencias:_

_Archivos de Texto (.txt): Texto plano normal y sin nada especial. Lo vemos igual sin importar dónde lo abrImos, ya sea con el bloc de notas o con editores de texto avanzados._

_Archivos RTF (.rtf): Podemos guardar texto con diferentes tamaños, estilos y colores. Pero si lo abrimos desde un editor de código, vamos a ver que es mucho más complejo que solo el texto plano. Esto es porque debe guardar todos los estilos del texto y, para esto, usa un código especial un poco difícil de entender y muy diferente a los textos con estilos especiales al que estamos acostumbrados._

_Archivos de Word (.docx): Podemos guardar imágenes y texto con diferentes tamaños, estilos o colores. Al abrirlo desde un editor de código podemos ver que es código binario, muy difícil de entender y muy diferente al texto al que estamos acostumbrados. Esto es porque Word está optimizado para entender este código especial y representarlo gráficamente._

_Recuerda que debes habilitar la opción de ver la extensión de los archivos, de lo contrario, solo podrás ver su nombre. La forma de hacerlo en Windows es Vista > Mostrar u ocultar > Extensiones de nombre de archivo._"

 __tomado de John Freddy vega__

 Descargamos en google o safari nuestro visual code que es el mas popular como editor de codigo.

## __¿Qué es el staging y los repositorios? Ciclo básico de trabajo en Git__
Para iniciar un repositorio, o sea, activar el sistema de control de versiones de Git en tu proyecto, solo debes ejecutar el comando _git init._

Este comando se encargará de dos cosas: primero, crear una carpeta _.git_, donde se guardará toda la base de datos con cambios atómicos de nuestro proyecto; y segundo, crear un área que conocemos como Staging, que guardará temporalmente nuestros archivos (cuando ejecutemos un comando especial para eso) y nos permitirá, más adelante, guardar estos cambios en el repositorio (también con un comando especial).

__Ciclo de vida o estados de los archivos en Git:__

Cuando trabajamos con Git nuestros archivos pueden vivir y moverse entre 4 diferentes estados (cuando trabajamos con repositorios remotos pueden ser más estados, pero lo estudiaremos más adelante):

+ __Archivos Tracked:__  son los archivos que viven dentro de Git, no tienen cambios pendientes y sus últimas actualizaciones han sido guardadas en el repositorio gracias a los comandos git add y git commit.

+ __Archivos Staged:__  son archivos en Staging. Viven dentro de Git y hay registro de ellos porque han sido afectados por el comando git add, aunque no sus últimos cambios. Git ya sabe de la existencia de estos últimos cambios, pero todavía no han sido guardados definitivamente en el repositorio porque falta ejecutar el comando git commit.

+ __Archivos Unstaged:__ entiéndelos como archivos “Tracked pero Unstaged”. Son archivos que viven dentro de Git pero no han sido afectados por el comando git add ni mucho menos por git commit. Git tiene un registro de estos archivos, pero está desactualizado, sus últimas versiones solo están guardadas en el disco duro.

+ __Archivos Untracked:__ son archivos que _NO_ viven dentro de Git, solo en el disco duro. Nunca han sido afectados por git add, así que Git no tiene registros de su existencia.

Recuerda que hay un caso muy raro donde los archivos tienen dos estados al mismo tiempo:_staged y untracked._

 Esto pasa cuando guardas los cambios de un archivo en el área de Staging (con el comando git add), pero antes de hacer commit para guardar los cambios en el repositorio haces nuevos cambios que todavía no han sido guardados en el área de Staging (en realidad, todo sigue funcionando igual pero es un poco divertido).

__Comandos para mover archivos entre los estados de Git:__

+ __git status:__ nos permite ver el estado de todos nuestros archivos y carpetas.
+ __git add:__ nos ayuda a mover archivos del Untracked o Unstaged al estado Staged. Podemos usar _git nombre-del-archivo-o-carpeta_ para añadir archivos y carpetas individuales o _git add -A_ para mover todos los archivos de nuestro proyecto (tanto Untrackeds como unstageds).
+ __git reset HEAD:__ nos ayuda a sacar archivos del estado Staged para devolverlos a su estado anterior. Si los archivos venían de Unstaged, vuelven allí. Y lo mismo se venían de Untracked.
+ __git commit:__ nos ayuda a mover archivos de Unstaged a Staged. Esta es una ocasión especial, los archivos han sido guardado o actualizados en el repositorio. Git nos pedirá que dejemos un mensaje para recordar los cambios que hicimos y podemos usar el argumento -m para escribirlo (git commit -m "mensaje").
+ __git rm:__ este comando necesita alguno de los siguientes argumentos para poder ejecutarse correctamente:
 
  + _git rm --cached:_ Mueve los archivos que le indiquemos al estado Untracked.
  
  + _git rm --force:_ Elimina los archivos de Git y del disco duro. Git guarda el registro de la existencia de los archivos, por lo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados).

  ## __¿Qué es un Branch (rama) y cómo funciona un Merge en Git?__

Git es una base de datos muy precisa con todos los cambios y crecimiento que ha tenido nuestro proyecto. Los commits son la única forma de tener un registro de los cambios. Pero las ramas amplifican mucho más el potencial de Git.

Todos los commits se aplican sobre una rama. Por defecto, siempre empezamos en la rama master (pero puedes cambiarle el nombre si no te gusta) y creamos nuevas ramas, a partir de esta, para crear flujos de trabajo independientes.

Crear una nueva rama se trata de copiar un commit (de cualquier rama), pasarlo a otro lado (a otra rama) y continuar el trabajo de una parte específica de nuestro proyecto sin afectar el flujo de trabajo principal (que continúa en la rama master o la rama principal).

Los equipos de desarrollo tienen un estándar: Todo lo que esté en la rama master va a producción, las nuevas features, características y experimentos van en una rama “development” (para unirse a master cuando estén definitivamente listas) y los issues o errores se solucionan en una rama “hotfix” para unirse a master tan pronto como sea posible.

Crear una nueva rama lo conocemos como _Checkout._ Unir dos ramas lo conocemos como _Merge._

Podemos crear todas las ramas y commits que queramos. De hecho, podemos aprovechar el registro de cambios de Git para crear ramas, traer versiones viejas del código, arreglarlas y combinarlas de nuevo para mejorar el proyecto.

Solo ten en cuenta que combinar estas ramas (sí, hacer _“merge”_) puede generar conflictos. Algunos archivos pueden ser diferentes en ambas ramas. Git es muy inteligente y puede intentar unir estos cambios automáticamente, pero no siempre funciona. En algunos casos, somos nosotros los que debemos resolver estos conflictos “a mano”.

## __Crea un repositorio de Git y haz tu primer commit__

Si quieres ver los archivos ocultos de una carpeta puedes habilitar la opción de Vista > Mostrar u ocultar > Elementos ocultos (en Windows) o ejecutar el comando ls -a.

Le indicaremos a Git que queremos crear un nuevo repositorio para utilizar su sistema de control de versiones. Solo debemos posicionarnos en la carpeta raíz de nuestro proyecto y ejecutar el comando git init.

Recuerda que al ejecutar este comando (y de aquí en adelante) vamos a tener una nueva carpeta oculta llamada .git con toda la base de datos con cambios atómicos en nuestro proyecto.

Recuerda que Git está optimizado para trabajar en equipo, por lo tanto, debemos darle un poco de información sobre nosotros. No debemos hacerlo todas las veces que ejecutamos un comando, basta con ejecutar solo una sola vez los siguientes comandos con tu información:

~~~
git config --global user.email "tu@email.com"
git config --global user.name "Tu Nombre" 
~~~
Existen muchas otras configuraciones de Git que puedes encontrar ejecutando el comando git config --list (o solo git config para ver una explicación más detallada).

## __Analizar cambios en los archivos de tu proyecto con Git__

El comando _git show_ nos muestra los cambios que han existido sobre un archivo y es muy útil para detectar cuándo se produjeron ciertos cambios, qué se rompió y cómo lo podemos solucionar. Pero podemos ser más detallados.

Si queremos ver la diferencia entre una versión y otra, no necesariamente todos los cambios desde la creación del archivo, podemos usar el comando _git diff commitA commitB._

Recuerda que puedes obtener el ID de tus commits con el comando _git log._

 si se te olvida agrgar un comentario dentro de un  commit, puedes escribirlo en el momento que te pide escribir el comentario y sales con _esc shift zz_ , lo puedes usar con _vim_ tambien 

## _Volver en el tiempo en nuestro repositorio utilizando branches y checkout_

El comando _git checkout + ID + archivo_  nos permite viajar en el tiempo. Podemos volver a cualquier versión anterior de un archivo específico o incluso del proyecto entero. Esta también es la forma de crear ramas y movernos entre ellas. 

para ir al archivo inicial podemos colocar _git checkout master|archivo 

También hay una forma de hacerlo un poco más “ruda”: usando el comando _git reset_. En este caso, no solo “volvemos en el tiempo”, sino que borramos los cambios que hicimos después de este commit.

Hay dos formas de usar _git reset:_ con el argumento _--hard_, borrando toda la información que tengamos en el área de staging (y perdiendo todo para siempre). O, un poco más seguro, con el argumento _--soft_, que mantiene allí los archivos del área de staging para que podamos aplicar nuestros últimos cambios pero desde un commit anterior.

_git log --stat_ podemos ver los commits con los cambios especificos.

## __Git reset vs. Git rm__

_Texto: @juandc_

 __Git reset y git rm__ son comandos con utilidades muy diferentes, pero aún así se confunden muy fácilmente.

+ __git rm__
Este comando nos ayuda a eliminar archivos de Git sin eliminar su historial del sistema de versiones. Esto quiere decir que si necesitamos recuperar el archivo solo debemos “viajar en el tiempo” y recuperar el último commit antes de borrar el archivo en cuestión.

Recuerda que git rm no puede usarse así nomás. Debemos usar uno de los flags para indicarle a Git cómo eliminar los archivos que ya no necesitamos en la última versión del proyecto:

+ _git rm --cached:_  Elimina los archivos del área de Staging y del próximo commit pero los mantiene en nuestro disco duro.

+ _git rm --force:_ Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados).

__git reset__

Este comando nos ayuda a volver en el tiempo. Pero no como git checkout que nos deja ir, mirar, pasear y volver. Con git reset volvemos al pasado sin la posibilidad de volver al futuro. Borramos la historia y la debemos sobreescribir. No hay vuelta atrás.

Este comando es muy peligroso y debemos usarlo solo en caso de emergencia. Recuerda que debemos usar alguna de estas dos opciones:

Hay dos formas de usar _git reset:_  con el argumento _--hard,_ borrando toda la información que tengamos en el área de _staging_ (y perdiendo todo para siempre). O, un poco más seguro, con el argumento _--soft,_ que mantiene allí los archivos del área de staging para que podamos aplicar nuestros últimos cambios pero desde un commit anterior.

+ _git reset --soft:_ Borramos todo el historial y los registros de Git pero guardamos los cambios que tengamos en Staging, así podemos aplicar las últimas actualizaciones a un nuevo commit.

+ _git reset --hard:_ Borra toda la información de los commits y del área de staging se borra del historial.


__git reset HEAD: Este es el comando para sacar archivos del área de Staging. No para borrarlos ni nada de eso, solo para que los últimos cambios de estos archivos no se envíen al último commit, a menos que cambiemos de opinión y los incluyamos de nuevo en staging con git add.__


__Si usamos git reset HEAD, lo único que haremos será mover cambios de Staging a Unstaged. Seguiremos teniendo los últimos cambios del archivo, el repositorio mantendrá el archivo (no con sus últimos cambios pero sí con los últimos en los que hicimos commit) y no habremos perdido nada__

## __Introducción a las ramas o branches de Git__

Las ramas son la forma de hacer cambios en nuestro proyecto sin afectar el flujo de trabajo de la rama principal. Esto porque queremos trabajar una parte muy específica de la aplicación o simplemente experimentar.

La cabecera o HEAD representan la rama y el commit de esa rama donde estamos trabajando. Por defecto, esta cabecera aparecerá en el último commit de nuestra rama principal. Pero podemos cambiarlo al crear una rama (git branch rama, git checkout -b rama) o movernos en el tiempo a cualquier otro commit de cualquier otra rama con los comandos (git reset id-commit, git checkout rama-o-id-commit).

Recuerda que al ejecutar el comando git checkout para cambiar de rama o commit puedes perder el trabajo que no hayas guardado. Guarda tus cambios antes de hacer git checkout.

podemos guardar nuestros cambios con git commit -am mensajeque queramos y esto da por entendido el git add, esto nos simplifica el proceso de commit

_Recuerda que puedes borrar commits con git reset y ramas con git branch -d_

## __Solución de conflictos al hacer un merge__


Git es muy inteligente y puede resolver algunos conflictos automáticamente: cambios, nuevas líneas, entre otros. Pero algunas veces no sabe cómo resolver estas diferencias, por ejemplo, cuando dos ramas diferentes hacen cambios distintos a una misma línea.

Esto lo conocemos como conflicto y lo podemos resolver manualmente, solo debemos hacer el merge, ir a nuestro editor de código y elegir si queremos quedarnos con alguna de estas dos versiones o algo diferente. Algunos editores de código como VSCode nos ayudan a resolver estos conflictos sin necesidad de borrar o escribir líneas de texto, basta con hundir un botón y guardar el archivo.

Recuerda que siempre debemos crear un nuevo commit para aplicar los cambios del merge. Si Git puede resolver el conflicto hará commit automáticamente. Pero, en caso de no pueda resolverlo, debemos solucionarlo y hacer el commit.

Los archivos con conflictos por el comando git merge entran en un nuevo estado que conocemos como Unmerged. Funcionan muy parecido a los archivos en estado Unstaged, algo así como un estado intermedio entre Untracked y Unstaged, solo debemos ejecutar git add para pasarlos al área de staging y git commit para aplicar los cambios en el repositorio.

