# Comandos básicos de linux

El intérprete de comandos espera que le indiquemos una línea de órdenes para ejecutar la tarea que le hayamos indicado.  

La sintáxis básica de una orden es **comando** [**opciones**] [**parametros**].  

Con el **COMANDO** le indico qué tiene que hacer, en las opciones cómo debe hacerlo y con los parámetros le indico los elementos donde tendrá que realizar la acción.  

Puedo obtener ayuda de cualquier comando usando `man [comando]`

### Comandos del sistema de ficheros

* El comando `pwd` muestra el directorio actual.
* El comando `cd` cambia de directorio.
* El carácter `~` hace referencia al directorio personal del que ejecuta la orden.
* El comando `ls` lista el contenido de un directorio. Las opciones comunes que modifican cómo se mostrará la informació son:  
  * `-l` lista con detalle.
  * `-h` muestra el tamaño más legible.
  * `-a` muestra los ocultos.
  * `-S` ordena por tamaño.
  * `-t` ordena por fecha.
  * `-r` invierte el criterio de ordenación.
*  Para indicar dónde se encuentra un elemento del sistema de ficheros (un archivo o un directorio), se utilizan **rutas**.  
   Estas pueden ser **absolutas** (indico todos los directorios que tengo que seguir desde la raíz del sistema) o **relativas** (indico el camino desde el directorio donde ejecuto la orden).
*  Las rutas **absolutas** siempre empiezan por una barra `/` (que indica la raíz).
*  Si utilizo `..` en una ruta estoy haciendo referencia al directorio padre. Un único punto indica el directorio actual.
*  Linux distingue entre **mayúsculas y minúsculas**.
*  Si quiero usar espacio en un nombre deberé ponerlo entre comillas `[""]` o con un carácter de escape `[\]`.
*  Usando los cursores arriba y abajo en la terminal, aparecerán las últimas ordenes que he ejecutado.
*  El tabulador ayuda para terminar de escribir una ruta.
*  Con `Control+R` puedo buscar en el **historial de instrucciones**.
*  El comando `history`  muestra el historial de instrucciones y puedo ejecutarlas usando **![numero_instrucción]**. 
*  El comando `mkdir` sirve para crear directorios.
*  El comando `rm` borra ficheros, y con `-r` directorios
*  El comando `touch` crea ficheros vacíos.
*  El comando `mv` mueve elementos o cambia su nombre.
*  El comando `cp` copia ficheros y directorios.
*  El símbolo asterisco `[*]` equivale a cualquier secuencia de caracteres en el nombre de un elemento.
*  El símbolo interrogación `[?]` equivale a un sólo carácter, puediendo éste ser cualquiera.

### Administarción de software

Linux utiliza repositorios, que son servidores en Internet que se encargan de guardar los ficheros necesarios para que  
funcione en una máquina linux.  

Es decir, nosotros consultamos a esos servidores y vemos que paquetes tiene disponibles y automáticamente con las
herramientas que nos ofrece linux, podemos descargar esos paquetes e instalarlos de una forma muy sencilla.

Existe un fichero de configuración `sources.list` donde estan guardados estos repositorios y este se encuentra en `/etc/apt/sources.list`.

El comando `apt update` lo que hace es decirle al sistema que vuelva a preguntar a esos servidores para actualizar 
la información de los paquetes disponibles.

Ahora por ejemplo, estoy buscando un reproductor, por ejemplo **vlc**, en este caso sería con el comando `apt-cache`,
cache porque ya nos vamos a basar en la lista de paquetes que tenemos ya en el ordenado, y el comando final sería:
`apt-cache search vlc` y se mostrar toda una lista de paquetes y entre esas opciones debería apararecer disponible el
paquete **vlc** y una vez verificado se puede instalar `apt-get install vlc`.

* El comando `apt-get remove [paquete]` solo desinstala el programa, pero todavía deja archivos de configuración en el sistema.
* El comando `apt-get purge [paquete]` elimina totalmente toda referencia del programa.





