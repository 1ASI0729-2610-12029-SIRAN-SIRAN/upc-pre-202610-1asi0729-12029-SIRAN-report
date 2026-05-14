# Capítulo III: Requirements Specification

## 3.1. User Stories

- **Epics**

<table border="1" style="border-collapse:collapse">
  <thead>
    <tr>
      <th>EPIC ID</th>
      <th>Titulo</th>
      <th>Descripcion</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>EP01</td>
      <td>Gestión y Monitoreo de Datos Neonatales</td>
      <td>Como padre o neonatólogo, quiero registrar y consultar información del recién nacido para llevar un control detallado de su evolución y seguimiento clínico.</td>
    </tr>
    <tr>
      <td>EP02</td>
      <td>Alertas Inteligentes y Notificaciones</td>
      <td>Como padre o neonatólogo, quiero recibir alertas y notificaciones sobre valores críticos del bebé para reaccionar oportunamente y priorizar la atención médica.</td>
    </tr>
    <tr>
      <td>EP03</td>
      <td>Análisis y Reportes</td>
      <td>Como padre o neonatólogo, quiero visualizar reportes y resúmenes del estado del bebé para comprender su evolución y apoyar la toma de decisiones.</td>
    </tr>
    <tr>
      <td>EP04</td>
      <td>Gestión de Cuenta</td>
      <td>Como padre o neonatólogo, quiero gestionar mi cuenta en la plataforma para acceder de manera segura a las funcionalidades del sistema.</td>
    </tr>
    <tr>
      <td>EP05</td>
      <td>Captación y Presentación de la Plataforma</td>
      <td>Como visitante, quiero conocer la plataforma y sus beneficios para evaluar su utilidad y decidir si registrarme.</td>
    </tr>
    <tr>
      <td>EP06</td>
      <td>Documentación Técnica y Marco Estratégico del Proyecto</td>
      <td>Como developer, quiero definir y documentar el modelo de negocio, requisitos y diseño del sistema para guiar el desarrollo del producto de manera estructurada.</td>
    </tr>
  </tbody>
</table>


- **User Stories**


<table border="1" style="border-collapse:collapse">
  <thead>
    <tr>
      <th>STORY ID</th>
      <th>Titulo</th>
      <th>Descripcion</th>
      <th>Criterios de aceptacion</th>
      <th>EPIC ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>HU01</td>
      <td>Registrar parámetros diarios del bebé</td>
      <td>Como padre, quiero registrar los parámetros diarios del bebé para llevar un control preciso de su evolución.</td>
      <td><strong>Escenario 1:</strong> Registro correcto (almacena datos con fecha/hora). 

GIVEN que el padre se encuentra en el formulario de registro diario de parámetros y ha ingresado valores válidos en todos los campos obligatorios como peso, temperatura y frecuencia alimenticia.

WHEN el padre presiona el botón de guardar.

THEN el sistema confirma que el registro fue exitoso, almacena los datos en la base de datos y los vincula automáticamente con la fecha y hora exacta.

<br><strong>Escenario 2:</strong> Datos incompletos (el sistema rechaza el registro).

GIVEN que el padre está completando el formulario de evolución diaria y deja campos críticos sin información o con valores vacíos.

WHEN intenta procesar el registro seleccionando la opción de guardar.

THEN el sistema bloquea la transacción, no guarda ninguna información en el historial y muestra un mensaje de alerta resaltando los campos que deben ser corregidos.</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>HU02</td>
      <td>Consultar historial completo del recién nacido</td>
      <td>Como neonatólogo, quiero consultar el historial completo de registros de un recién nacido.</td>
      <td><strong>Escenario 1:</strong> Muestra datos cronológicamente.

GIVEN el neonatólogo ha seleccionado el perfil específico de un recién nacido y accede a la sección de historial completo.

WHEN el usuario solicita la visualización de todos los registros almacenados en el sistema.

THEN el sistema despliega una lista detallada de todos los parámetros médicos organizados de forma descendente desde el registro más reciente hasta el más antiguo.

<br><strong>Escenario 2:</strong> Filtros por parámetro o rango de fechas.

Given el neonatólogo se encuentra en la pantalla de historial del paciente y cuenta con las opciones de filtrado por tipo de dato o periodo de tiempo.

