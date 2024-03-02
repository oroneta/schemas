Collection of documentation, shcemas, logo, design, etc. for the project.


# Spanish
## Documentación
Os explico un poco:

El proyecto se va a reestructurar. Back y Front se mantiene.

—— Back ——
*core-system* Será el sistema que gestiona toda las llamadas de los módulos. Recibirá las peticiones del modulo (Para empezar, siendo simples. Solo vamos a hacer que compruebe rutas) que será la ruta definida, y el core se encarga de ver si existe algún dispositivo del modo que esté (de momento solo de vuelo), en caso de que esté definida el core denegará el vuelo. Todo dispositivo deberá estar registrado, por ello hay un protocolo de matriculas que cada dispositivo la debería recordar con una llave publica, que a la hora de hacer peticiones deberá identificarse con esa llave (se hará asi de simple de momento)
        - Puerto: 80000
        - Tecnología: C (Posiblemente para reducir tiempo se usa Python)
        - Protocolo: HTTP

*drone-modules* Será el modulo que se encargará de gestionar lo que el cliente quiera poner (Solo rutas y alarmas de momento). Por el puerto *80001* en protocolo HTTP se escucha un server que atiende al cliente (API). Por el puerto *80002* está el servidor que recibe el “GET status” de cada drone, y le devolverá las instrucciones que tiene que seguir para continuar la ruta definida. Puerto *80003* protocolo HLS recibe los live-streaming de cada drone (Para poder dar alarma).
         - Tecnología: Node (para los tres servers)

—— Front ——
*drone-front* Servidor que devuelve la interfaz para el cliente y que pueda interactuar con la API de *drone-module*. 
         - Tecnología: LAMP (Apache - PHP)
         - Puerto: Web (80 y 435)


Gracias. Cualquier añadido que me diga. He tenido que simplicar y escoger lo más main. Si tenemos tiempo podemos añadir más cosas.