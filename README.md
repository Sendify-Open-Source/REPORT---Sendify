## Capítulo 3: Requirements Specification

## 3.1. To - Be Scenario Mapping

<img width="302" height="512" alt="user 1" src="https://github.com/user-attachments/assets/028b6c58-4166-4c14-98b0-0e675a9ed874" />

## 3.2. User Stories

| **Epic / Story ID** | **Título** | **Descripción** | **Criterios de Aceptación** | **Relacionado con (Epic ID)** |
|--------|---------|-------------|--------|--------|
| Epic-01 | Gestión de Envíos | Como administrador logístico, quiero registrar y gestionar envíos en un solo panel para reducir tiempos de operación. | –   | –   |
| US-01.1 | Crear envío | Como administrador logístico, quiero crear una orden de envío con datos de remitente, destinatario, dirección, peso y costo para centralizar la gestión. | Given un usuario autenticado<br><br>When completa los datos requeridos y confirma<br><br>Then el sistema guarda la orden y genera un código único | Epic-01 |
| US-01.2 | Guardar clientes frecuentes | Como administrador logístico, quiero guardar clientes y direcciones frecuentes para agilizar la creación de envíos. | Given un administrador que ha creado un envío<br><br>When selecciona guardar los datos de cliente<br><br>Then el sistema almacena los datos en una lista reutilizable | Epic-01 |
| Epic-02 | Tracking Unificado | Como usuario, quiero visualizar en un timeline claro el estado del envío para dar confianza al cliente final. | –   | –   |
| US-02.1 | Ver estado del envío | Como administrador logístico, quiero consultar el estado de cada envío en un timeline estandarizado. | Given un envío con un código válido<br><br>When el usuario consulta el código<br><br>Then el sistema muestra estados: registrado → en tránsito → en reparto → entregado | Epic-02 |
| US-02.2 | Consulta pública de tracking | Como consumidor final, quiero ingresar el código en un portal público para conocer el estado de mi pedido. | Given un cliente con código de envío<br><br>When lo introduce en el buscador<br><br>Then el sistema devuelve el estado actual sin requerir autenticación | Epic-02 |
| Epic-03 | Cotización de Tarifas | Como emprendedor, quiero comparar costos de envío entre couriers para elegir la mejor opción. | –   | –   |
| US-03.1 | Cotizador de tarifas | Como emprendedor, quiero ingresar peso y destino para cotizar tarifas disponibles. | Given un usuario autenticado<br><br>When ingresa peso y destino<br><br>Then el sistema muestra tarifas y tiempos por courier | Epic-03 |
| US-03.2 | Selección de courier | Como administrador, quiero elegir entre diferentes couriers sugeridos para optimizar costo/tiempo. | Given un listado de opciones de courier<br><br>When el usuario selecciona uno<br><br>Then el sistema asocia el envío con ese transportista | Epic-03 |
| Epic-04 | Notificaciones | Como usuario, quiero recibir alertas automáticas para conocer retrasos o entregas. | –   | –   |
| US-04.1 | Notificación de retraso | Como administrador logístico, quiero recibir alertas de retraso para reaccionar a tiempo. | Given un envío con retraso<br><br>When el sistema detecta la condición<br><br>Then se envía una alerta automática al administrador | Epic-04 |
| US-04.2 | Confirmación de entrega | Como cliente final, quiero recibir notificación cuando mi pedido haya sido entregado. | Given un envío marcado como entregado<br><br>When se actualiza el estado<br><br>Then el sistema notifica al cliente por el canal registrado (email/WhatsApp) | Epic-04 |
| Epic-05 | Reportes y Analítica | Como administrador, quiero obtener reportes de costos y tiempos para mejorar decisiones. | –   | –   |
| US-05.1 | Reportes de desempeño | Como administrador, quiero generar reportes de tiempos de entrega y costos consolidados. | Given un administrador autenticado<br><br>When selecciona rango de fechas<br><br>Then el sistema genera un reporte exportable en CSV o PDF | Epic-05 |
| US-05.2 | Exportación de reportes | Como administrador, quiero exportar reportes en distintos formatos para compartir con mi equipo. | Given un reporte generado<br><br>When el usuario selecciona formato CSV o PDF<br><br>Then el sistema descarga el archivo en el formato elegido | Epic-05 |
| Epic-06 | Landing Page | Como visitante, quiero conocer la propuesta de Sendify y planes disponibles para decidir registrarme. | –   | –   |
| US-06.1 | Información de la propuesta | Como visitante, quiero ver beneficios de Sendify para entender el valor de la plataforma. | Given un visitante<br><br>When accede a la landing<br><br>Then visualiza misión, visión y propuesta de valor | Epic-06 |
| US-06.2 | Registro inicial | Como visitante, quiero registrarme desde la landing page para comenzar a usar Sendify. | Given un visitante en la landing<br><br>When completa el formulario de registro<br><br>Then el sistema crea una cuenta en el plan Free | Epic-06 |
| Epic-07 | API RESTful | Como developer, quiero exponer endpoints seguros para que el sistema interactúe con terceros. | –   | –   |
| TS-07.1 | Endpoint de creación de envíos | Como developer, quiero un endpoint POST para registrar envíos con validación de datos. | Given un request POST con JSON válido<br><br>When contiene remitente, destinatario, dirección y peso<br><br>Then el sistema devuelve un código de envío y status 201 | Epic-07 |
| TS-07.2 | Endpoint de tracking | Como developer, quiero un endpoint GET para consultar estados por código de envío. | Given un request<br><br>GET con código válido<br><br>When el sistema recibe la consulta}<br><br>Then devuelve JSON con el estado actual y timeline histórico | Epic-07 |
| TS-07.3 | Endpoint de tarifas | Como developer, quiero un endpoint GET que devuelva tarifas según peso y destino. | Given un request<br><br>GET con peso y destino<br><br>When el sistema procesa<br><br>Then responde JSON con tarifas y tiempos por courier | Epic-07 |
| Epic-08 | Autenticación y Seguridad | Como usuario, quiero ingresar de forma segura para proteger mis datos y operaciones. | – | – |
| US-08.1 | Inicio de sesión seguro | Como usuario registrado, quiero iniciar sesión con correo y contraseña para acceder a mis envíos. | Given un usuario registrado<br><br>When ingresa credenciales válidas<br><br>Then el sistema permite el acceso y genera un token de sesión | Epic-08 |
| US-08.2 | Recuperación de contraseña | Como usuario, quiero restablecer mi contraseña mediante email para no perder el acceso. | Given un usuario que olvidó su contraseña<br><br>When solicita recuperar el acceso<br><br>Then el sistema envía un enlace temporal para generar una nueva contraseña | Epic-08 |
| US-08.3 | Autenticación 2FA | Como administrador, quiero activar 2FA para mayor seguridad. | Given un administrador con 2FA habilitado<br><br>When inicia sesión<br><br>Then el sistema solicita un código adicional enviado por email o SMS | Epic-08 |
| Epic-09 | Gestión de Usuarios y Roles | Como administrador, quiero controlar roles y permisos para evitar accesos no autorizados. | – | – |
| US-09.1 | Crear roles | Como superadministrador, quiero crear roles personalizados con permisos específicos. | Given un superadmin<br><br>When define un nuevo rol<br><br>Then el sistema lo registra con los permisos seleccionados | Epic-09 |
| US-09.2 | Asignación de roles | Como superadministrador, quiero asignar roles a usuarios para delimitar su acceso. | Given un usuario existente<br><br>When se le asigna un rol<br><br>Then el usuario obtiene los permisos establecidos | Epic-09 |
| Epic-10 | Automatización Operativa | Como administración logística, quiero automatizar procesos repetitivos para ahorrar tiempo. | – | – |
| US-10.1 | Generación automática de etiquetas | Como administrador, quiero generar etiquetas PDF automáticamente al crear un envío. | Given un envío creado<br><br>When se confirma<br><br>Then el sistema genera una etiqueta con QR/código de barras | Epic-10 |
| US-10.2 | Actualización automática del estado | Como administrador, quiero que los estados se actualicen automáticamente mediante API con couriers. | Given un envío asociado a un courier<br><br>When el courier actualiza el estado<br><br>Then el sistema sincroniza el estado en tiempo real | Epic-10 |
| Epic-11 | Integraciones con Couriers | Como empresa, quiero conectar con couriers externos para registrar envíos y obtener tarifas automáticamente. | – | – |
| US-11.1 | Integración con Courier A | Como administrador, quiero conectar Sendify con un courier mediante API. | Given credenciales API del courier<br><br>When se configura la integración<br><br>Then el sistema permite crear envíos mediante esa API | Epic-11 |
| US-11.2 | Webhooks de actualización | Como developer, quiero recibir webhooks de actualización de estado desde couriers. | Given un webhook registrado<br><br>When el courier envía un update<br><br>Then el sistema actualiza el estado del envío correspondiente | Epic-11 |
| Epic-12 | Pagos y Facturación | Como usuario, quiero pagar mis envíos dentro de la plataforma y obtener comprobantes. | – | – |
| US-12.1 | Pago por envío | Como usuario, quiero pagar un envío con tarjeta o transferencia. | Given un envío pendiente de pago<br><br>When selecciona método de pago<br><br>Then el sistema procesa el pago y marca el envío como pagado | Epic-12 |
| US-12.2 | Facturación automática | Como usuario, quiero recibir una factura en PDF tras completar el pago. | Given un pago confirmado<br><br>When se registra<br><br>Then el sistema envía la factura al correo registrado | Epic-12 |
| Epic-13 | Centro de Ayuda | Como usuario, quiero acceder a soporte para resolver problemas rápidamente. | – | – |
| US-13.1 | Chat de soporte | Como usuario, quiero escribir al chat de soporte para resolver dudas en tiempo real. | Given un usuario autenticado<br><br>When abre el chat<br><br>Then puede enviar consultas y recibir respuestas | Epic-13 |
| US-13.2 | Base de conocimientos | Como visitante, quiero consultar artículos y guías sin contactar soporte. | Given un visitante<br><br>When accede a la base de conocimientos<br><br>Then visualiza artículos y FAQs | Epic-13 |
| Epic-14 | Dashboard Operativo | Como administrador, quiero ver métricas clave para tomar decisiones informadas. | – | – |
| US-14.1 | KPIs en tiempo real | Como administrador, quiero KPIs de entregas, retrasos y envíos activos. | Given un admin autenticado<br><br>When accede al dashboard<br><br>Then visualiza métricas actualizadas | Epic-14 |
| US-14.2 | Panel de incidencias | Como administrador, quiero ver incidencias de envíos para gestionarlas. | Given una incidencia registrada<br><br>When accede al panel<br><br>Then visualiza detalle y estado actual | Epic-14 |
| Epic-15 | Gestión de Devoluciones (RMA) | Como administrador, quiero gestionar devoluciones completas del cliente. | – | – |
| US-15.1 | Registrar devolución | Como administrador, quiero registrar devoluciones con motivo y estado. | Given un envío entregado<br><br>When se inicia devolución<br><br>Then el sistema crea un RMA asociado | Epic-15 |
| US-15.2 | Seguimiento de devolución | Como usuario, quiero ver el estado de mi devolución igual que un envío. | Given un RMA creado<br><br>When el usuario consulta el código<br><br>Then el sistema muestra timeline del proceso | Epic-15 |


