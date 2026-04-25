# Capítulo III: Requirements Specification

## 3.1. User Stories

| EPIC ID | Titulo | Descripcion |
| :--- | :--- | :--- |
| EP01 | Gestión y Monitoreo de Datos Neonatales | Como padre o neonatólogo, quiero registrar y consultar información del recién nacido para llevar un control detallado de su evolución y seguimiento clínico. |
| EP02 | Alertas Inteligentes y Notificaciones | Como padre o neonatólogo, quiero recibir alertas y notificaciones sobre valores críticos del bebé para reaccionar oportunamente y priorizar la atención médica. |
| EP03 | Análisis y Reportes | Como padre o neonatólogo, quiero visualizar reportes y resúmenes del estado del bebé para comprender su evolución y apoyar la toma de decisiones. |
| EP04 | Gestión de Cuenta | Como padre o neonatólogo, quiero gestionar mi cuenta en la plataforma para acceder de manera segura a las funcionalidades del sistema. |
| EP05 | Captación y Presentación de la Plataforma | Como visitante, quiero conocer la plataforma y sus beneficios para evaluar su utilidad y decidir si registrarme. |
| EP06 | Documentación Técnica y Marco Estratégico del Proyecto | Como developer, quiero definir y documentar el modelo de negocio, requisitos y diseño del sistema para guiar el desarrollo del producto de manera estructurada. |

- User Stories