When el usuario define un rango de fechas específico o selecciona un parámetro particular como la temperatura para realizar la búsqueda.

Then el sistema actualiza la vista mostrando únicamente los registros que coinciden con los criterios aplicados para facilitar el análisis clínico.


</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>HU03</td>
      <td>Recibir alertas por parámetros anormales</td>
      <td>Como padre, quiero recibir alertas automáticas cuando un parámetro se salga de los rangos normales.</td>
      <td><strong>Escenario 1:</strong> Generación de alerta.

GIVEN el sistema detecta el ingreso de un nuevo registro de salud para el recién nacido.

WHEN el valor ingresado supera o es inferior a los límites establecidos como normales para su edad.

THEN el sistema genera una alerta automática de forma instantánea y la envía al dispositivo del usuario.

<br><strong>Escenario 2:</strong> Visualización con prioridad.

GIVEN el padre tiene la aplicación abierta o se encuentra en la pantalla de inicio del sistema.

WHEN ocurre una detección de un parámetro en nivel crítico.

THEN el sistema despliega una notificación visual llamativa que destaca sobre el resto de las interfaces para asegurar una atención inmediata.

<br><strong>Escenario 3:</strong> No alerta si el dato es normal.

Given el usuario registra parámetros médicos que se encuentran dentro de los rangos saludables definidos.

When el proceso de validación del sistema analiza los datos guardados.

Then el sistema almacena la información silenciosamente en el historial sin disparar ningún tipo de notificación o aviso de emergencia.
</td>
      <td>EP02</td>
    </tr>
    <tr>
      <td>HU04</td>
      <td>Ver reportes gráficos del bebé</td>
      <td>Como padre, quiero visualizar reportes gráficos de la evolución del bebé.</td>
      <td><strong>Escenario 1:</strong> Generación de gráficos (temp, peso, etc). 

Given el padre se encuentra en la sección de analítica y selecciona un parámetro específico como temperatura o peso.

When el usuario solicita la visualización del progreso en la interfaz.

Then el sistema genera automáticamente un gráfico de líneas o barras que muestra la tendencia de los valores registrados a lo largo del tiempo.<br><strong>

Escenario 2:</strong> Exportación de reporte.
Given el usuario tiene un reporte gráfico generado en la pantalla de su dispositivo.

When selecciona la opción de exportar o descargar el documento.

Then el sistema procesa la información actual y genera un archivo en formato PDF listo para ser compartido con el médico pediatra.

<br><strong>Escenario 3:</strong> Sin datos suficientes.Given el padre accede a la sección de reportes gráficos por primera vez o tras un periodo sin actividad.

When el sistema verifica que existen menos de dos registros para el parámetro seleccionado.

Then el sistema muestra un mensaje informativo indicando que no hay datos suficientes para trazar una gráfica y sugiere realizar nuevos registros.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>HU05</td>
      <td>Recibir notificaciones de alertas críticas</td>
      <td>Como padre, quiero recibir notificaciones push o correo ante alertas críticas para actuar de inmediato ante emergencias.</td>
      <td>
        <strong>Escenario 1: Envío rápido</strong><br>
        Given el sistema detecta un parámetro médico en estado crítico.
        When se activa el protocolo de emergencia. 
        Then el sistema envía una notificación push y correo en menos de 60 segundos.<br><br>
        <strong>Escenario 2: Acceso directo</strong><br>
        Given el padre recibe una alerta crítica en su dispositivo. 
        When el usuario interactúa con la notificación. 
        Then el sistema abre la aplicación y redirige automáticamente al detalle de la alerta.
      </td>
      <td>EP02</td>
    </tr>
    <tr>
      <td>HU06</td>
      <td>Generar reportes médicos del bebé</td>
      <td>Como neonatólogo, quiero generar reportes detallados para la consulta médica con el fin de facilitar la toma de decisiones clínicas.</td>
      <td>
        <strong>Escenario 1: Reporte completo</strong><br>
        Given el neonatólogo solicita un informe de un periodo determinado. 
        When el sistema procesa la solicitud de informe profesional. 
        Then el sistema genera un documento con el análisis de tendencias y resumen de alertas.<br><br>
        <strong>Escenario 2: Exportación</strong><br>
        Given el reporte médico ha sido generado exitosamente. 
        When el neonatólogo elige la opción de compartir. 
        Then el sistema permite descargar el PDF o enviarlo directamente por correo electrónico.
      </td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>HU07</td>
      <td>Registrarse en la plataforma</td>
      <td>Como padre o neonatólogo, quiero registrarme en la plataforma.</td>
      <td><strong>Escenario 1: Registro válido.