## 3.3. Impact Mapping

<img width="302" height="512" alt="user 1" src="https://github.com/user-attachments/assets/743854d6-1c1d-4c27-98ad-893d663c7371" />

## 3.4. Product Backlog

| **Órden** | **Story ID** | **Título** | **Descripción** | **Story Points** |
|--------|---------|-------------|--------|--------|
| 1   | US-01.1 | Crear envío | Como administrador logístico, quiero crear una orden de envío (remitente, destinatario, dirección, peso, costo) para centralizar la gestión. | 8   |
| 2   | US-01.2 | Guardar clientes frecuentes | Como administrador logístico, quiero guardar clientes y direcciones frecuentes para agilizar la creación de envíos. | 5   |
| 3   | US-02.1 | Ver estado del envío | Como administrador logístico, quiero consultar el estado de cada envío en un timeline estandarizado. | 5   |
| 4   | US-02.2 | Consulta pública de tracking | Como consumidor final, quiero ingresar el código en un portal público para conocer el estado de mi pedido. | 5   |
| 5   | US-03.1 | Cotizador de tarifas | Como emprendedor, quiero ingresar peso y destino para cotizar tarifas disponibles. | 5   |
| 6   | US-03.2 | Selección de courier | Como administrador, quiero elegir entre diferentes couriers sugeridos para optimizar costo/tiempo. | 5   |
| 7   | US-04.1 | Notificación de retraso | Como administrador logístico, quiero recibir alertas de retraso para reaccionar a tiempo. | 3   |
| 8   | US-04.2 | Confirmación de entrega | Como cliente final, quiero recibir notificación cuando mi pedido haya sido entregado. | 3   |
| 9   | US-05.1 | Reportes de desempeño | Como administrador, quiero generar reportes de tiempos de entrega y costos consolidados. | 5   |
| 10  | US-05.2 | Exportación de reportes | Como admin, quiero exportar reportes en CSV o PDF para compartir con mi equipo. | 3   |
| 11  | US-06.1 | Información de la propuesta | Como visitante, quiero ver beneficios de Sendify en la landing page para entender el valor de la plataforma. | 2   |
| 12  | US-06.2 | Registro inicial | Como visitante, quiero registrarme desde la landing page para comenzar a usar Sendify. | 3   |
| 13  | TS-07.1 | Endpoint de creación de envíos | Como developer, quiero un endpoint POST para registrar envíos con validación de datos. | 8   |
| 14  | TS-07.2 | Endpoint de tracking | Como developer, quiero un endpoint GET para consultar estados por código de envío. | 5   |
| 15  | TS-07.3 | Endpoint de tarifas | Como developer, quiero un endpoint GET que devuelva tarifas según peso y destino. | 5   |
| 16 | US-08.1 | Inicio de sesión seguro | Como usuario registrado, quiero iniciar sesión con credenciales válidas. | 3 |
| 17 | US-08.2 | Recuperación de contraseña | Como usuario, quiero recuperar mi contraseña mediante email. | 3 |
| 18 | US-08.3 | Autenticación 2FA | Como administrador, quiero mayor seguridad al iniciar sesión. | 5 |
| 19 | US-09.1 | Crear roles | Como superadmin, quiero crear roles personalizados. | 5 |
| 20 | US-09.2 | Asignación de roles | Como superadmin, quiero asignar roles a usuarios. | 3 |
| 21 | US-10.1 | Generación automática de etiquetas | Como admin, quiero generar etiquetas con QR automáticamente. | 5 |
| 22 | US-10.2 | Actualización automática del estado | Como admin, quiero sincronización automática por API. | 8 |
| 23 | US-11.1 | Integración con Courier A | Integrar Sendify con un courier vía API. | 8 |
| 24 | US-11.2 | Webhooks de actualización | Recibir actualizaciones desde couriers. | 5 |
| 25 | US-12.1 | Pago por envío | Como usuario, quiero pagar el envío dentro de la plataforma. | 8 |
| 26 | US-12.2 | Facturación automática | Generar factura PDF tras el pago. | 5 |
| 27 | US-13.1 | Chat de soporte | Acceder a soporte vía chat. | 8 |
| 28 | US-13.2 | Base de conocimientos | Consultar artículos y guías. | 3 |
| 29 | US-14.1 | KPIs en tiempo real | Dashboard con métricas operativas. | 5 |
| 30 | US-14.2 | Panel de incidencias | Gestionar incidencias de envíos. | 5 |
| 31 | US-15.1 | Registrar devolución | Registrar RMA. | 5 |
| 32 | US-15.2 | Seguimiento de devolución | Tracking de devolución para el usuario. | 5 |
##
