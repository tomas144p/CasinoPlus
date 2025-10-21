# TOMA DE REQUERIMIENTOS

## 1. Contexto.

Los clientes de un casino, no son notificados de los beneficios de unirse al club de dicho casino, ni de cuando los mismos, son ganadores, generando problemas en los sorteos y perdiendo oportunidad de crear juego en los usuarios.

El metodo actual de usuarios del Club es inscripcion manual, y tarjetas del casino, donde para visualizar los beneficios y puntos existe un totem en la totalidad del casino, el cual pasa desapercibido entre las maquinas TGM del local, y este totem es la principal causa de problemas en el casino, donde el sector de boveda debe ir y solucionar el problema, impidiendo el funcionamiento normal del area.

Los sorteos tambien presentan problemas, pues el metodo actual es llamado al escenario del casino para confirmar identidad y premiar al cliente afortunado, para confirmar la identidad se requiere Cedula de identidad al dia y tarjeta del club, es usual que al cliente afortunado olvide su tarjeta en el area de juego en la que se encontraba, y con un limite de tiempo de 90 segundos, no llegan a volver a tiempo, o directamente no tienen su tarjeta o cedula de identidad expirada, produciendo asi, conflictos entre el cliente y los presentadores, asi mismo, afecta tambien la transparencia y la credibilidad del casino, con acusaciones usuales de que "Esta arreglado y por eso no me quieren esperar", "Si fuese un cliente usual no me pedirian mi cedula de identidad", entre muchas otras.

## 2. Antecedentes del cliente.

El Lucky 38, es un casino que ha funcionado desde hace años en Chile, pero su tecnologia empieza a quedarse atras, ralentizando su avance y su competitividad con otros casinos de la zona, aun asi, se establece como un "Clasico incomparable" entre clientes de variadas experiencias, asi mismo, su ubicacion es perfecta para atraer clientela primeriza.

## 3. Que se espera que el software haga.

Se espera que el software asista al personal y a los clientes a tener una experiencia mas fluida y clara dentro del establecimiento, impidiendo contratiempos que causan molestia en los clientes y los colaboradores del local.

## 4. Requerimientos funcionales.

- Otorgar y almacenar informacion del usuario.

- Notificar al cliente que ganaron-perdieron en caso de participar en un Sorteo.

## 5. Requerimientos no funcionales.

- Asistir en inscripcion a sorteos y torneos.

- Otorgar informacion de beneficios, como y donde obtenerlos, asi como de los puntos que ha acumulado el cliente.

- Cofidencialidad de datos.

- Notificacion de sorteos futuros.

- MongoDB de Docker.

## 6. Usuarios del software.

- Clientes tanto primerizos como frecuentes del casino. (Usuario)

- Personal encargado de sorteos para contrastar informacion personal. (Personal)

- Personas encargadas de subir la informacion para visualizacion de los usuarios. (Administradores)

## 7. Permisos.

//Este apartado describe los permisos por perfil del software, los cuales son **"Usuarios", "Personal" y
//"Administradores".**.
-------------------------------------------------------
Contexto:
La gerarquia de las asignaciones del software cabe en 3 perfiles que son los usuarios, el personal y los administradores, en el mismo software los administradores asignan al personal y asi mismo el personal puede crear perfiles de los clientes nuevos que ingresen al club.

Usuarios/Clientes:
-Interacciones de los usuarios con el software:
Se entiende que el software generado tendra una interfaz para el usuario/cliente, donde en él se asigna una id al crear su tarjeta virtual (Datos basicos para crear la tarjeta virtual "Nombre, Apellido, Rut, Telefono, Correo Electrónico"), tendra acceso a un perfil donde el mismo puede subir su informacion personal (no como un blog sino mas como un cuestionario de datos no escenciales al crear la tarjeta).
-Seguridad:
Los usuarios no pueden ver la informacion personal de otros usuarios.
Los usuarios no pueden modificar datos bancarios o del casino desde la aplicacion.


Este apartado describe los permisos por perfil del software, los cuales son **"Usuarios", "Personal" y "Administradores".**.

### 7.1 Usuarios/Cliente.
Se definen como Usuario/Cliente:
Cualquier Individuo que obtenga una tarjeta del club y sus ventajas son que
podran ver su propia informacion personal, como puntos, sorteos inscritos, informacion de sorteos futuros, entre otros previamente mencionados.
Cada tarjeta virtual contiene un id unico asignado al usuario.
Restricciones como Usuario/Cliente:
La tarjeta del club solo es una manera de gestion de puntos y por ende no tendra
espacio para transacciones o funciones comunes de las tarjetas de credito.