GIVEN que el usuario se encuentra en la pantalla de Registro y el correo ingresado no existe previamente en la base de datos.

WHEN completa todos los campos requeridos y presiona el botón "Crear Cuenta".

THEN el servidor responde con un 201 Created, los datos se almacenan en el archivo db.json y el usuario es redirigido a la pantalla de bienvenida o login.<br>

<strong>Escenario 2: Correo repetido (error).

GIVEN que el usuario intenta registrarse con un correo electrónico que ya está vinculado a una cuenta existente.

WHEN completa el formulario y presiona "Crear Cuenta".

THEN el servidor responde con un error de conflicto (ej. 409 Conflict) y el sistema muestra un mensaje indicando que el correo ya está en uso.<br>

<strong>Escenario 3: Datos incompletos (error).

GIVEN que el usuario se encuentra en el formulario de registro.

WHEN deja campos obligatorios vacíos (como la contraseña o el correo) e intenta enviar el formulario.

THEN el servidor responde con un 400 Bad Request y el frontend resalta los campos faltantes con un mensaje de advertencia.</td>
      <td>EP04</td>
    </tr>
    <tr>
  <td>HU08</td>
  <td>Iniciar sesión en la plataforma</td>
  <td>Como usuario registrado, quiero iniciar sesión en la plataforma para acceder a mis datos.</td>
  <td>
    <strong>Escenario 1: Acceso válido</strong><br>
    Given el usuario ingresa su correo y contraseña correctos.<br>
    When presiona el botón de ingresar.<br>
    Then el sistema valida las credenciales y redirige al panel principal.<br><br>
    <strong>Escenario 2: Credenciales incorrectas</strong><br>
    Given el usuario ingresa datos que no coinciden con los registros.<br>
    When intenta iniciar sesión.<br>
    Then el sistema deniega el acceso y muestra un mensaje de error.<br><br>
    <strong>Escenario 3: Bloqueo temporal</strong><br>
    Given el usuario ha fallado cinco intentos consecutivos.<br>
    When intenta un nuevo ingreso.<br>
    Then el sistema bloquea la cuenta temporalmente por seguridad.
  </td>
  <td>EP04</td>
</tr>
<tr>
  <td>HU09</td>
  <td>Visualizar beneficios de la plataforma</td>
  <td>Como visitante, quiero conocer los beneficios principales de SIRAN.</td>
  <td>
    <strong>Escenario 1: Vista de beneficios</strong><br>
    Given el visitante accede a la página principal.<br>
    When navega hacia la sección de beneficios.<br>
    Then el sistema despliega las ventajas como monitoreo y alertas.<br><br>
    <strong>Escenario 2: Inicio de registro</strong><br>
    Given el visitante lee los beneficios.<br>
    When selecciona el botón de acción.<br>
    Then el sistema lo redirige al formulario de registro.
  </td>
  <td>EP05</td>
</tr>

<tr>
  <td>HU10</td>
  <td>Cerrar sesión en la plataforma</td>
  <td>Como usuario autenticado, quiero cerrar mi sesión para proteger mi información.</td>
  <td>
    <strong>Escenario 1: Finalización de sesión</strong><br>
    Given el usuario selecciona cerrar sesión.<br>
    When el sistema procesa la solicitud.<br>
    Then se destruye el token de acceso y redirige al inicio.<br><br>
    <strong>Escenario 2: Protección de datos</strong><br>
    Given el usuario ha cerrado sesión.<br>
    When intenta retroceder en el navegador.<br>
    Then el sistema bloquea el acceso y solicita credenciales.
  </td>
  <td>EP04</td>
</tr>

