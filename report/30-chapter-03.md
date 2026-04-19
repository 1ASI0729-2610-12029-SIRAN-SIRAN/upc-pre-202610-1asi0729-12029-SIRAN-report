# Capítulo III: Requirements Specification

## 3.1. User Stories

- Epic

```{=latex}
\newpage
\begin{longtable}{|p{3cm}|p{3cm}|p{3cm}|}
\hline
EPIC ID
& 
Titulo 
& 
Descripcion\\
\hline
EP01
& 
Gestión y Monitoreo de Datos Neonatales  
& 
Como padre o neonatólogo, quiero registrar y consultar información del recién nacido para llevar un control detallado de su evolución y seguimiento clínico.\\
\hline
EP02
& 
Alertas Inteligentes y Notificaciones 
& 
Como padre o neonatólogo, quiero recibir alertas y notificaciones sobre valores críticos del bebé para reaccionar oportunamente y priorizar la atención médica.\\
\hline
EP03
& 
Análisis y Reportes 
& 
Como padre o neonatólogo, quiero visualizar reportes y resúmenes del estado del bebé para comprender su evolución y apoyar la toma de decisiones.\\
\hline
EP04
& 
Gestión de Cuenta 
& 
Como padre o neonatólogo, quiero gestionar mi cuenta en la plataforma para acceder de manera segura a las funcionalidades del sistema.\\
\hline
EP05
& 
Captación y Presentación de la Plataforma 
& 
Como visitante, quiero conocer la plataforma y sus beneficios para evaluar su utilidad y decidir si registrarme.\\
\hline
EP06
& 
Documentación Técnica y Marco Estratégico del Proyecto 
& 
Como developer, quiero definir y documentar el modelo de negocio, requisitos y diseño del sistema para guiar el desarrollo del producto de manera estructurada.\\
\hline
\end{longtable}
```

- User Stories

