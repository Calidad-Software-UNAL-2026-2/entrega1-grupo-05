# Paso 2.5 — Requisitos de Interfaz

_Interacciones con otros sistemas o servicios mencionados o inferidos
(APIs, pasarelas de pago, servicios de notificación, etc.)._

| Sistema/Servicio externo | Tipo de interacción | Justificación/Origen |
|---|---|---|
| Software contable empresarial | API REST para consultar o intercambiar datos financieros; formato y mecanismo definitivos por equipo técnico. | Integración preferida, derivada de N-8 y del objetivo de automatización. |
| Archivos CSV exportados por software contable | Importación manual de archivos separados por campos para pruebas y operación de respaldo. | Alternativa manual aceptada por el equipo cuando no exista integración por API. |
| Archivos Excel (.xlsx) exportados por software contable | Importación manual estructurada de datos financieros para pruebas y operación de respaldo. | Requerida explícitamente por el equipo. |
| Navegador web | Interfaz web responsive mediante protocolos HTTP/HTTPS. | Permite acceso desde navegadores comunes y cumple el requisito de compatibilidad. |
| Generador de informes Excel | Exportación de informes con formato de revisión claro. | Necesidad N-5 expresada por el gerente financiero. |
| Servicio de autenticación | Validación de credenciales y factor adicional de autenticación; proveedor definitivo por equipo técnico. | Seguridad y autenticación de dos factores declaradas en el modelo verbal. |
| Servicio de correo | Notificaciones opcionales de eventos, accesos o hallazgos; implementación definitiva por equipo técnico. | Inferido para colaboración y alertas; debe aprobarse antes de registrarlo como obligatorio. |