<tr>
  <td>HU11</td>
  <td>Visualizar testimonios y casos de uso</td>
  <td>Como visitante, quiero ver testimonios reales para generar confianza.</td>
  <td>
    <strong>Escenario 1: Testimonios segmentados</strong><br>
    Given el visitante está en la sección de testimonios.<br>
    When selecciona el filtro de médicos o padres.<br>
    Then el sistema muestra las experiencias según el rol elegido.<br><br>
    <strong>Escenario 2: Identificación clara</strong><br>
    Given el sistema carga los testimonios.<br>
    When el usuario visualiza una entrada.<br>
    Then el sistema muestra una etiqueta que identifica al autor.
  </td>
  <td>EP05</td>
</tr>

<tr>
  <td>HU12</td>
  <td>Ver resumen del estado del bebé</td>
  <td>Como padre, quiero ver un resumen diario o semanal de la salud de mi bebé.</td>
  <td>
    <strong>Escenario 1: Promedios y destacados</strong><br>
    Given el padre accede al dashboard principal.<br>
    When solicita el resumen del periodo.<br>
    Then el sistema muestra promedios de temperatura, peso y alimentación.<br><br>
    <strong>Escenario 2: Alertas importantes</strong><br>
    Given se genera el resumen en pantalla.<br>
    When existen registros críticos en ese lapso.<br>
    Then el sistema resalta los eventos críticos para su revisión.
  </td>
  <td>EP05</td>
</tr>

<tr>
  <td>HU13</td>
  <td>Visualizar planes disponibles</td>
  <td>Como visitante, quiero visualizar los planes de suscripción disponibles.</td>
  <td>
    <strong>Escenario 1: Vista de precios</strong><br>
    Given el visitante ingresa a suscripciones.<br>
    When el sistema carga la información.<br>
    Then el usuario ve las tarjetas con costos y características.<br><br>
    <strong>Escenario 2: Selección y pago</strong><br>
    Given el usuario elige un plan específico.<br>
    When presiona proceder al pago.<br>
    Then el sistema lo redirige a la pasarela segura.
  </td>
  <td>EP05</td>
</tr>

<tr>
  <td>HU14</td>
  <td>Recibir alertas de pacientes con valores críticos</td>
  <td>Como neonatólogo, quiero recibir alertas de mis pacientes para intervenir a tiempo.</td>
  <td>
    <strong>Escenario 1: Notificación crítica</strong><br>
    Given un paciente bajo supervisión tiene un registro fuera de rango.<br>
    When el sistema detecta la anomalía.<br>
    Then el neonatólogo recibe una alerta inmediata en su panel.<br><br>
    <strong>Escenario 2: Gestión de alerta</strong><br>
    Given el médico visualiza la alerta recibida.<br>
    When ingresa a gestionar alerta.<br>
    Then el sistema permite registrar un comentario y marcar como revisada.
  </td>
  <td>EP02</td>
</tr>

<tr>
  <td>HU15</td>
  <td>Registrar observaciones y síntomas</td>
  <td>Como usuario, quiero registrar síntomas u observaciones cualitativas del bebé.</td>
  <td>
    <strong>Escenario 1: Guardado de nota</strong><br>
    Given el usuario redacta un síntoma observado.<br>
    When selecciona guardar.<br>
    Then el sistema almacena el texto con la fecha y autor.<br><br>
    <strong>Escenario 2: Historial</strong><br>
    Given el usuario accede a la línea de tiempo.<br>
    When solicita ver las notas previas.<br>
    Then el sistema lista todas las observaciones registradas.
  </td>
  <td>EP01</td>
</tr>

<tr>
  <td>HU16</td>
  <td>Revisar y marcar observaciones del bebé</td>
  <td>Como neonatólogo, quiero revisar y marcar observaciones enviadas por los padres.</td>
  <td>
    <strong>Escenario 1: Filtros de severidad</strong><br>
    Given el neonatólogo tiene una lista de observaciones.<br>
    When aplica un filtro por severidad.<br>
    Then el sistema organiza la lista priorizando las urgentes.<br><br>
    <strong>Escenario 2: Cambio de estado</strong><br>
    Given el médico analiza una observación.<br>
    When selecciona marcar como revisada.<br>
    Then el sistema cambia el estado a completado y lo archiva.
  </td>
  <td>EP01</td>
</tr>