```{=latex}
\begin{longtable}{|p{3cm}|p{3cm}|p{3cm}|p{3cm}|p{3cm}|}
\hline
STORY ID
& 
Titulo 
& 
Descripcion 
& 
Criterios de aceptacion 
& 
EPIC ID\\
\hline
HU01 
& 
Registrar parámetros diarios del bebé 
& 
Como padre, quiero registrar los parámetros diarios del bebé para llevar un control preciso de su evolución. 
& 
Escenario 1: Registro correcto \newline 
Given que el usuario tiene una sesión activa y un bebé registrado,  
When registra parámetros como temperatura, peso, alimentación, sueño, 
Then el sistema el sistema almacena los datos asociados a una fecha y hora.  
\newline
Escenario 2: Datos incompletos\newline
Given que el usuario intenta registrar un parámetro, When omite información obligatoria, Then el sistema rechaza el registro
&
EP01\\
\hline
HU02 
& 
Consultar historial completo del recién nacido 
& 
Como neonatólogo, quiero consultar el historial completo de registros de un recién nacido para tener una visión integral de su evolución. 
& 
Escenario 1:\newline
Given que el profesional tiene acceso autorizado al bebé,  
When solicita el historial de registros,  
Then el sistema muestra todos los datos cronológicamente.

Escenario 2:\newline
Given que existen registros de múltiples días,  
When el profesional filtra por parámetro o rango de fechas,  
Then el sistema devuelve solo los datos solicitados. 
& 
EP01\\
\hline
HU03 
& 
Recibir alertas por parámetros anormales del bebé 
& 
Como padre,quiero recibir alertas automáticas cuando un parámetro del bebé se salga de los rangos normales para reaccionar oportunamente. 
& 
Escenario 1:  Generación de alerta\newline
Given que se registró un valor de temperatura, peso o cualquier parámetro,  
When este supera los umbrales médicos definidos,  
Then el sistema genera una alerta asociada al registro.\newline  
\newline
Escenario 2:  Visualización de alerta\newline
Given que se genera una alerta,  
When el usuario accede al sistema,  
Then visualiza la alerta con nivel de prioridad y recomendación clara.\newline
\newline
Escenario 3: No generación de alerta\newline
Given que se registra un parámetro dentro de los rangos normales,
When el sistema valida el dato,
Then no se genera ninguna alerta.
& 
EP02\\
\hline
HU04
& 
Ver reportes gráficos del bebé 
& 
Como padre , quiero visualizar reportes gráficos de la evolución del bebé para entender mejor su progreso. 
& 
Escenario 1: Generación de reportes\newline
Given que existen registros de al menos 3 días,  
When el usuario solicita un reporte de evolución,  
Then el sistema genera gráficos de temperatura, peso, alimentación y sueño.\newline  
\newline
Escenario 2: Exportación\newline
Given que se genera un reporte,  
When el usuario lo exporta,  
Then obtiene un archivo con los datos y gráficos.\newline
\newline
Escenario 3: Sin datos \newline
Given que no existen registros suficientes,
When el usuario solicita un reporte,
Then el sistema indica que no hay información disponible.& 
EP03\\
\hline
HU05 
& 
Recibir notificaciones de alertas críticas
& 
Como padre, quiero recibir notificaciones push o por correo ante alertas críticas para no depender solo de la revisión manual de la aplicación. 
& 
Escenario 1:  Envío de notificación\newline
Given que se genera una alerta de alta prioridad,  
When el usuario tiene habilitadas las notificaciones,  
Then el sistema envía una notificación externa en un tiempo menor a 60 segundos\newline 
\newline
Escenario 2:  Acceso desde notificación\newline
Given que el usuario recibe una notificación,
When accede a ella,
Then el sistema muestra el detalle de la alerta correspondiente.\newline
& 
EP02\\
\hline
HU06
& 
Generar reportes médicos del bebé
& 
Como neonatólogo, quiero generar reportes detallados del bebé para usarlos durante la consulta médica. 
& 
Escenario 1: Generacion de reporte detallado\newline 
Given que el profesional tiene acceso al bebé,  
When solicita un reporte clínico,  
Then el sistema genera un documento con tendencias, alertas ocurridas y observaciones.\newline
\newline  
Escenario 2: Envio de reporte\newline
Given que se genera un reporte,  
When el profesional lo comparte,  
Then puede enviarlo directamente al correo del padre o guardarlo en el expediente.\newline
& 
EP03\\
\hline
HU07
& 
Registrarse en la plataforma
& 
Como padre o neonatólogo, quiero registrarme en la plataforma para crear una cuenta y acceder a las funcionalidades de SIRAN. 
& 
Escenario 1: Registro de usuario valido\newline
Given que el usuario ingresa datos válidos y completos,
When envía el formulario de registro,
Then el sistema crea la cuenta y envía un correo de confirmación.\newline
\newline
Escenario 2: Registro de usuario invalido por datos repetidos\newline 
Given que el usuario ingresa un correo electrónico ya registrado,
When intenta registrarse,
Then el sistema rechaza el registro e informa que el correo ya existe\newline
\newline
Escenario 3: Registro de usuario invalido por datos incompletos\newline 
Given que el usuario ingresa datos incompletos o en formato incorrecto,
When envía el formulario,
Then el sistema rechaza el registro.
& 
EP04\\
\hline
HU08
& 
Iniciar sesión en la plataforma
& 
Como padre o neonatólogo registrado, quiero iniciar sesión en la plataforma para acceder a mi cuenta. 
& 
Escenario 1: Inicio de sesion valido\newline 
Given que el usuario ingresa credenciales válidas,
When confirma el inicio de sesión,
Then el sistema permite el acceso a su cuenta.
\newline
Escenario 2: Inicio de sesion invalido por credenciales incorrectas\newline
Given que el usuario ingresa credenciales incorrectas,
When intenta iniciar sesión,
Then el sistema deniega el acceso.\newline
\newline
Escenario 3: Activacion de bloqueo de inicio de sesion\newline  
Given que el usuario excede el número máximo de intentos fallidos,
When intenta iniciar sesión,
Then el sistema bloquea temporalmente el inicio de sesion en el dispositivo.& 
EP04\\
\hline
HU09 
& 
Visualizar beneficios de la plataforma 
& 
Como visitante, quiero conocer los beneficios principales de SIRAN para decidir si registrarme. 
& 
Escenario 1:Vista previa de funcionalidades\newline 
Given que el visitante accede a la landing page,  
When visualiza la sección de beneficios,  
Then se muestran claramente las ventajas para padres y para personal médico.\newline
\newline 
Escenario 2:Presentacion de inicio de registro\newline
Given que el visitante navega en la landing page,
When desea registrarse o contactar,
Then el sistema presenta una opción disponible para iniciar el proceso de registro
& 
EP05\\
\hline
HU10
& 
Cerrar sesión en la plataforma 
& 
Como padre o neonatólogo autenticado, quiero cerrar mi sesión para proteger el acceso a mi cuenta.
& 
Escenario 1: Cierre de sesion valido\newline
Given que el usuario tiene una sesión activa,
When solicita cerrar sesión,
Then el sistema finaliza la sesión\newline
\newline
Escenario 2: Ciclo de sesiones en dispositivo\newline 
Given que el usuario cierra sesión,
When intenta acceder a información protegida,
Then el sistema solicita nuevamente el inicio de sesión.
& 
EP04\\
\hline
HU11
& 
Visualizar testimonios y casos de uso 
&  
Como visitante del segmento padre primerizo, quiero ver testimonios o casos de uso reales para generar confianza en la herramienta.
& 
Escenario 1: Testimonios de validacion en Landing Page\newline
Given que el visitante está en la sección de testimonios,  
When revisa el contenido,  
Then encuentra testimonios diferenciados de padres y de personal médico.\newline
\newline
Escenario 2: Variedad de testimonios en Landing Page\newline 
Given que se muestran testimonios,  
When el visitante los lee,  
Then puede identificar claramente a qué segmento pertenecen.\newline
& 
EP05\\
\hline
HU12
& 
Ver resumen del estado del bebé 
& 
Como padre, quiero ver un resumen diario o semanal del estado del bebé para tener una visión rápida. 
& 
Escenario 1: \newline 
Given que existen registros del día o semana,  
When el usuario accede al resumen,  
Then el sistema muestra promedio de parámetros y destacados relevantes.\newline  
\newline
Escenario 2:\newline 
Given que hubo alertas en el período,  
When se muestra el resumen,  
Then se incluyen las alertas más importantes.\newline
& 
EP05\\
\hline
HU13 
& 
Visualizar planes disponibles de la plataforma 
& 
Como visitante, quiero visualizar los planes de suscripción disponibles para evaluar cuál se adapta mejor a mis necesidades. 
& 
Escenario 1: Visualización de planes\newline
Given que el visitante accede a la sección de planes,
When revisa la información disponible,
Then el sistema presenta los planes de suscripción con sus características y precios correspondientes.\newline
\newline
Escenario 2: Selección de plan\newline
Given que el visitante evalúa los planes disponibles,
When decide continuar con uno de ellos,
Then el sistema presenta una opción para iniciar el proceso de suscripción.\newline
\newline
Escenario 3: Acceso a proceso de pago\newline
Given que el visitante selecciona un plan de suscripción,
When accede a la sección de pago,
Then el sistema muestra las opciones disponibles para completar la suscripción.\newline
& 
EP05\\
\hline
HU14
& 
Recibir alertas de pacientes con valores críticos
& 
Como neonatólogo, quiero recibir alertas cuando un paciente bajo mi seguimiento presente valores críticos para priorizar atención. 
& 
Escenario 1: Asignación de valores críticos\newline
Given que un bebé tiene un profesional asignado,  
When se registra un valor crítico,  
Then el sistema notifica al profesional.\newline  
\newline
Escenario 2: Comentario tras revisión\newline 
Given que se genera una alerta médica,  
When el profesional la revisa,  
Then puede marcarla como atendida y agregar comentarios.
& 
EP02\\
\hline
HU15 
& 
Registrar observaciones y síntomas del bebé 
& 
Como usuario, quiero registrar síntomas o observaciones cualitativas para complementar los datos cuantitativos.
& 
Escenario 1: Registro de observación\newline  
Given que el médico está registrando información del bebé,  
When agrega una observación textual (llanto excesivo, color de piel, etc.),  
Then el sistema la guarda asociada a la fecha y hora.\newline
\newline
Escenario 2: Visualización de observaciones\newline  
Given se dejo información dentro del registro del bebé Y mi cuenta esta iniciada,
When me dirija a la sección de observaciones del bebé
Then podré visualizar todas las observaciones del bebé y el médico que las hizo.
& 
EP01\\
\hline
HU16
& 
Revisar y marcar observaciones del bebé
& 
Como neonatólogo, quiero revisar y marcar observaciones registradas para dar seguimiento clínico 
& 
Escenario 1: Orden de observaciones mediante filtro\newline
Given que existen observaciones registradas,
When el profesional accede a ellas,
Then el sistema las muestra ordenadas, según el filtro seleccionado.\newline
\newline
Escenario 2: Cambio de estados de observaciones\newline
Given que se registra una observación,  
When el personal médico la revisa,  
Then puede marcarla como revisada.
& 
EP01\\
\hline
HU17
& 
Visualizar interfaz adaptativa 
& 
Como visitante, quiero que la landing page se adapte a mi dispositivo móvil para navegar cómodamente desde cualquier lugar.
& 
Escenario 1: Navegación móvil \newline
Given que el usuario accede desde un smartphone, 
When carga la página, 
Then los elementos se reordenan verticalmente y el menú se convierte en tipo hamburguesa. \newline
\newline
Escenario 2: Cambio de orientación \newline
Given que el usuario rota su tablet, 
When la pantalla cambia de tamaño, 
Then el diseño se ajusta fluidamente sin perder información ni superponer textos.
& 
EP05\\
\hline
HU18
& 
Cambiar idioma de la plataforma
& 
Como visitante extranjero, quiero cambiar el idioma de la página mediante un botón para entender mejor la propuesta de SIRAN. 
& 
Escenario 1: Traducción instantánea\newline
Given que el usuario está en la landing page, 
When hace clic en el botón de cambio de idioma (ES/EN), 
Then todos los textos de la página se traducen al idioma seleccionado sin recargar el sitio. \newline
\newline
Escenario 2: Persistencia de idioma \newline
Given que el usuario seleccionó un idioma, 
When navega entre las secciones de la landing, 
Then el sistema mantiene el idioma elegido durante toda la sesión. 
& 
EP05\\
\hline
HU19
& 
Navegación por anclas 
& 
Como visitante, quiero navegar por las secciones de la landing desde el menú principal para acceder rápido a la información. 
& 
Escenario 1: Desplazamiento suave \newline
Given que el usuario hace clic en "Planes" en el menú, 
When el sistema procesa el clic, 
Then la página se desliza suavemente hasta la sección correspondiente en lugar de saltar bruscamente. \newline
\newline
Escenario 2: Enlace roto \newline
Given que una sección fue eliminada, 
When el usuario hace clic en el menú, 
Then el sistema redirige al inicio de la página por defecto.
& 
EP05\\
\hline
HU20 
& 
Personalizar umbrales de alerta médica 
& 
Como neonatólogo, quiero ajustar los rangos de normalidad para un paciente específico para recibir alertas basadas en su condición clínica. 
& 
Escenario 1: Actualización de rangos \newline 
Given que el médico visualiza el perfil de un bebé con condiciones especiales,  
When modifica los valores máximos y mínimos de temperatura u oxígeno, 
Then el sistema aplica estos nuevos límites exclusivamente para dicho paciente. \newline  
\newline
Escenario 2: Valores inconsistentes \newline
Given que el médico intenta guardar un rango,
When el valor mínimo es mayor al valor máximo,
Then el sistema impide el guardado y solicita la corrección de los datos.
& 
EP02\\
\hline
\end{longtable}
```

