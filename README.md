## Capítulo 3: Requirements Specification

## 3.1. To - Be Scenario Mapping

<img width="302" height="512" alt="user 1" src="https://github.com/user-attachments/assets/028b6c58-4166-4c14-98b0-0e675a9ed874" />

## 3.2. User Stories

| **Epic / Story ID** | **Título** | **Descripción** | **Criterios de Aceptación** | **Relacionado con (Epic ID)** |
|--------|---------|-------------|--------|--------|
| Epic-01 | Gestión de Envíos | Como administrador logístico, quiero gestionar envíos para reducir tiempos de operación. | – | – |
| US-01.1 | Crear envío | Como administrador logístico, quiero crear una orden de envío con datos de remitente, destinatario, dirección, peso y costo para centralizar la gestión. | Given un usuario autenticado<br><br>When completa los datos requeridos y confirma<br><br>Then el sistema guarda la orden y genera un código único | Epic-01 |
| US-01.2 | Guardar clientes frecuentes | Como administrador logístico, quiero guardar clientes y direcciones frecuentes para agilizar la creación de envíos. | Given un envío creado<br><br>When selecciona guardar los datos del cliente<br><br>Then el sistema almacena la información para reutilizarla | Epic-01 |
| Epic-02 | Tracking Unificado | Como usuario, quiero visualizar el estado del envío para dar confianza al cliente final. | – | – |
| US-02.1 | Ver estado del envío | Como administrador logístico, quiero consultar el estado de cada envío en un timeline estandarizado. | Given un envío con código válido<br><br>When el usuario realiza la consulta<br><br>Then el sistema muestra estado y timeline | Epic-02 |
| US-02.2 | Consulta pública | Como consumidor final, quiero ingresar el código del envío para conocer su estado sin iniciar sesión. | Given un código<br><br>When lo ingresa en el buscador<br><br>Then el sistema muestra el estado actual | Epic-02 |
| Epic-03 | Cotización | Como emprendedor, quiero comparar costos de envíos para elegir la mejor opción. | – | – |
| US-03.1 | Cotizador | Como emprendedor, quiero ingresar peso y destino para cotizar tarifas disponibles. | Given un usuario<br><br>When ingresa peso y destino<br><br>Then el sistema muestra tarifas y tiempos | Epic-03 |
| US-03.2 | Selección de courier | Como usuario, quiero elegir entre diferentes couriers sugeridos para optimizar costo/tiempo. | Given un listado de opciones<br><br>When selecciona un courier<br><br>Then el sistema asocia el envío al seleccionado | Epic-03 |
| Epic-04 | Notificaciones | Como usuario, quiero recibir alertas automáticas del estado de mis envíos. | – | – |
| US-04.1 | Notificación de retraso | Como administrador, quiero recibir alertas cuando un envío se retrase. | Given un envío retrasado<br><br>When se detecta<br><br>Then el sistema envía una notificación automática | Epic-04 |
| US-04.2 | Confirmación de entrega | Como cliente final, quiero recibir una notificación cuando mi envío haya sido entregado. | Given un envío entregado<br><br>When el estado cambia<br><br>Then se envía notificación al cliente | Epic-04 |
| Epic-05 | Reportes | Como administrador, quiero obtener reportes para mejorar decisiones. | – | – |
| US-05.1 | Reportes de desempeño | Como administrador, quiero generar reportes de tiempos de entrega y costos. | Given un administrador autenticado<br><br>When selecciona rango de fechas<br><br>Then el sistema genera un reporte descargable | Epic-05 |
| US-05.2 | Exportación de reportes | Como administrador, quiero exportar los reportes generados para compartirlos. | Given un reporte<br><br>When selecciona formato<br><br>Then el sistema descarga el archivo | Epic-05 |
| Epic-06 | Landing Page | Como visitante, quiero conocer Sendify y registrarme fácilmente. | – | – |
| US-06.1 | Información de la propuesta | Como visitante, quiero ver beneficios de Sendify para entender el valor de la plataforma. | Given un visitante<br><br>When accede a la landing<br><br>Then visualiza misión, visión y propuesta | Epic-06 |
| US-06.2 | Registro inicial | Como visitante, quiero registrarme desde la landing page para comenzar a usar Sendify. | Given un visitante<br><br>When completa el formulario<br><br>Then el sistema crea una cuenta en el plan Free | Epic-06 |
| Epic-07 | Autenticación | Como usuario, quiero ingresar de forma segura a mi cuenta. | – | – |
| US-07.1 | Inicio de sesión | Como usuario, quiero iniciar sesión con mi correo y contraseña para acceder a mis envíos. | Given un usuario registrado<br><br>When ingresa sus credenciales<br><br>Then el sistema le permite ingresar | Epic-07 |
| US-07.2 | Recuperación de contraseña | Como usuario, quiero recuperar mi contraseña si la olvido. | Given un usuario<br><br>When solicita recuperación<br><br>Then el sistema envía un enlace temporal | Epic-07 |
| Epic-08 | Automatización | Como usuario, quiero automatizar acciones para ahorrar tiempo. | – | – |
| US-08.1 | Etiquetas automáticas | Como administrador, quiero generar etiquetas PDF automáticamente al crear un envío. | Given un envío creado<br><br>When se confirma<br><br>Then el sistema genera la etiqueta | Epic-08 |
| US-08.2 | Actualización automática | Como usuario, quiero que el estado de mis pedidos se actualice automáticamente. | Given un envío<br><br>When hay un cambio<br><br>Then el sistema lo refleja sin intervención manual | Epic-08 |
| Epic-09 | Pagos | Como usuario, quiero pagar mis envíos dentro de la plataforma. | – | – |
| US-09.1 | Pago por envío | Como usuario, quiero pagar con tarjeta o billetera digital. | Given un envío pendiente<br><br>When selecciona un método de pago<br><br>Then el sistema procesa la transacción | Epic-09 |
| US-09.2 | Facturación automática | Como usuario, quiero recibir mi factura después de pagar. | Given un pago<br><br>When se completa<br><br>Then el sistema envía la factura PDF | Epic-09 |
| Epic-10 | Soporte | Como usuario, quiero acceder a soporte para resolver problemas rápidamente. | – | – |
| US-10.1 | Chat de soporte | Como usuario, quiero enviar consultas al chat de soporte. | Given un usuario<br><br>When abre el chat<br><br>Then puede escribir y recibir respuestas | Epic-10 |
| US-10.2 | Base de conocimientos | Como visitante, quiero consultar artículos y guías sin contactar soporte. | Given un visitante<br><br>When accede a la base de conocimientos<br><br>Then puede leer artículos, tutoriales y FAQs | Epic-10 |
| Epic-11 | Dashboard | Como administrador, quiero ver métricas clave del negocio. | – | – |
| US-11.1 | Ver KPIs | Como administrador, quiero visualizar KPIs actualizados. | Given un admin<br><br>When ingresa al dashboard<br><br>Then ve métricas de entregas, tiempos y retrasos | Epic-11 |
| US-11.2 | Panel de incidencias | Como admin, quiero ver incidencias para gestionarlas. | Given incidencias registradas<br><br>When ingresa al panel<br><br>Then ve detalle, severidad y estado | Epic-11 |
| Epic-12 | Devoluciones | Como usuario, quiero gestionar devoluciones fácilmente. | – | – |
| US-12.1 | Registrar devolución | Como usuario, quiero iniciar una solicitud de devolución. | Given un envío entregado<br><br>When solicita devolución<br><br>Then el sistema registra un RMA | Epic-12 |
| US-12.2 | Tracking de devolución | Como usuario, quiero ver el estado de mi devolución. | Given una devolución<br><br>When consulta el código<br><br>Then el sistema muestra timeline del proceso | Epic-12 |