<tr>
  <td>HU17</td>
  <td>Visualizar interfaz adaptativa</td>
  <td>Como visitante, quiero una interfaz que se adapte a dispositivos móviles.</td>
  <td>
    <strong>Escenario 1: Navegación móvil</strong><br>
    Given el visitante accede desde un smartphone.<br>
    When la pantalla es menor a 768px.<br>
    Then el sistema contrae el menú en un botón de hamburguesa.<br><br>
    <strong>Escenario 2: Ajuste de gráficas</strong><br>
    Given el usuario visualiza una gráfica móvil.<br>
    When rota la pantalla horizontalmente.<br>
    Then el sistema escala los elementos automáticamente al nuevo ancho.
  </td>
  <td>EP05</td>
</tr>

<tr>
  <td>HU18</td>
  <td>Cambiar idioma de la plataforma</td>
  <td>Como visitante, quiero cambiar el idioma de la interfaz.</td>
  <td>
    <strong>Escenario 1: Traducción instantánea</strong><br>
    Given el usuario selecciona un nuevo idioma.<br>
    When el sistema procesa el cambio.<br>
    Then se traducen los textos sin recargar la página.<br><br>
    <strong>Escenario 2: Persistencia</strong><br>
    Given el usuario cambió el idioma a inglés.<br>
    When vuelve a ingresar más tarde.<br>
    Then el sistema carga la interfaz en el idioma guardado.
  </td>
  <td>EP05</td>
</tr>

<tr>
  <td>HU19</td>
  <td>Navegación por anclas</td>
  <td>Como visitante, quiero navegar por las secciones del menú rápidamente.</td>
  <td>
    <strong>Escenario 1: Desplazamiento suave</strong><br>
    Given el visitante hace clic en una opción del menú.<br>
    When se activa el ancla interna.<br>
    Then el sistema realiza un scroll suave hasta la sección.<br><br>
    <strong>Escenario 2: Redirección</strong><br>
    Given el usuario accede a un enlace roto.<br>
    When el sistema detecta el error.<br>
    Then redirige automáticamente a la sección de inicio.
  </td>
  <td>EP05</td>
</tr>

<tr>
  <td>HU20</td>
  <td>Personalizar umbrales de alerta médica</td>
  <td>Como neonatólogo, quiero ajustar rangos de alerta por paciente.</td>
  <td>
    <strong>Escenario 1: Nuevos límites</strong><br>
    Given el médico modifica los valores mínimos y máximos.<br>
    When guarda la configuración del paciente.<br>
    Then el sistema dispara alertas basadas en estos nuevos límites.<br><br>
    <strong>Escenario 2: Validación</strong><br>
    Given el médico ingresa un mínimo mayor al máximo.<br>
    When intenta guardar.<br>
    Then el sistema bloquea el cambio y muestra una advertencia.
  </td>
  <td>EP02</td>
</tr>
  </tbody>
</table>


- **Technical Stories**


<table border="1" style="border-collapse:collapse">
  <thead>
    <tr>
      <th>STORY ID</th>
      <th>Titulo</th>
      <th>Descripcion</th>
      <th>Criterios de aceptacion</th>
      <th>EPIC ID</th>
    </tr>
  </thead>
  <tbody>
   <tr>
  <td>TS01</td>
  <td>API de registro de datos del bebé</td>
  <td>Como Developer, quiero implementar un endpoint para registrar los datos del bebé para almacenar información clínica.</td>
  <td>
    <strong>Escenario 1: Registro exitoso</strong><br>
    Given el cliente envía una petición POST con un cuerpo JSON que contiene peso, temperatura y frecuencia alimenticia válidos.<br>
    When el servidor procesa la solicitud y valida los tipos de datos.<br>
    Then el sistema responde con un estado 201 Created, confirma la persistencia en la base de datos y retorna el objeto creado.<br><br>
    <strong>Escenario 2: Datos inválidos</strong><br>
    Given el cuerpo de la petición POST está incompleto o contiene valores fuera de los formatos permitidos.<br>
    When el servidor intenta validar la estructura del JSON.<br>
    Then el sistema rechaza la operación con un error 400 Bad Request y detalla los campos incorrectos.
  </td>
  <td>EP01</td>
</tr>

