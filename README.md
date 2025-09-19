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

##