| STORY ID | Titulo | Descripcion | Criterios de aceptacion | EPIC ID |
| :--- | :--- | :--- | :--- | :--- |
| HU01 | Registrar parámetros diarios del bebé | Como padre, quiero registrar los parámetros diarios del bebé para llevar un control preciso de su evolución. | **Escenario 1:** Registro correcto (almacena datos con fecha/hora). <br>**Escenario 2:** Datos incompletos (el sistema rechaza el registro). | EP01 |
| HU02 | Consultar historial completo del recién nacido | Como neonatólogo, quiero consultar el historial completo de registros de un recién nacido. | **Escenario 1:** Muestra datos cronológicamente. <br>**Escenario 2:** Filtros por parámetro o rango de fechas. | EP01 |
| HU03 | Recibir alertas por parámetros anormales | Como padre, quiero recibir alertas automáticas cuando un parámetro se salga de los rangos normales. | **Escenario 1:** Generación de alerta. <br>**Escenario 2:** Visualización con prioridad. <br>**Escenario 3:** No alerta si el dato es normal. | EP02 |
| HU04 | Ver reportes gráficos del bebé | Como padre, quiero visualizar reportes gráficos de la evolución del bebé. | **Escenario 1:** Generación de gráficos (temp, peso, etc). <br>**Escenario 2:** Exportación de reporte. <br>**Escenario 3:** Sin datos suficientes. | EP03 |
| HU05 | Recibir notificaciones de alertas críticas | Como padre, quiero recibir notificaciones push o correo ante alertas críticas. | **Escenario 1:** Envío en <60 seg. <br>**Escenario 2:** Acceso directo al detalle desde la notificación. | EP02 |
| HU06 | Generar reportes médicos del bebé | Como neonatólogo, quiero generar reportes detallados para la consulta médica. | **Escenario 1:** Documento con tendencias y alertas. <br>**Escenario 2:** Envío por correo o guardado. | EP03 |
| HU07 | Registrarse en la plataforma | Como padre o neonatólogo, quiero registrarme en la plataforma. | **Escenario 1:** Registro válido. <br>**Escenario 2:** Correo repetido (error). <br>**Escenario 3:** Datos incompletos (error). | EP04 |
| HU08 | Iniciar sesión en la plataforma | Como usuario registrado, quiero iniciar sesión en la plataforma. | **Escenario 1:** Acceso válido. <br>**Escenario 2:** Credenciales incorrectas (denegado). <br>**Escenario 3:** Bloqueo temporal por intentos fallidos. | EP04 |
| HU09 | Visualizar beneficios de la plataforma | Como visitante, quiero conocer los beneficios principales de SIRAN. | **Escenario 1:** Vista de beneficios. <br>**Escenario 2:** Opción de inicio de registro. | EP05 |
| HU10 | Cerrar sesión en la plataforma | Como usuario autenticado, quiero cerrar mi sesión. | **Escenario 1:** Finalización de sesión. <br>**Escenario 2:** Protección de datos tras cierre. | EP04 |
| HU11 | Visualizar testimonios y casos de uso | Como visitante, quiero ver testimonios reales para generar confianza. | **Escenario 1:** Testimonios segmentados (padres/médicos). <br>**Escenario 2:** Identificación clara de segmentos. | EP05 |
| HU12 | Ver resumen del estado del bebé | Como padre, quiero ver un resumen diario o semanal. | **Escenario 1:** Promedios y destacados. <br>**Escenario 2:** Inclusión de alertas importantes. | EP05 |
| HU13 | Visualizar planes disponibles | Como visitante, quiero visualizar los planes de suscripción. | **Escenario 1:** Visualización de planes y precios. <br>**Escenario 2:** Selección de plan. <br>**Escenario 3:** Acceso a pago. | EP05 |
| HU14 | Recibir alertas de pacientes con valores críticos | Como neonatólogo, quiero recibir alertas de mis pacientes. | **Escenario 1:** Notificación por valor crítico. <br>**Escenario 2:** Comentario tras revisión de alerta. | EP02 |
| HU15 | Registrar observaciones y síntomas | Como usuario, quiero registrar síntomas u observaciones cualitativas. | **Escenario 1:** Guardado de observación. <br>**Escenario 2:** Visualización histórica de observaciones. | EP01 |
| HU16 | Revisar y marcar observaciones del bebé | Como neonatólogo, quiero revisar y marcar observaciones. | **Escenario 1:** Ordenamiento por filtro. <br>**Escenario 2:** Cambio de estado (revisada). | EP01 |
| HU17 | Visualizar interfaz adaptativa | Como visitante, quiero una interfaz que se adapte a dispositivos móviles. | **Escenario 1:** Navegación móvil (hamburguesa). <br>**Escenario 2:** Ajuste fluido al rotar pantalla. | EP05 |
| HU18 | Cambiar idioma de la plataforma | Como visitante extranjero, quiero cambiar el idioma. | **Escenario 1:** Traducción instantánea. <br>**Escenario 2:** Persistencia de idioma. | EP05 |
| HU19 | Navegación por anclas | Como visitante, quiero navegar por las secciones del menú. | **Escenario 1:** Desplazamiento suave. <br>**Escenario 2:** Redirección a inicio ante error. | EP05 |
| HU20 | Personalizar umbrales de alerta médica | Como neonatólogo, quiero ajustar rangos por paciente. | **Escenario 1:** Aplicación de nuevos límites. <br>**Escenario 2:** Validación de valores inconsistentes. | EP02 |

- Technical Stories