### 7.2 Personal.

El personal no contara con los permisos previos, pues ellos no pueden ser clientes del propio casino, sin embargo, podran visualizar los sorteos y torneos que sucederan, con el fin de promoverlos en vivo y contrastar informacion con los Administradores en caso de ser necesario.

Tambien deberan revisar la informacion desde el telefono del cliente ganador para verificacion de identidad, reemplazando asi las tarjetas del club.

Esto incluye al personal encargado de anunciar ganadores, es decir, a los promotores y anunciadores del casino.

### 7.3 Administradores.

Los administradores contaran con permisos para enviar mensaje directo a el usuario ganador mediante su ID de cliente, asi como enviar notificaciones de sorteos (Cuando habra un sorteo, la hora del sorteo, el ganador o ganadora del sorteo) y encargarse de mantener a los usuarios informados de sus beneficios.

Los administradores se encargaran tambien de la inscripcion de Usuarios, pues se debe contrastar si el usuario posee la mayoria de edad y que, en efecto, es el usuario que desea inscribirse (Evitar suplantacion de identidad, multiples cuentas).

Por la naturaleza de estos permisos, el personal del club del casino sera administrador, pues ellos se encargan de crear sorteos y contrastar la infromacion (de la manera antigua) del cliente para saber si es el autentico ganador y de añadir usuarios al club.

## 8. Lo mínimo indispensable para empezar. (MVP)

- Inscripcion de clientes (De manera local).

- Almacenamiento de informacion de cliente (Puntos, sorteos, etc).

## 9. MVP por perfil.

Este apartado incluye lo minimo de cada perfil para el funcionamiento basico de la API.

### 9.1 Usuario.

Mostrar informacion de usuarios ya inscritos.

### 9.2 Personal.

Creacion de perfil, pues no es indispensable para comenzar pero si sera importante mas tarde.

### 9.3 Administrador.

Notificar ganador de sorteo por ID Cliente.

## 10. Prioridades.

    alta
    media
    baja

## 11. Flujo principal.

El flujo principal describe el recorrido típico del usuario, desde su inscripción en el sistema hasta su participación y eventual notificación en sorteos, incluyendo las interacciones del personal y los administradores.

### 11.1 Registro del Cliente (Usuario)

El cliente se acerca al mostrador del casino o accede al sistema desde un punto autorizado (como una tablet o stand digital).

El personal o el propio usuario ingresa los datos básicos requeridos para crear la tarjeta virtual del club, incluyendo:

- Nombre completo.

- RUT.

- Teléfono.

- Correo Electrónico.

El sistema valida que el usuario:

- Sea mayor de edad (≥18 años).

- No posea una cuenta duplicada.

Una vez validado, se genera una ID única para el cliente y se le asigna un bono de bienvenida inicial (por ejemplo, puntos o una participación gratuita en un sorteo).

El usuario puede acceder a su perfil en la aplicación para consultar sus puntos, sorteos activos, beneficios y notificaciones.

### 11.2 Participación en Sorteos y Torneos

El sistema muestra al usuario los sorteos o torneos disponibles, con detalles como:

- Nombre del evento.

- Fecha y hora del sorteo.

- Requisitos de participación.

- Premios disponibles.

El cliente puede inscribirse con un solo clic o escaneo de código QR desde su tarjeta virtual.

Una vez inscrito, el sistema registra su participación en la base de datos y actualiza su perfil con el evento correspondiente.

Los administradores pueden enviar recordatorios automáticos o manuales sobre los sorteos próximos.

### 11.3 Realización del Sorteo

En el momento del sorteo, el sistema selecciona al ganador de forma aleatoria entre los inscritos.

El administrador o personal designado recibe una notificación interna con el ID del cliente ganador.

El administrador verifica la identidad del ganador a través de la aplicación (revisando la información en su teléfono o dispositivo móvil del casino).

En caso de validación exitosa, el sistema envía una notificación inmediata al usuario ganador indicando que ha resultado seleccionado.

Si el usuario se encuentra dentro del establecimiento, el personal puede confirmar en vivo su identidad mediante el ID de cliente y otorgar el premio.

### 11.4 Notificación y Registro del Ganador