<tr>
  <td>TS02</td>
  <td>API de consulta de historial del bebé</td>
  <td>Como Developer, quiero implementar un endpoint para obtener el historial de registros del bebé.</td>
  <td>
    <strong>Escenario 1: Consulta exitosa</strong><br>
    Given el cliente realiza una petición GET proporcionando un identificador de bebé válido.<br>
    When el servidor recupera los registros asociados desde la base de datos.<br>
    Then el sistema retorna un estado 200 OK junto con la lista de registros ordenados cronológicamente.<br><br>
    <strong>Escenario 2: Bebé no encontrado</strong><br>
    Given el identificador del bebé proporcionado en la URL no existe en el sistema.<br>
    When se ejecuta la búsqueda en el repositorio.<br>
    Then el servidor responde con un error 404 Not Found y un mensaje explicativo.
  </td>
  <td>EP01</td>
</tr>

<tr>
  <td>TS03</td>
  <td>Lógica de generación de alertas</td>
  <td>Como Developer, quiero implementar la lógica de alertas basada en parámetros para detectar valores fuera de rango.</td>
  <td>
    <strong>Escenario 1: Generación de alerta</strong><br>
    Given se ha registrado un nuevo valor clínico para un paciente.<br>
    When la lógica de negocio compara el dato contra los umbrales mínimos y máximos configurados.<br>
    Then el sistema dispara un evento de alerta crítica si el valor excede o es inferior al rango permitido.<br><br>
    <strong>Escenario 2: Valor dentro de rango</strong><br>
    Given se procesa un nuevo dato de salud del recién nacido.<br>
    When la validación comprueba que el dato es normal según la configuración.<br>
    Then el sistema finaliza el proceso sin activar ninguna bandera de alerta.
  </td>
  <td>EP02</td>
</tr>

<tr>
  <td>TS04</td>
  <td>API de consulta de alertas generadas</td>
  <td>Como Developer, quiero implementar un endpoint para consultar las alertas generadas.</td>
  <td>
    <strong>Escenario 1: Consulta exitosa</strong><br>
    Given el usuario autenticado solicita el listado de alertas desde su panel de control.<br>
    When el servidor filtra las notificaciones activas para ese usuario.<br>
    Then el sistema retorna un arreglo con los detalles de cada alerta registrada.<br><br>
    <strong>Escenario 2: Sin alertas</strong><br>
    Given no se han producido eventos críticos para el paciente en el periodo consultado.<br>
    When se realiza la petición de consulta al servidor.<br>
    Then el sistema responde con un estado 200 OK y una lista vacía.
  </td>
  <td>EP02</td>
</tr>

<tr>
  <td>TS05</td>
  <td>API de generación de reportes del bebé</td>
  <td>Como Developer, quiero implementar un endpoint para generar reportes para el análisis de evolución.</td>
  <td>
    <strong>Escenario 1: Generación exitosa</strong><br>
    Given existen suficientes registros históricos para calcular tendencias de salud.<br>
    When el servidor procesa una solicitud de reporte analítico.<br>
    Then el sistema genera un resumen de tendencias evolutivas y lo entrega en formato estructurado.<br><br>
    <strong>Escenario 2: Datos insuficientes</strong><br>
    Given la base de datos contiene muy poca información para realizar cálculos estadísticos.<br>
    When se intenta invocar el endpoint de reportes.<br>
    Then el sistema retorna un error indicando que se requieren más registros para proceder.
  </td>
  <td>EP03</td>
</tr>

<tr>
  <td>TS06</td>
  <td>Definición de Modelo de Negocio y alcance</td>
  <td>Como Developer quiero definir el modelo de negocio y alcance del proyecto SIRAN.</td>
  <td>
    <strong>Escenario 1: Validación de supuestos</strong><br>
    Given se han identificado los problemas principales en el cuidado neonatal.<br>
    When se documentan las suposiciones de negocio y del cliente.<br>
    Then el equipo valida que el proyecto resuelve una necesidad real del mercado.<br><br>
    <strong>Escenario 2: Especificación de ingresos</strong><br>
    Given se analiza la sostenibilidad financiera del proyecto.<br>
    When se definen los canales de monetización e indicadores clave de rendimiento.<br>
    Then se establece un plan claro de crecimiento y retorno de inversión.
  </td>
  <td>EP06</td>
</tr>