| STORY ID | Titulo | Descripcion | Criterios de aceptacion | EPIC ID |
| :--- | :--- | :--- | :--- | :--- |
| TS01 | API de registro de datos del bebé | Como Developer, quiero implementar un endpoint para registrar los datos del bebé para almacenar información clínica. | **Escenario 1:** Registro exitoso (POST válido, almacena y retorna confirmación). <br>**Escenario 2:** Datos inválidos (POST incompleto/incorrecto, retorna error). | EP01 |
| TS02 | API de consulta de historial del bebé | Como Developer, quiero implementar un endpoint para obtener el historial de registros del bebé. | **Escenario 1:** Consulta exitosa (GET válido, retorna registros ordenados). <br>**Escenario 2:** Bebé no encontrado (GET inexistente, retorna error). | EP01 |
| TS03 | Lógica de generación de alertas | Como Developer, quiero implementar la lógica de alertas basada en parámetros para detectar valores fuera de rango. | **Escenario 1:** Generación de alerta (valor excede umbral). <br>**Escenario 2:** Valor dentro de rango (no genera alerta). | EP02 |
| TS04 | API de consulta de alertas generadas | Como Developer, quiero implementar un endpoint para consultar las alertas generadas. | **Escenario 1:** Consulta exitosa (retorna lista de alertas). <br>**Escenario 2:** Sin alertas (retorna lista vacía). | EP02 |
| TS05 | API de generación de reportes del bebé | Como Developer, quiero implementar un endpoint para generar reportes para el análisis de evolución. | **Escenario 1:** Generación exitosa (resumen de tendencias). <br>**Escenario 2:** Datos insuficientes (retorna error). | EP03 |
| TS06 | Definición de Modelo de Negocio y alcance | Como Developer quiero definir el modelo de negocio y alcance del proyecto SIRAN. | **Escenario 1:** Validación de Business/Customer Assumptions. <br>**Escenario 2:** Especificación de ingresos e indicadores. <br>**Escenario 3:** Alcance funcional y no funcional. | EP06 |
| TS07 | Análisis de Necesidades y Realidad del Usuario | Como Developer, quiero documentar las necesidades para tener claridad antes de diseñar la arquitectura. | **Escenario 1:** Documentación de 5W's, 2H's y Problem Statement. <br>**Escenario 2:** Necesidades específicas por segmento. | EP06 |
| TS08 | Especificación de Requisitos | Como Developer, quiero especificar los requisitos funcionales y no funcionales. | **Escenario 1:** User Stories con criterios de aceptación. <br>**Escenario 2:** Requisitos no funcionales (seguridad, rendimiento, etc). | EP06 |
| TS09 | Diseño de Producto | Como Developer, quiero diseñar la arquitectura y experiencia antes de la implementación. | **Escenario 1:** Documentación de arquitectura y componentes. <br>**Escenario 2:** Prototipos o wireframes. | EP06 |
| TS10 | Implementación, Validación y Deploy | Como Developer, quiero implementar, validar y desplegar el sistema. | **Escenario 1:** Implementación de funcionalidades según prioridades. <br>**Escenario 2:** Verificación mediante pruebas funcionales. | EP06 |
## 3.2. Impact Mapping

![impact-mapping.jpg](assets/impact-mapping.jpeg)

## 3.3. Product Backlog
El siguiente Product Backlog presenta la priorización de las User Stories del sistema SIRAN, organizadas en función del valor que aportan al negocio. Se incluyen las historias relacionadas con la Plataforma Web Informativa (Landing Page) para validar la propuesta de valor del producto y atraer usuarios desde etapas tempranas. Seguidamente se priorizan las funcionalidades clave del sistema relacionadas con el monitoreo del bebé, generación de alertas y análisis de datos. Finalmente, se consideran las historias asociadas a la gestión de cuentas, dado que no representan el mayor valor inicial para el usuario. 


| ID | Título | Estimación (Esfuerzo) |
| :--- | :--- | :---: |
| HU07 | Registrarse en la plataforma | 3 |
| HU08 | Iniciar sesión en la plataforma | 2 |
| HU01 | Registrar parámetros diarios del bebé | 5 |
| HU02 | Consultar historial completo del recién nacido | 3 |
| HU03 | Recibir alertas por parámetros anormales | 8 |
| HU14 | Recibir alertas de pacientes con valores críticos | 5 |
| HU05 | Recibir notificaciones de alertas críticas | 5 |
| HU04 | Ver reportes gráficos del bebé | 8 |
| HU06 | Generar reportes médicos del bebé | 5 |
| HU15 | Registrar observaciones y síntomas del bebé | 2 |
| HU16 | Revisar y marcar observaciones del bebé | 2 |
| HU12 | Ver resumen del estado del bebé | 3 |
| HU20 | Personalizar umbrales de alerta médica | 5 |
| HU10 | Cerrar sesión en la plataforma | 1 |
| HU09 | Visualizar beneficios de la plataforma (Landing) | 2 |
| HU11 | Visualizar testimonios y casos de uso | 2 |
| HU13 | Visualizar planes disponibles de la plataforma | 3 |
| HU17 | Visualizar interfaz adaptativa (Mobile) | 3 |
| HU18 | Cambiar idioma de la plataforma | 2 |
| HU19 | Navegación por anclas | 1 |

<img src="assets/Product-Backlog.png">

Para más detalle, ver el anexo 4.



