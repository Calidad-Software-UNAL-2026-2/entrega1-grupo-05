# Paso 3 — Mapa de Procesos y Modelo de Ciclo de Vida

## 1. Qué se hace aquí y qué se hace en GitHub Actions

Esta página es el lugar donde se caracteriza el **mapa de procesos completo** del proyecto: procesos **estratégicos**, **de apoyo** y **clave/misionales**.

El workflow de GitHub Actions (`.github/workflows/mapa-procesos-*.yml`), que genera `docs/mapa-procesos.md`, **solo representa los procesos clave/misionales** — es decir, los procesos técnicos del ciclo de vida del software (p. ej. Requisitos, Diseño, Implementación, Testing). Los procesos estratégicos y de apoyo **no se representan ahí**: se caracterizan únicamente en esta página.

En resumen:

| Tipo de proceso | Dónde se caracteriza |
|---|---|
| Estratégico | Solo aquí |
| De apoyo | Solo aquí |
| Clave / misional | Aquí **y** en `docs/mapa-procesos.md` (vía el workflow de Actions) |

## 2. Selección y tailoring de procesos

De los procesos del ciclo de vida de la **ISO/IEC/IEEE 12207:2017**, seleccione los pertinentes al alcance del proyecto, clasificándolos en las tres categorías anteriores, y justifique brevemente por qué se incluye cada uno (*tailoring*). No es necesario citar textualmente ninguna cláusula en este paso — eso solo aplica al Paso 7.

## 3. Molde de caracterización (copiar y pegar por cada proceso)

Use este bloque una vez por cada proceso seleccionado, sin importar su tipo:

```
### Proceso: <Nombre del proceso>

- **Tipo:** Estratégico / De apoyo / Clave
- **Justificación de la selección:** <por qué se incluye este proceso en el tailoring del proyecto>
- **Entradas:** <...>
- **Actividades:** <...>
- **Salidas:** <...>
- **Recursos:** <...>
```

### 3.1 Procesos estratégicos

### Proceso: Gestión de Proyectos

**Tipo:** Estratégico
**Justificación de la selección:** Este proceso permite planificar, monitorear y
controlar la ejecución del proyecto AuditTrack durante sus seis meses de duración,
garantizando la entrega oportuna de los módulos de auditoría y el cumplimiento del
presupuesto asignado.
**Entradas:** Propuesta del proyecto AuditTrack, modelo verbal, restricciones de tiempo
(6 meses) y asignación de recursos iniciales.
**Actividades:** Elaboración de la EDT/WBS, estimación de esfuerzo (FPA y PERT),
seguimiento del cronograma mediante la vista Roadmap en GitHub Projects, gestión de hitos y
reuniones de seguimiento.
**Salidas:** Plan de Gestión del Proyecto (PMP), cronograma en diagrama de Gantt,
asignación de hitos y reportes periódicos de avance.
**Recursos:** Director de Proyecto / Scrum Master, entorno de GitHub Projects, hojas de
cálculo para cálculo de esfuerzos.

### Proceso: Gestión de Calidad y Cumplimiento Normativo

**Tipo:** Estratégico
**Justificación de la selección:** Es indispensable para verificar que AuditTrack cumpla
con las estrictas métricas de calidad exigidas, como procesar 10,000 transacciones en menos
de 5 segundos, tiempos de generación de informes inferiores a 3 segundos, disponibilidad
del 99.9% y un puntaje SUS >= 80.
**Entradas:** Requisitos no funcionales de AuditTrack, estándares ISO/IEC/IEEE 12207,
áreas de proceso CMMI y pautas de accesibilidad WCAG 2.1.
**Actividades:** Definición de métricas de calidad, ejecución de auditorías de proceso,
revisión de código fuente y evaluación continua de la tasa de errores críticos.
**Salidas:** Plan de aseguramiento de calidad, reportes de evaluación de usabilidad (SUS)
e informes de cumplimiento de métricas (<1% de errores críticos).
**Recursos:** Líder de Calidad / QA Lead, formularios de evaluación SUS y herramientas de
análisis estático de código.


### 3.2 Procesos de apoyo

### Proceso: Gestión de Seguridad de la Información

**Tipo:** De apoyo
**Justificación de la selección:** AuditTrack maneja estados financieros altamente
sensibles; por lo tanto, se requiere implementar cifrado de datos en reposo y en tránsito,
autenticación de dos factores (2FA) y control de acceso basado en roles para proteger la
confidencialidad.
**Entradas:** Políticas de seguridad empresarial, requerimientos de cifrado y normativas
de protección de datos financieros.
**Actividades:** Configuración de protocolos de cifrado, integración del módulo de
autenticación 2FA, pruebas de penetración y revisión del historial/trazabilidad de
acciones.
**Salidas:** Módulo 2FA integrado, datos financieros cifrados, matriz de control de
accesos y logs de auditoría de seguridad.
**Recursos:** Ingeniero de Ciberseguridad, librerías de cifrado en Python/JavaScript y
proveedor de autenticación 2FA.

### Proceso: Gestión de Infraestructura (DevOps / Cloud)

**Tipo:** De apoyo
**Justificación de la selección:** Provee la plataforma de servidores, bases de datos SQL
y entornos de despliegue necesarios para garantizar un tiempo de actividad (uptime) del
99.9% y alta escalabilidad en la nube.
**Entradas:** Requisitos de disponibilidad (99.9%), rendimiento transaccional y documento
de arquitectura del sistema.
**Actividades:** Aprovisionamiento de servidores cloud, configuración de bases de datos
SQL, implementación de balanceadores de carga y monitoreo de salud del sistema.
**Salidas:** Entornos de desarrollo, pruebas y producción operativos, infraestructura
escalable y planes de respaldo/backup.
**Recursos:** Ingeniero DevOps / SysAdmin, proveedores cloud (AWS/GCP/Azure) y motores de
base de datos SQL.

