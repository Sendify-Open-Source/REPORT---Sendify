## Capítulo 3: Requirements Specification

## 3.1. To - Be Scenario Mapping

<img width="302" height="512" alt="user 1" src="https://github.com/user-attachments/assets/028b6c58-4166-4c14-98b0-0e675a9ed874" />

## 3.2. User Stories

| **Epic / Story ID** | **Título** | **Descripción** | **Criterios de Aceptación** | **Relacionado con (Epic ID)** |
|--------|---------|-------------|--------|--------|
| Epic-01 | Gestión de Envíos | Como administrador logístico, quiero gestionar envíos para reducir tiempos de operación. | – | – |
| US-01.1 | Crear envío | Como administrador logístico, quiero crear una orden de envío con datos de remitente, destinatario, dirección, peso y costo. | Given usuario autenticado<br>When completa los datos<br>Then se genera código único | Epic-01 |
| US-01.2 | Guardar clientes frecuentes | Como administrador, quiero guardar clientes frecuentes para agilizar futuros envíos. | Given envío creado<br>When selecciona guardar<br>Then sistema almacena cliente | Epic-01 |
| TS-01.3 | Validación backend de órdenes | Implementar validaciones de formato, peso, costos y campos obligatorios en API interna. | Given payload<br>When se envía<br>Then backend valida esquema y reglas | Epic-01 |
| Epic-02 | Tracking Unificado | Como usuario, quiero visualizar el estado de mi envío. | – | – |
| US-02.1 | Ver estado del envío | Consultar timeline de estados. | Given código válido<br>When consulta<br>Then timeline visible | Epic-02 |
| US-02.2 | Consulta pública | Cliente final consulta estado sin autenticación. | Given código<br>When lo ingresa<br>Then se muestra estado | Epic-02 |
| TS-02.3 | Infraestructura para tracking | Crear microservicio de tracking con base de datos optimizada. | Given microservicio<br>When recibe consulta<br>Then responde en <200ms | Epic-02 |
| Epic-03 | Cotización | Como emprendedor, quiero comparar tarifas. | – | – |
| US-03.1 | Cotizador | Ingreso peso/destino y veo tarifas. | Given datos<br>When consulta<br>Then muestra tarifas | Epic-03 |
| US-03.2 | Selección de courier | Elegir courier sugerido. | Given lista<br>When selecciona<br>Then se asigna courier | Epic-03 |
| TS-03.3 | Integración con APIs de couriers | Conectar con APIs externas para obtener tarifas y tiempos. | Given request<br>When se consulta<br>Then obtiene datos reales | Epic-03 |
| Epic-04 | Notificaciones | Como usuario, quiero recibir alertas. | – | – |
| US-04.1 | Notificación de retraso | Administrador recibe alertas. | Given retraso<br>When detectado<br>Then envía alerta | Epic-04 |
| US-04.2 | Confirmación de entrega | Cliente recibe confirmación. | Given entrega<br>When se actualiza<br>Then se notifica | Epic-04 |
| TS-04.3 | Motor de notificaciones | Crear un servicio para email y WhatsApp. | Given evento<br>When se dispara<br>Then se envía notificación | Epic-04 |
| Epic-05 | Reportes | Como administrador, quiero reportes. | – | – |
| US-05.1 | Reportes de desempeño | Generar reportes descargables. | Given fechas<br>When consulta<br>Then genera reporte | Epic-05 |
| US-05.2 | Exportación | Exportar en CSV/PDF. | Given reporte<br>When selecciona formato<br>Then descarga archivo | Epic-05 |
| TS-05.3 | Motor de generación de PDF | Implementar generador PDF server-side. | Given datos<br>When exporta<br>Then genera PDF ligero | Epic-05 |
| Epic-06 | Landing Page | Como visitante, quiero ver información de Sendify. | – | – |
| US-06.1 | Información de la propuesta | Ver beneficios. | Given visitante<br>When accede<br>Then visualiza info | Epic-06 |
| US-06.2 | Registro inicial | Registro desde la landing. | Given formulario<br>When lo completa<br>Then crea cuenta | Epic-06 |
| TS-06.3 | Optimización SEO | Implementar SEO técnico para aumentar captación. | Given página<br>When indexada<br>Then mejora ranking | Epic-06 |
| Epic-07 | Autenticación | Como usuario, quiero ingresar a mi cuenta. | – | – |
| US-07.1 | Inicio de sesión | Login seguro. | Given credenciales<br>When válidas<br>Then accede | Epic-07 |
| US-07.2 | Recuperación de contraseña | Recuperar acceso. | Given usuario<br>When solicita<br>Then recibe enlace | Epic-07 |
| TS-07.3 | Autenticación JWT/Session | Implementar seguridad backend. | Given login<br>When autentica<br>Then genera token seguro | Epic-07 |
| Epic-08 | Automatización | Como usuario, quiero automatizar acciones. | – | – |
| US-08.1 | Etiquetas automáticas | Generar etiquetas PDF. | Given envío<br>When confirma<br>Then genera etiqueta | Epic-08 |
| US-08.2 | Actualización automática | Estados se actualizan solos. | Given envío<br>When hay cambio<br>Then se refleja | Epic-08 |
| TS-08.3 | Cron Jobs automáticos | Crear tareas periódicas para actualización de estados. | Given cron<br>When ejecuta<br>Then sincroniza estados | Epic-08 |
| Epic-09 | Pagos | Como usuario, quiero pagar envíos. | – | – |
| US-09.1 | Pago por envío | Pagar con tarjeta o billetera. | Given envío<br>When paga<br>Then procesa transacción | Epic-09 |
| US-09.2 | Facturación automática | Recibir factura automática. | Given pago<br>When confirma<br>Then envía factura PDF | Epic-09 |
| TS-09.3 | Integración con pasarela | Integración Stripe/NIUBiz. | Given transacción<br>When procesa<br>Then retorna estado | Epic-09 |
| Epic-10 | Soporte | Como usuario, quiero soporte rápido. | – | – |
| US-10.1 | Chat de soporte | Enviar consultas. | Given usuario<br>When abre chat<br>Then puede chatear | Epic-10 |
| US-10.2 | Base de conocimientos | Consultar artículos. | Given visitante<br>When accede<br>Then lee FAQs | Epic-10 |
| TS-10.3 | Integración chatbot IA | IA básica para respuestas automáticas. | Given pregunta<br>When IA responde<br>Then reduce tickets | Epic-10 |
| Epic-11 | Dashboard | Como admin, quiero ver métricas. | – | – |
| US-11.1 | Ver KPIs | Ver estadísticas. | Given admin<br>When accede<br>Then ve KPIs | Epic-11 |
| US-11.2 | Panel de incidencias | Ver incidencias. | Given datos<br>When accede<br>Then visualiza panel | Epic-11 |
| TS-11.3 | Motor analítico | Agregar agregaciones y cálculos backend. | Given datos<br>When consulta<br>Then retorna métricas | Epic-11 |
| Epic-12 | Devoluciones | Como usuario, quiero gestionar devoluciones. | – | – |
| US-12.1 | Registrar devolución | Iniciar solicitud. | Given entrega<br>When solicita<br>Then crea RMA | Epic-12 |
| US-12.2 | Tracking devolución | Ver estado de devolución. | Given RMA<br>When consulta<br>Then muestra timeline | Epic-12 |
| TS-12.3 | Sistema de RMA | Crear módulo técnico para devoluciones. | Given request<br>When procesa<br>Then registra y gestiona | Epic-12 |