El sistema registra automáticamente el resultado del sorteo (ganador, hora, tipo de premio, validación).

El administrador puede publicar la información del ganador en una sección de resultados dentro del sistema o en pantallas del casino, respetando la confidencialidad de los datos personales (solo se muestra nombre parcial o ID).

El usuario ganador recibe en su perfil una notificación permanente del premio obtenido y el estado del canje (pendiente, entregado, expirado).

### 11.5 Gestión Continua del Cliente

El sistema acumula puntos o beneficios a medida que el usuario participa en sorteos, torneos o realiza actividades dentro del casino.

Los usuarios pueden consultar su historial de sorteos, puntos acumulados, beneficios activos y próximos eventos desde su perfil.

Los administradores y personal pueden actualizar, eliminar o corregir datos en caso de inconsistencias o cambios en la cuenta del usuario.

En caso de pérdida de acceso, el personal puede reemitir la tarjeta virtual o restablecer el perfil del usuario mediante validación de identidad.

### 11.6 Flujo Resumido General

Usuario: Se registra → obtiene ID y bono → participa en sorteos → recibe notificaciones.

Personal: Asiste a usuarios en el registro → verifica ganadores → comunica resultados en vivo.

Administrador: Supervisa inscripciones → gestiona sorteos → envía notificaciones → mantiene base de datos actualizada.

## 12. Datos básicos a almacenar.

Por la naturaleza de este software, debe contener informacion del cliente, como su ID de jugador, su RUT, Nombre y cantidad de puntos acumulados.

Tambien debe almacenar la informacion de los sorteos que estan en proceso o que estaran en proceso.


## 13. Post-MVP. (Futuras versiones)

Luego de los requerimientos minimos, se espera que los **Administradores** puedan subir informacion de sorteos / torneos futuros y tendran la posibilidad de añadir usuarios nuevos localmente, los **usuarios** podran inscribirse desde el club del casino, podran revisar su informacion y consultar por torneos y/o sorteos futuros e implementar el perfil de **Personal**, para que puedan acceder a la informacion de sorteos y torneos sin ser clientes para evitar que el personal pueda salir ganador y mantener informado a los presentadores.

## 14. Plazo deseado.



Pago inicial.

## 15. Definicion de alcance y presupuesto (alcance acordado: solo API con Mongo + Express).

**ALCANCE INCLUIDO:**

**Infestructura**
- API REST desarrollada con Express.js.
- Base de datos MongoDB en contenedor Docker.
- Autenticación JWT por perfiles de usuario.
- Documentación API.

**Modelos de Datos**
- Usuarios/Clientes. (nombre, RUT, puntos, beneficios)
- Sorteos y Torneos. (estado, fechas, participantes)
- Notificaciones. (ganadores, sorteos futuros)

**Endpoints Principales**

/users - CRUD usuarios
/raffles - Gestión de sorteos
/notifications - Notificaciones a usuarios
/auth - Autenticación por perfiles

**PRESUPUESTO ESTIMADO:**

| Item | Valor | Descripción |
|------|-------|-------------|
| **RECURSOS HUMANOS** | | |
| Desarrolladores | $1.920.000 | 2 semanas (C/U (4)) $480.000/semana |
| Arquitecto DB | $300.000 | 1 semana de trabajo |
| **LICENCIAS Y HERRAMIENTAS** | | |
| Licencias Software | $80.000 | -- |
| Monitorización API | $600.000 | -- |
| **INFRAESTRUCTURA** | | |
| Configuración MongoDB | $100.000 | Docker + seguridad |
| Contenedores Docker | $150.000 | Configuración |
| **DOCUMENTACIÓN** | | |
| Documentación Técnica | $75.000 | Manuales técnicos |
| Documentación Usuario | $80.000 | Manuales administrativos |
| **GASTOS OPERACIONALES** | | |
| Gestión de Proyecto | $300.000 | 15% del desarrollo |
| Fondo Contingencia | $250.000 | 10% del total |
| **SUBTOTAL** | **$3.855.000** | |
| **IVA (19%)** | **$732.450** | |


## 16. Criterios de aceptación.

**Criterios de aceptación (API)**

- Endpoints responden segun el contrato API (JSON) y pasan pruebas de integracion basica.

- No existen errores criticos que impidan operaciones CRUD de usuarios.

**Garantia sugerida**

- Los desarrolladores se comprometen a solucionar errores criticos en los primeros 30 dias de uso sin coste adicional al cliente.
