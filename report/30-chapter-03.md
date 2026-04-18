# Capítulo III: Requirements Specification

## 3.1. User Stories

```{=latex}
\newpage
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
Relacionado con (EPIC ID)\\
\hline
EPIC / Story 
& 
Titulo 
& 
Descripcion 
& 
Criterios de aceptacion 
& 
Relacionado con (EPIC ID)\\
\hline
EPIC / Story 
& 
Titulo 
& 
Descripcion 
& 
Criterios de aceptacion 
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
\newline
Escenario 4: Confirmación de suscripción\newline
Given que el usuario selecciona un método de pago,
When confirma la operación,
Then el sistema registra la suscripción como exitosa y activa el plan correspondiente.\newline
\newline
Escenario 5: Cancelación del proceso\newline
Given que el usuario inicia el proceso de suscripción,
When abandona la operación antes de confirmarla,
Then el sistema no activa ningún plan.\newline
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
EPIC / Story 
& 
Titulo 
& 
Descripcion 
& 
Criterios de aceptacion 
& 
Relacionado con (EPIC ID)\\
\hline
EPIC / Story 
& 
Titulo 
& 
Descripcion 
& 
Criterios de aceptacion 
& 
Relacionado con (EPIC ID)\\
\hline
EPIC / Story 
& 
Titulo 
& 
Descripcion 
& 
Criterios de aceptacion 
& 
Relacionado con (EPIC ID)\\
\hline
EPIC / Story 
& 
Titulo 
& 
Descripcion 
& 
Criterios de aceptacion 
& 
Relacionado con (EPIC ID)\\
\hline
EPIC / Story 
& 
Titulo 
& 
Descripcion 
& 
Criterios de aceptacion 
& 
Relacionado con (EPIC ID)\\
\hline
EPIC / Story 
& 
Titulo 
& 
Descripcion 
& 
Criterios de aceptacion 
& 
Relacionado con (EPIC ID)\\
\hline
EPIC / Story 
& 
Titulo 
& 
Descripcion 
& 
Criterios de aceptacion 
& 
Relacionado con (EPIC ID)\\
\hline
EPIC / Story 
& 
Titulo 
& 
Descripcion 
& 
Criterios de aceptacion 
& 
Relacionado con (EPIC ID)\\
\hline
EPIC / Story 
& 
Titulo 
& 
Descripcion 
& 
Criterios de aceptacion 
& 
Relacionado con (EPIC ID)\\
\hline
\end{longtable}
```

## 3.2. Impact Mapping

## 3.3. Product Backlog