## 3.3. Impact Mapping

<img width="500" height="512" alt="user 1" src="https://github.com/user-attachments/assets/743854d6-1c1d-4c27-98ad-893d663c7371" />

## 3.4. Product Backlog

| **ID** | **Story Title** | **Tipo** | **Prioridad** | **Story Points** |
|--------|----------------|----------|---------------|------------------|
| US-01.1 | Crear envío | Funcional | Alta | 8 |
| US-01.2 | Guardar clientes frecuentes | Funcional | Media | 5 |
| TS-01.3 | Validación backend de órdenes | Técnica | Alta | 5 |
| US-02.1 | Ver estado del envío | Funcional | Alta | 8 |
| US-02.2 | Consulta pública de tracking | Funcional | Alta | 5 |
| TS-02.3 | Infraestructura de tracking | Técnica | Alta | 8 |
| US-03.1 | Cotizador | Funcional | Alta | 8 |
| US-03.2 | Selección de courier | Funcional | Media | 5 |
| TS-03.3 | Integración APIs de couriers | Técnica | Alta | 13 |
| US-04.1 | Notificación de retraso | Funcional | Alta | 5 |
| US-04.2 | Confirmación de entrega | Funcional | Alta | 3 |
| TS-04.3 | Motor de notificaciones | Técnica | Alta | 8 |
| US-05.1 | Reportes de desempeño | Funcional | Media | 8 |
| US-05.2 | Exportación | Funcional | Media | 5 |
| TS-05.3 | Generación PDF backend | Técnica | Media | 5 |
| US-06.1 | Información de la propuesta | Funcional | Baja | 3 |
| US-06.2 | Registro inicial | Funcional | Alta | 5 |
| TS-06.3 | SEO técnico | Técnica | Baja | 3 |
| US-07.1 | Inicio de sesión | Funcional | Alta | 5 |
| US-07.2 | Recuperación | Funcional | Media | 3 |
| TS-07.3 | Autenticación segura | Técnica | Alta | 8 |
| US-08.1 | Etiquetas PDF | Funcional | Media | 8 |
| US-08.2 | Auto-actualización | Funcional | Alta | 5 |
| TS-08.3 | Cron Jobs | Técnica | Alta | 5 |
| US-09.1 | Pago por envío | Funcional | Alta | 8 |
| US-09.2 | Facturación automática | Funcional | Alta | 5 |
| TS-09.3 | Integración pasarela | Técnica | Alta | 13 |
| US-10.1 | Chat de soporte | Funcional | Media | 5 |
| US-10.2 | Base de conocimiento | Funcional | Baja | 3 |
| TS-10.3 | Chatbot IA | Técnica | Media | 8 |
| US-11.1 | KPIs | Funcional | Media | 8 |
| US-11.2 | Panel incidencias | Funcional | Media | 5 |
| TS-11.3 | Motor analítico | Técnica | Alta | 13 |
| US-12.1 | Registrar devolución | Funcional | Media | 5 |
| US-12.2 | Tracking de devolución | Funcional | Media | 5 |
| TS-12.3 | Sistema RMA | Técnica | Alta | 8 |