## 3.3. Impact Mapping

<img width="302" height="512" alt="user 1" src="https://github.com/user-attachments/assets/743854d6-1c1d-4c27-98ad-893d663c7371" />

## 3.4. Product Backlog

| **ID**  | **User Story**                      | **Prioridad** | **Estimación (Story Points)** |
| ------- | ----------------------------------- | ------------- | ----------------------------- |
| US-01.1 | Crear envío                         | Alta          | 8                             |
| US-01.2 | Guardar clientes frecuentes         | Media         | 5                             |
| US-02.1 | Ver estado del envío                | Alta          | 8                             |
| US-02.2 | Consulta pública de tracking        | Alta          | 5                             |
| US-03.1 | Cotizador de tarifas                | Alta          | 8                             |
| US-03.2 | Selección de courier                | Media         | 5                             |
| US-04.1 | Notificación de retraso             | Alta          | 5                             |
| US-04.2 | Confirmación de entrega             | Alta          | 3                             |
| US-05.1 | Reportes de desempeño               | Media         | 8                             |
| US-05.2 | Exportación de reportes             | Media         | 5                             |
| US-06.1 | Información de la propuesta         | Media         | 3                             |
| US-06.2 | Registro inicial                    | Alta          | 5                             |
| US-07.1 | Inicio de sesión                    | Alta          | 5                             |
| US-07.2 | Recuperación de contraseña          | Media         | 3                             |
| US-08.1 | Etiquetas automáticas               | Media         | 8                             |
| US-08.2 | Actualización automática del estado | Alta          | 5                             |
| US-09.1 | Pago por envío                      | Alta          | 8                             |
| US-09.2 | Facturación automática              | Alta          | 5                             |
| US-10.1 | Chat de soporte                     | Media         | 5                             |
| US-10.2 | Base de conocimientos               | Baja          | 3                             |
| US-11.1 | Ver KPIs                            | Media         | 8                             |
| US-11.2 | Panel de incidencias                | Media         | 5                             |
| US-12.1 | Registrar devolución                | Media         | 5                             |
| US-12.2 | Tracking de devolución              | Media         | 5                             |

##