### Proceso: Documentación y Capacitación

**Tipo:** De apoyo
**Justificación de la selección:** Facilita la adopción de AuditTrack por parte de
auditores, contadores y gerentes financieros, asegurando que la curva de aprendizaje no
supere las dos horas de entrenamiento.
**Entradas:** Requisitos funcionales de los módulos de la plataforma y versiones estables
compiladas.
**Actividades:** Redacción de manuales de usuario por rol (auditor, administrador,
gerente), elaboración de guías de integración con software contable y material didáctico.
**Salidas:** Manual de usuario de AuditTrack, guías de administración del sistema y
material de capacitación.
**Recursos:** Redactor Técnico / Technical Writer, plataforma GitHub Wiki y herramientas
de captura y documentación.

### 3.3 Procesos clave / misionales

> Recuerde: estos procesos, además de caracterizarse aquí, deben quedar representados en `docs/mapa-procesos.md` mediante el workflow de GitHub Actions correspondiente (flujo único o paralelo, según el modelo de ciclo de vida) — ver el `README.md` del repositorio.

### Proceso: Análisis de Requisitos de Software

**Tipo:** Clave
**Justificación de la selección:** Permite especificar detalladamente las funcionalidades
de creación de auditorías, importación de datos contables, gestión de usuarios y generación
de informes financieros automáticos.
**Entradas:** Modelo verbal de AuditTrack, necesidades del negocio y regulaciones
financieras.
**Actividades:** Elicitación de necesidades de auditores y contadores, redacción de
historias de usuario con criterios de aceptación y definición de requisitos no funcionales.
**Salidas:** Documento de Especificación de Requisitos, historias de usuario cargadas en
GitHub Issues (`[RF-XX]`, `[RNF-XX]`) y vista "Registro de Requisitos".
**Recursos:** Analista de Requisitos / Product Owner, formularios de GitHub Issues.

### Proceso: Diseño y Arquitectura de Software

**Tipo:** Clave
**Justificación de la selección:** Define la estructura tecnológica modular en Python y
JavaScript, el modelo de base de datos SQL y la arquitectura necesaria para soportar un
procesamiento transaccional veloz y seguro.
**Entradas:** Especificación de Requisitos de Software y métricas de rendimiento y
calidad.
**Actividades:** Diseño de la arquitectura de la aplicación, modelado del esquema
entidad-relación SQL, diseño de interfaces del panel de control y definición de APIs de
integración.
**Salidas:** Documento de Arquitectura de Software, modelo relacional de BD SQL y
wireframes/diseños de interfaz de usuario.
**Recursos:** Arquitecto de Software, diseñador UI/UX y herramientas de diagramación
(Draw.io / PlantUML).

### Proceso: Construcción y Desarrollo de Software

**Tipo:** Clave
**Justificación de la selección:** Materializa en código fuente el motor de análisis
automático de transacciones, los módulos de carga de datos financieros y la generación
gráfica de informes.
**Entradas:** Documento de Arquitectura, diseño de base de datos y tareas de desarrollo
asignadas.
**Actividades:** Codificación en Python (backend) y JavaScript (frontend), desarrollo de
consultas SQL optimizadas para la regla de <5s por 10,000 transacciones e integración de
componentes.
**Salidas:** Código fuente compilado de AuditTrack en el repositorio Git, componentes de
software ejecutables y endpoints de API.
**Recursos:** Desarrolladores Frontend y Backend, IDEs de programación, lenguajes Python
y JavaScript, motor SQL.

### Proceso: Verificación y Pruebas de Software

**Tipo:** Clave
**Justificación de la selección:** Valida de manera objetiva que AuditTrack no presente
más de 1% de errores críticos, cumpla con la velocidad de respuesta (<3s en informes) y sea
aceptado por los usuarios mediante pruebas SUS.
**Entradas:** Código fuente ejecutable, casos de prueba derivados de requisitos
funcionales y no funcionales.
**Actividades:** Ejecución de pruebas unitarias, de integración, pruebas de carga/estrés
para 10,000 transacciones y sesiones de evaluación de usabilidad SUS con usuarios.
**Salidas:** Reportes de pruebas automatizadas, registro de fallos corregidos y matriz de
trazabilidad de pruebas.
**Recursos:** Ingenieros de Pruebas / QA Testers, frameworks de pruebas (PyTest, Jest) y
herramientas de pruebas de carga.

### Proceso: Transición y Despliegue

**Tipo:** Clave
**Justificación de la selección:** Entrega el sistema AuditTrack en el entorno productivo
cloud para que pueda ser utilizado por los auditores y administradores de las empresas
cliente.
**Entradas:** Incremento de software probado y verificado, scripts de despliegue y base
de datos configurada.
**Actividades:** Ejecución de scripts de migración de base de datos SQL, despliegue del
código fuente en el servidor de producción y pruebas de humo (smoke tests) post-despliegue.
**Salidas:** Sistema AuditTrack desplegado y accesible en producción, versión etiquetada
(Release Tag).
**Recursos:** Equipo de despliegue, scripts de integración/despliegue continuo.


## 4. Diagrama del mapa de procesos

Elabore un diagrama (herramienta libre) que muestre los tres tipos de procesos y su relación entre sí, y arrástrelo directamente a este editor — GitHub lo sube y genera el enlace automáticamente.

<!-- Arrastra aquí la imagen del mapa de procesos -->