<tr>
  <td>TS07</td>
  <td>Análisis de Necesidades y Realidad del Usuario</td>
  <td>Como Developer, quiero documentar las necesidades para tener claridad antes de diseñar la arquitectura.</td>
  <td>
    <strong>Escenario 1: Documentación técnica</strong><br>
    Given se inicia la fase de descubrimiento del producto.<br>
    When se completan las herramientas 5W's, 2H's y el enunciado del problema.<br>
    Then el equipo de desarrollo obtiene una visión clara de qué construir y por qué.<br><br>
    <strong>Escenario 2: Necesidades por segmento</strong><br>
    Given se han identificado padres y neonatólogos como usuarios principales.<br>
    When se mapean los requerimientos específicos de cada grupo.<br>
    Then el sistema prioriza funcionalidades que agreguen valor directo a cada rol.
  </td>
  <td>EP06</td>
</tr>

<tr>
  <td>TS08</td>
  <td>Especificación de Requisitos</td>
  <td>Como Developer, quiero especificar los requisitos funcionales y no funcionales.</td>
  <td>
    <strong>Escenario 1: User Stories</strong><br>
    Given se cuenta con el análisis de necesidades previo.<br>
    When se redactan las historias de usuario siguiendo el formato estándar.<br>
    Then cada historia incluye criterios de aceptación claros para su validación técnica.<br><br>
    <strong>Escenario 2: Requisitos no funcionales</strong><br>
    Given el sistema manejará datos sensibles de salud infantil.<br>
    When se definen las políticas de seguridad, rendimiento y disponibilidad.<br>
    Then la arquitectura se diseña para cumplir con estándares de protección de datos.
  </td>
  <td>EP06</td>
</tr>

<tr>
  <td>TS09</td>
  <td>Diseño de Producto</td>
  <td>Como Developer, quiero diseñar la arquitectura y experiencia antes de la implementación.</td>
  <td>
    <strong>Escenario 1: Arquitectura de componentes</strong><br>
    Given los requisitos técnicos están definidos.<br>
    When se elaboran los diagramas de arquitectura y flujo de datos.<br>
    Then el equipo tiene un mapa técnico para guiar la codificación.<br><br>
    <strong>Escenario 2: Prototipado</strong><br>
    Given se requiere validar la usabilidad con los interesados.<br>
    When se diseñan los wireframes o prototipos de alta fidelidad.<br>
    Then el frontend se construye sobre una base visual aprobada.
  </td>
  <td>EP06</td>
</tr>

<tr>
  <td>TS10</td>
  <td>Implementación, Validación y Deploy</td>
  <td>Como Developer, quiero implementar, validar y desplegar el sistema.</td>
  <td>
    <strong>Escenario 1: Desarrollo iterativo</strong><br>
    Given existe un backlog de tareas priorizado.<br>
    When se desarrollan las funcionalidades en ciclos de entrega.<br>
    Then el sistema crece de manera estable y controlada.<br><br>
    <strong>Escenario 2: Verificación y despliegue</strong><br>
    Given el código ha pasado por la fase de implementación.<br>
    When se ejecutan pruebas funcionales y se realiza el deploy.<br>
    Then el producto final está disponible para el usuario en el entorno de producción.
  </td>
  <td>EP06</td>
</tr>
  </tbody>
</table>

## 3.2. Impact Mapping

<img src="assets/impact-mapping.jpeg" alt="Impact Mapping"/>

## 3.3. Product Backlog

El siguiente Product Backlog presenta la priorización de las User Stories del sistema SIRAN, organizadas en función del valor que aportan al negocio. Se incluyen las historias relacionadas con la Plataforma Web Informativa (Landing Page) para validar la propuesta de valor del producto y atraer usuarios desde etapas tempranas. Seguidamente se priorizan las funcionalidades clave del sistema relacionadas con el monitoreo del bebé, generación de alertas y análisis de datos. Finalmente, se consideran las historias asociadas a la gestión de cuentas, dado que no representan el mayor valor inicial para el usuario. 

