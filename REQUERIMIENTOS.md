
# TOMA DE REQUERIMIENTOS

## 1. Contexto

Los clientes de un casino, no son notificados de los beneficios de unirse al club de dicho casino, ni de cuando los mismos, son ganadores, generando problemas en los sorteos y perdiendo oportunidad de crear juego en los usuarios.

El metodo actual de usuarios del Club es inscripcion manual, y tarjetas del casino, donde para visualizar los beneficios y puntos existe un totem en la totalidad del casino, el cual pasa desapercibido entre las maquinas TGM del local, y este totem es la principal causa de problemas en el casino, donde el sector de boveda debe ir y solucionar el problema, impidiendo el funcionamiento normal del area.

Los sorteos tambien presentan problemas, pues el metodo actual es llamado al escenario del casino para confirmar identidad y premiar al cliente afortunado, para confirmar la identidad se requiere Cedula de identidad al dia y tarjeta del club, es usual que al cliente afortunado olvide su tarjeta en el area de juego en la que se encontraba, y con un limite de tiempo de 90 segundos, no llegan a volver a tiempo, o directamente no tienen su tarjeta o cedula de identidad expirada, produciendo asi, conflictos entre el cliente y los presentadores, asi mismo, afecta tambien la transparencia y la credibilidad del casino, con acusaciones usuales de que "Esta arreglado y por eso no me quieren esperar", "Si fuese un cliente usual no me pedirian mi cedula de identidad", entre muchas otras 

## 2. Antecedentes del cliente

El Lucky 38, es un casino que ha funcionado desde hace años en Chile, pero su tecnologia empieza a quedarse atras, ralentizando su avance y su competitividad con otros casinos de la zona, aun asi, se establece como un "Clasico incomparable" entre clientes de variadas experiencias, asi mismo, su ubicacion es perfecta para atraer clientela primeriza.

## 3. Que se espera que el software haga

Se espera que el software asista al personal y a los clientes a tener una experiencia mas fluida y clara dentro del establecimiento, impidiendo contratiempos que causan molestia en los clientes y los colaboradores del local.

## 4. Requerimientos funcionales

- Otorgar y almacenar informacion del usuario

- Notificar al cliente que ganaron-perdieron en caso de participar en un Sorteo.

## 5. Requerimientos no funcionales

- Asistir en inscripcion a sorteos y torneos

- Otorgar informacion de beneficios, como y donde obtenerlos, asi como de los puntos que ha acumulado el cliente.

- Cofidencialidad de datos

- Notificacion de sorteos futuros

- MongoDB de Docker

## 6. Usuarios del software

- Clientes tanto primerizos como frecuentes del casino. (Usuario)

- Personal encargado de sorteos para contrastar informacion personal. (Personal)

- Personas encargadas de subir la informacion para visualizacion de los usuarios. (Administradores)

## 7. Permisos

Este apartado describe los permisos por perfil del software, los cuales son **"Usuarios", "Personal" y "Administradores".**

### 7.1 Usuarios

Los usuarios podran ver su propia informacion personal, como puntos, sorteos inscritos, informacion de sorteos futuros, entre otros previamente mencionados.

Esto incluye comunmente, clientes del casino inscritos en el club (Previamente y futuramente).

### 7.2 Personal

El personal no contara con los permisos previos, pues ellos no pueden ser clientes del propio casino, sin embargo, podran visualizar los sorteos y torneos que sucederan, con el fin de promoverlos en vivo y contrastar informacion con los Administradores en caso de ser necesario.

Tambien deberan revisar la informacion desde el telefono del cliente ganador para verificacion de identidad, reemplazando asi las tarjetas del club.

Esto incluye al personal encargado de anunciar ganadores, es decir, a los promotores y anunciadores del casino.

### 7.3 Administradores

Los administradores contaran con permisos para enviar mensaje directo a el usuario ganador mediante su ID de cliente, asi como enviar notificaciones de sorteos (Cuando habra un sorteo, la hora del sorteo, el ganador o ganadora del sorteo) y encargarse de mantener a los usuarios informados de sus beneficios.

Los administradores se encargaran tambien de la inscripcion de Usuarios, pues se debe contrastar si el usuario posee la mayoria de edad y que, en efecto, es el usuario que desea inscribirse (Evitar suplantacion de identidad, multiples cuentas).

Por la naturaleza de estos permisos, el personal del club del casino sera administrador, pues ellos se encargan de crear sorteos y contrastar la infromacion (de la manera antigua) del cliente para saber si es el autentico ganador y de añadir usuarios al club.

## 8. Lo minimo indispensable para empezar (MVP)

- Inscripcion de clientes (De manera local).

- Almacenamiento de informacion de cliente (Puntos, sorteos, etc).

## 9. MVP por perfil

Este apartado incluye lo minimo de cada perfil para el funcionamiento basico de la API.

### 9.1 Usuario

Mostrar informacion de usuarios ya inscritos

### 9.2 Personal

Creacion de perfil, pues no es indispensable para comenzar pero si sera importante mas tarde

### 9.3 Administrador

Notificar ganador de sorteo por ID Cliente

## 10. Prioridades

    alta
    media
    baja

## 11. Flujo principal

El cliente se incribe -> Datos iniciales (Nombre, rut, bono de bienvendia) -> Participacion en sorteos

## 12. Datos basicos a almacenar

Por la naturaleza de este software, debe contener informacion del cliente, como su ID de jugador, su RUT, Nombre y cantidad de puntos acumulados

Tambien debe almacenar la informacion de los sorteos que estan en proceso o que estaran en proceso


## 13. Post-MVP (Futuras versiones)

Luego de los requerimientos minimos, se espera que los **Administradores** puedan subir informacion de sorteos / torneos futuros y tendran la posibilidad de añadir usuarios nuevos localmente, los **usuarios** podran inscribirse desde el club del casino, podran revisar su informacion y consultar por torneos y/o sorteos futuros e implementar el perfil de **Personal**, para que puedan acceder a la informacion de sorteos y torneos sin ser clientes para evitar que el personal pueda salir ganador y mantener informado a los presentadores.

## 14. Plazo deseado



Pago inicial

## 15. Definicion de alcance y presupuesto (alcance acordado: solo API con Mongo + Express)

sacatealaverga

## 16. Criterios de aceptacion

**Criterios de aceptación (API)**

- Endpoints responden segun el contrato API (JSON) y pasan pruebas de integracion basica

- No existen errores criticos que impidan operaciones CRUD de usuarios

**Garantia sugerida**

- Los desarrolladores se comprometen a solucionar errores criticos en los primeros 30 dias de uso sin coste adicional al cliente.