- Technical Stories
```{=latex}
\begin{longtable}{|p{3cm}|p{3cm}|p{3cm}|p{3cm}|p{3cm}|}
\hline
STORY ID
& 
Titulo 
& 
Descripcion 
& 
Criterios de aceptacion 
& 
EPIC ID\\
\hline
TS01
& 
API de registro de datos del bebé 
& 
Como Developer, quiero implementar un endpoint para registrar los datos del bebé para almacenar información clínica en el sistema.
& 
Escenario 1: Registro exitoso\newline
Given que se recibe una solicitud POST con datos válidos del bebé,
When el endpoint procesa la solicitud,
Then el sistema almacena la información en la base de datos y retorna confirmación exitosa.\newline
\newline
Escenario 2: Datos inválidos\newline
Given que se recibe una solicitud POST con datos incompletos o incorrectos,
When el endpoint valida la información,
Then el sistema rechaza la solicitud y retorna un mensaje de error.
& 
EP01\\
\hline
TS02 
& 
API de consulta de historial del bebé 
& 
Como Developer, quiero implementar un endpoint para obtener el historial de registros del bebé para permitir su visualización y análisis. 
& 
Escenario 1: Consulta exitosa\newline
Given que se recibe una solicitud GET con un identificador válido del bebé,
When el endpoint procesa la solicitud,
Then el sistema retorna los registros ordenados cronológicamente.\newline
\newline
Escenario 2: Bebé no encontrado\newline
Given que se recibe una solicitud GET con un identificador inexistente,
When el endpoint procesa la solicitud,
Then el sistema retorna un mensaje indicando que no existe información. 
& 
EP01\\
\hline
TS03
& 
Lógica de generación de alertas por parámetros 
& 
Como Developer, quiero implementar la lógica de generación de alertas basada en parámetros registrados para detectar valores fuera de rango.
& 
Escenario 1: Generación de alerta\newline
Given que se registra un dato que excede los umbrales definidos,
When el sistema evalúa el valor,
Then se genera una alerta asociada al bebé.\newline
\newline
Escenario 2: Valor dentro de rango\newline
Given que se registra un dato dentro de los rangos normales,
When el sistema evalúa el valor,
Then no se genera ninguna alerta.
& 
EP02\\
\hline
TS04 
& 
API de consulta de alertas generadas 
& 
Como Developer, quiero implementar un endpoint para consultar las alertas generadas para permitir su visualización por usuarios autorizados. 
& 
Escenario 1: Consulta de alertas existentes\newline
Given que se recibe una solicitud GET con un bebé válido,
When el endpoint procesa la solicitud,
Then el sistema retorna la lista de alertas registradas.\newline
\newline
Escenario 2: Sin alertas\newline
Given que no existen alertas registradas para el bebé,
When el endpoint procesa la solicitud,
Then el sistema retorna una lista vacía.& 
EP02\\
\hline
TS05
& 
API de generación de reportes del bebé
& 
Como Developer, quiero implementar un endpoint para generar reportes del bebé para facilitar el análisis de su evolución. 
& 
Escenario 1: Generación exitosa de reporte\newline
Given que existen datos suficientes del bebé,
When se solicita el reporte,
Then el sistema genera un resumen con tendencias y datos relevantes.\newline
\newline
Escenario 2: Datos insuficientes\newline
Given que no existen registros suficientes,
When se solicita el reporte,
Then el sistema retorna un mensaje indicando falta de información. 
& 
EP03\\
\hline
TS06
& 
Definición de Modelo de Negocio y alcance 
& 
Como Developer quiero definir el modelo de negocio y el alcance completo del proyecto SIRAN para que el equipo cuente con una base alineada con los objetivos del producto antes de iniciar el desarrollo técnico. 
& 
Escenario 1: Validación de Business y Customer Assumptions en modelo de negocio\newline
Given que se ha recopilado la información del problema neonatal, la solución propuesta y el proceso Lean UX,
When se elabora el documento de modelo de negocio  
Then el documento contiene las Business Assumptions y Customer Assumptions completas tal como se describen en la sección 1.2.2.2.\newline
\newline
Escenario 2: Especificación de fuentes de ingreso e indicadores de éxito\newline
Given que se han definido las hipótesis de valor del producto,   
When se documenta el modelo de negocio, 
Then se especifican las posibles fuentes de ingresos y los indicadores de éxito esperados.\newline
\newline
Escenario 3: Definición de alcance funcional y no funcional por segmentos\newline
Given que se han identificado los segmentos objetivo, 
When se define el alcance del proyecto, 
Then el documento incluye el alcance funcional y no funcional.
& 
EP06\\
\hline
TS07 
& 
Análisis de Necesidades y Realidad del Usuario 
& 
Como Developer, quiero documentar el análisis de necesidades y la realidad del usuario para que el equipo tenga claridad sobre el problema, los usuarios afectados y los requisitos prioritarios antes de diseñar la arquitectura técnica. 
& 
Escenario 1: Documentación del análisis de necesidades y Problem Statement\newline
Given que se cuenta con la descripción del problema y las preguntas formuladas (5W´s y 2H´s)
When se redacta el análisis de necesidades,  
Then el documento incluye la tabla completa con las respuestas a cada pregunta y la Problem Statement del Lean UX\newline
\newline
Escenario 2: Documentación de necesidades por segmento objetivo\newline
Given que se han identificado los segmentos objetivos 
When se documenta la realidad del usuario,  
Then se describen las necesidades específicas de cada segmento
& 
EP06\\
\hline
TS08
& 
Especificación de Requisitos 
& 
Como Developer, quiero especificar los requisitos funcionales y no funcionales del sistema para contar con una base clara que guíe el desarrollo del producto. 
& 
Escenario 1: Documentación de User Stories y criterios de aceptación\newline
Given que se han identificado las necesidades de los usuarios y los segmentos objetivo,
When se redactan los requisitos funcionales,
Then el documento incluye User Stories con el formato y sus criterios de aceptación.\newline
\newline
Escenario 2: Definición de requisitos no funcionales\newline
Given que se han identificado las características de calidad del sistema,
When se documentan los requisitos,
Then se incluyen requisitos no funcionales como seguridad, rendimiento, disponibilidad y escalabilidad. 
& 
EP06\\
\hline
TS09
& 
Diseño de Producto 
& 
Como Developer, quiero diseñar la arquitectura y la experiencia del producto para definir cómo funcionará el sistema antes de su implementación. 
& 
Escenario 1: Diseño de arquitectura del sistema\newline
Given que se cuenta con los requisitos definidos,
When se elabora el diseño técnico,
Then se documenta la arquitectura del sistema incluyendo componentes, servicios y relaciones.\newline
\newline
Escenario 2: Diseño de interfaz y experiencia de usuario\newline
Given que se han identificado los flujos principales del usuario,
When se diseña el producto,
Then se incluyen prototipos o wireframes que representan la interacción del usuario con el sistema. 
& 
EP06\\
\hline
TS10 
& 
Implementación de Producto, Validación y Deploy 
& 
Como Developer, quiero implementar, validar y desplegar el sistema para asegurar su funcionamiento y disponibilidad para los usuarios finales. 
& 
Escenario 1: Implementación de funcionalidades principales\newline
Given que se cuenta con los requisitos y diseño definidos,
When se desarrolla el sistema,
Then se implementan las funcionalidades principales según las User Stories priorizadas.\newline
\newline
Escenario 2: Validación del sistema\newline
Given que el sistema ha sido implementado,
When se realizan pruebas funcionales,
Then se verifica que las funcionalidades cumplen con los criterios de aceptación definidos. 
& 
EP06\\
\hline
\end{longtable}
```

## 3.2. Impact Mapping

## 3.3. Product Backlog