<table border="1" style="border-collapse: collapse">
  <thead>
    <tr>
      <th>ID</th>
      <th>Título</th>
      <th>Descripción</th>
      <th>Estimación (Esfuerzo)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>HU07</td>
      <td>Registrarse en la plataforma</td>
      <td>Permite a los padres o neonatólogos crear una cuenta nueva en SIRAN proporcionando sus datos personales y credenciales de acceso.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>HU08</td>
      <td>Iniciar sesión en la plataforma</td>
      <td>Facilita el acceso seguro de los usuarios registrados a sus respectivos paneles de control mediante la validación de credenciales.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>HU01</td>
      <td>Registrar parámetros diarios del bebé</td>
      <td>Permite el ingreso manual de datos vitales como temperatura, peso y frecuencia de alimentación para el seguimiento del recién nacido.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>HU02</td>
      <td>Consultar historial completo del recién nacido</td>
      <td>Ofrece una vista detallada y cronológica de todos los registros médicos y parámetros ingresados desde el nacimiento del bebé.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>HU03</td>
      <td>Recibir alertas por parámetros anormales</td>
      <td>Implementa un sistema de detección automática que avisa a los padres cuando un valor ingresado se sale de los rangos normales.</td>
      <td>8</td>
    </tr>
    <tr>
      <td>HU14</td>
      <td>Recibir alertas de pacientes con valores críticos</td>
      <td>Módulo especializado para neonatólogos que centraliza las notificaciones de urgencia de todos los bebés bajo su supervisión médica.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>HU05</td>
      <td>Recibir notificaciones de alertas críticas</td>
      <td>Envío de mensajes push o correos electrónicos inmediatos ante eventos que requieran atención médica urgente.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>HU04</td>
      <td>Ver reportes gráficos del bebé</td>
      <td>Visualización mediante gráficos interactivos de la evolución de las métricas de salud para facilitar la interpretación de tendencias.</td>
      <td>8</td>
    </tr>
    <tr>
      <td>HU06</td>
      <td>Generar reportes médicos del bebé</td>
      <td>Funcionalidad para exportar resúmenes detallados de la salud del infante en formatos listos para compartir con especialistas.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>HU15</td>
      <td>Registrar observaciones y síntomas del bebé</td>
      <td>Permite a los cuidadores anotar comportamientos, síntomas cualitativos o notas relevantes que no son puramente numéricas.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>HU16</td>
      <td>Revisar y marcar observaciones del bebé</td>
      <td>Permite al personal médico validar, comentar y marcar como atendidas las notas enviadas por los padres.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>HU12</td>
      <td>Ver resumen del estado del bebé</td>
      <td>Dashboard simplificado que muestra los indicadores más recientes y el estado general de salud del bebé de un solo vistazo.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>HU20</td>
      <td>Personalizar umbrales de alerta médica</td>
      <td>Permite a los médicos ajustar los rangos de normalidad de forma individualizada según las necesidades específicas de cada paciente.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>HU10</td>
      <td>Cerrar sesión en la plataforma</td>
      <td>Garantiza la salida segura del sistema y la protección de los datos sensibles al finalizar la sesión del usuario.</td>
      <td>1</td>
    </tr>
    <tr>
      <td>HU09</td>
      <td>Visualizar beneficios de la plataforma (Landing)</td>
      <td>Sección informativa de la página principal que explica las ventajas y funcionalidades clave del sistema SIRAN para nuevos usuarios.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>HU11</td>
      <td>Visualizar testimonios y casos de uso</td>
      <td>Exposición de experiencias reales de otros padres y médicos para generar confianza y demostrar la eficacia del sistema.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>HU13</td>
      <td>Visualizar planes disponibles de la plataforma</td>
      <td>Muestra las diferentes opciones de suscripción, costos y características incluidas en cada nivel de servicio.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>HU17</td>
      <td>Visualizar interfaz adaptativa (Mobile)</td>
      <td>Optimización de la experiencia de usuario para que la plataforma sea plenamente funcional en smartphones y tablets.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>HU18</td>
      <td>Cambiar idioma de la plataforma</td>
      <td>Opción de internacionalización que permite alternar la interfaz entre español e inglés según la preferencia del usuario.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>HU19</td>
      <td>Navegación por anclas</td>
      <td>Mejora de la navegación en la landing page mediante enlaces directos a secciones específicas para un acceso más rápido.</td>
      <td>1</td>
    </tr>
  </tbody>
</table>

A continuación, se presenta la versión del sprint en Trello.

<img src="assets/Product-Backlog.png">

Para más detalle, ver el Anexo 4.



