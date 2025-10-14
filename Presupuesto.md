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