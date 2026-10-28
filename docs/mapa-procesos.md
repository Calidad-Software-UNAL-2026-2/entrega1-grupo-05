# Mapa de Procesos Clave — AuditTrack

Este documento contiene la caracterización de los procesos clave / misionales del ciclo de vida del software para la plataforma **AuditTrack**, generado automáticamente mediante el workflow de flujo único.

---

### Proceso: Análisis de Requisitos de Software

- **Tipo:** Clave
- **Justificación de la selección:** Permite especificar detalladamente las funcionalidades de creación de auditorías, importación de datos contables, gestión de usuarios y generación de informes financieros automáticos.
- **Entradas:** Modelo verbal de AuditTrack, necesidades del negocio y regulaciones financieras.
- **Actividades:** Elicitación de necesidades de auditores y contadores, redacción de historias de usuario con criterios de aceptación y definición de requisitos no funcionales.
- **Salidas:** Documento de Especificación de Requisitos, historias de usuario cargadas en GitHub Issues (`[RF-XX]`, `[RNF-XX]`) y vista "Registro de Requisitos".
- **Recursos:** Analista de Requisitos / Product Owner, formularios de GitHub Issues.


### Proceso: Diseño y Arquitectura de Software

- **Tipo:** Clave
- **Justificación de la selección:** Define la estructura tecnológica modular en Python y JavaScript, el modelo de base de datos SQL y la arquitectura necesaria para soportar un procesamiento transaccional veloz y seguro.
- **Entradas:** Especificación de Requisitos de Software y métricas de rendimiento y calidad.
- **Actividades:** Diseño de la arquitectura de la aplicación, modelado del esquema entidad-relación SQL, diseño de interfaces del panel de control y definición de APIs de integración.
- **Salidas:** Documento de Arquitectura de Software, modelo relacional de BD SQL y wireframes/diseños de interfaz de usuario.
- **Recursos:** Arquitecto de Software, diseñador UI/UX y herramientas de diagramación (Draw.io / PlantUML).


### Proceso: Construcción y Desarrollo de Software

- **Tipo:** Clave
- **Justificación de la selección:** Materializa en código fuente el motor de análisis automático de transacciones, los módulos de carga de datos financieros y la generación gráfica de informes.
- **Entradas:** Documento de Arquitectura, diseño de base de datos y tareas de desarrollo asignadas.
- **Actividades:** Codificación en Python (backend) y JavaScript (frontend), desarrollo de consultas SQL optimizadas para la regla de <5s por 10,000 transacciones e integración de componentes.
- **Salidas:** Código fuente compilado de AuditTrack en el repositorio Git, componentes de software ejecutables y endpoints de API.
- **Recursos:** Desarrolladores Frontend y Backend, IDEs de programación, lenguajes Python y JavaScript, motor SQL.


### Proceso: Transición y Despliegue

- **Tipo:** Clave
- **Justificación de la selección:** Entrega el sistema AuditTrack en el entorno productivo cloud para que pueda ser utilizado por los auditores y administradores de las empresas cliente.
- **Entradas:** Incremento de software probado y verificado, scripts de despliegue y base de datos configurada.
- **Actividades:** Ejecución de scripts de migración de base de datos SQL, despliegue del código fuente en el servidor de producción y pruebas de humo (smoke tests) post-despliegue.
- **Salidas:** Sistema AuditTrack desplegado y accesible en producción, versión etiquetada (Release Tag).
- **Recursos:** Equipo de despliegue, scripts de integración/despliegue continuo.

