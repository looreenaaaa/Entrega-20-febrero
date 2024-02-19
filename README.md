# Entrega-20-febrero
Hecho por Jaime Más, Mario González, Unai Aguirre y Lorena Peñas

                          ~~~~~ PROGRAMA 2 ~~~~~
Para crear este script, hemos tenido que crearlo dentro de la bash usando el comando 'nano', seguido del nombre del programa; en nuestro caso 'programa2.sh' (.sh siendo la extensión de los scripts).
Escribiendo esto, y haciendo click en ENTER, ya estaremos dentro de la bash. Para guardar, usamos CTRL O y para salir de dicha bash, usamos CTRL X.
En cuanto a ejecutarlo, debemos escribir en la línea de comandos 'bash programa2.sh', seguido de la tecla ENTER.

Hemos comprobado que este programa funciona escribiendo 'ls' cada vez que se crea o borra un directorio/fichero, para asegurarnos de que, efectivamente, nuestro programa funcionaba perfectamente.

Código del script:
La cabecera para todos los scripts es '#!/bin/bash', así que hemos comenzado por escribirlo como la primera linea de todas en nuestros 3 diferentes programas. El método declarado llamado 'menu()' contiene dentro el comando 'clear' (borra todas las líneas anteriores —estética) y todas las opciones que queremos que imprima por pantalla, utilizando el comando 'echo' seguido del texto entre comillas. Nótese que hay una llave que denota el principio y el final del menú.
En la línea 13 llamamos al menú para que ejecute de la manera que hemos programado. Después, otro 'echo' para preguntar al usuario qué opción elige. Para que la bash detecte la opción escrita, debemos utilizar el comando 'read opcion' para ello, y a continuación utilizar un 'case $opcion in' para que, dependiendo de la opción que se elija, hacer una cosa u otra. Hay además un '$' antes de 'opción' para simplificar y llamar a la opción introducida por teclado. 
En el caso de que se haya introducido la opción 1, se ejecutaría la línea 17, que consiste en introducir el nombre del directorio que queremos crear (imprimimos esta instrucción con 'echo'), para después leerlo con 'read' y crearlo con 'mkdir' (todo esto separado con ';'). 
En el segundo caso, se ejecutaría la línea 18, que imprimiría que el usuario introduzca el nombre del directorio que se quiere borrar, lo lea, y lo borre con el comando 'rmdir', seguido del $directorio seguido del $directorio. 
La línea 19 se correspondería a la tercera y última opción; la de crear un fichero. Para ello, imprimimos con 'echo' que introduzca el nombre de fichero a crear, lo lea con 'read', y lo cree con 'touch', seguido del $fichero.
Es además importante cerrar este 'case' con un 'esac' ('case' al revés) para que sea capaz de ejecutarse con éxito.
