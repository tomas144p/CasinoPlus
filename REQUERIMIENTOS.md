#### TOMA DE REQUERIMIENTOS

### Contexto 

    Los clientes de un casino, no son notificados de los beneficios de unirse al club de dicho casino, ni de cuando ellos son ganadores perdiendo asi oportunidades de crear juego en los clientes casuales y frecuentes.

### Antecedentes del cliente

    El Lucky 38, es un casino que ha funcionado desde hace años en Chile, pero su tecnologia empieza a quedarse atras, ralentizando su avance y su competitividad con otros casinos de la zona, aun asi, se establece como un "Clasico incomparable" entre clientes de variadas experiencias

### Que se espera que el software haga

    Se espera que el software asista al personal y a los clientes a tener una experiencia mas fluida y clara dentro del establecimiento, impidiendo contratiempos que causan molestia en los clientes

## Requerimientos funcionales

    Otorgar y almacenar informacion del usuario

    Notificar al cliente que ganaron-perdieron en caso de participar en un Sorteo.

## Requerimientos no funcionales

    Asistir en inscripcion a sorteos / torneos

    Otorgar informacion de beneficios y como / donde obtenerlos, asi como de los puntos que ha acumulado el cliente.

    Interfaz amigable con el usuario

    Cofidencialidad de datos

    Notificacion de sorteos futuros

#### Usuarios del software

    Clientes tanto primerizos como frecuentes del casino. (Usuario)

    Personal encargado de sorteos para contrastar informacion personal. (Personal)

    Personas encargadas de subir la informacion para visualizacion de los usuarios. (Administradores)

### Permisos

    Se describen los permisos por perfil

## Usuarios

    Los usuarios podran ver su propia informacion personal, como puntos, sorteos inscritos, informacion de sorteos, entre otros previamente mencionados

## Personal

    El personal no contara con los permisos previos, pues ellos no pueden ser clientes del propio casino, sin embargo, podran visualizar los sorteos y torneos que sucederan, con el fin de promoverlos en vivo y contrastar informacion con los Administradores en caso de ser necesario.

    Tambien deberan revisar la informacion desde el telefono del cliente ganador para verificacion de identidad.

## Administradores

    Los administradores contaran con permisos para enviar mensaje directo a el usuario ganador mediante su ID de cliente, asi como enviar notificaciones de sorteos (Cuando habra un sorteo, la hora del sorteo, el ganador o ganadora del sorteo) y encargarse de mantener a los usuarios informados de sus beneficios.

    Los administradores se encargaran tambien de la inscripcion de Usuarios, pues se debe contrastar si el usuario posee la mayoria de edad y que, en efecto, es el usuario que desea inscribirse (Evitar suplantacion de identidad, multiples cuentas)

### Lo minimo indispensable para empezar (MVP)

    Inscripcion de clientes.

    Almacenamiento de informacion de cliente (Puntos, sorteos, etc).

### MVP por perfil
## Usuario

    Mostrar informacion de usuarios ya inscritos

## Personal

    Creacion de perfil, pues no es indispensable para comenzar pero si sera importante mas tarde

## Administrador

    Notificar ganador de sorteo por ID Cliente

### Datos basicos a almacenar

    Por la naturaleza de este software, debe contener informacion del cliente, como su ID de jugador, su RUT, Nombre y cantidad de puntos acumulados

    Tambien debe almacenar la informacion de los sorteos que estan en proceso o que estaran en proceso


### Post-MVP (Futuras versiones)

    Luego de los requerimientos minimos, se espera que los {Administradores} puedan subir informacion de sorteos / torneos futuros y tendran la posibilidad de añadir usuarios nuevos, los {usuarios} podran inscribirse desde el club del casino, podran revisar su informacion y consultar por torneos / sorteos futuros e implementar el perfil de {Personal}, para que puedan acceder a la informacion de sorteos y torneos sin ser clientes para evitar que el personal pueda salir ganador y mantener informado a los presentadores.
