# Capítulo I: Introducción

## 1.1. Startup Profile

### 1.1.1 Descripción de la Startup

Somos un equipo recientemente formado enfocado en desarrollar una solución tecnológica que responda a una necesidad real: mejorar el cuidado y la seguridad de los recién nacidos, ayudando a detectar a tiempo posibles señales de alerta que muchas veces pasan desapercibidas.

### 1.1.2 Perfiles de integrantes del equipo
| Foto | Apellido y nombre | Código | Carrera | Acerca de |
|------|------------------|--------|----------|------------|
| ![](assets/p5.jpeg) | Retuerto Rodríguez, Jorge Manuel | u202318612 | Ingeniería de Software | Mi nombre es Jorge Manuel Retuerto Rodríguez, tengo 20 años y estoy cursando el 6to ciclo de la carrera de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas. Mi conocimiento y habilidades de programación son intermedias en C++, C#, HTML y CSS. Sin embargo, básicas en Python y Java. Me haré responsable de la comunicación del grupo, planificación y desarrollo junto a mi equipo. |
| ![](assets/p4.jpeg) | Said Conde, Yazid | u202312348 | Ingeniería de Software | Me considero una persona responsable al momento de trabajar en equipo, siempre proactivo y dispuesto a tomar las riendas en situaciones críticas. Me encanta programar y todo el área de desarrollo de software, desarrollo de videojuegos y ciberseguridad en el área de Red Team. Tengo conocimientos en Python, SQL, C++, desarrollo web. Mis conocimientos serán de gran ayuda en el desarrollo del proyecto. |
| ![](assets/p1.jpeg) | Daril Johan Palomino Vilcañaupa | u202317338 | Ingeniería de Software | Soy estudiante de Ingeniería de Software en la UPC. Me considero una persona perseverante y constante, siempre enfocada en superarme día a día para afrontar nuevos desafíos con determinación. Me caracterizo por ser empático y saber trabajar con los demás. Además, disfruto practicar deportes y mantengo un fuerte compromiso con el proyecto y mis objetivos académicos. |
| ![](assets/p3.jpeg) | Mariel Lucero Mendoza Moreano | u20231a418 | Ingeniería de Software | Mi nombre es Mariel Lucero Mendoza Moreano, tengo 20 años y actualmente estudio Ingeniería de Software en la Universidad de Ciencias Aplicadas. Cuento con conocimientos en HTML, CSS y C++, los cuales he ido desarrollando a través de mis estudios y proyectos académicos. Me considero una persona responsable, proactiva y con disposición para colaborar y brindar apoyo cuando se requiere. Además, me interesa aprender constantemente nuevas tecnologías y mejorar mis habilidades para aportar de manera efectiva en proyectos de desarrollo de software. |
| ![](assets/p1.jpeg) | Diego Alonso Véliz Martínez | u20211b564 | Ingeniería de Software | Mi nombre es Diego Alonso Véliz Martínez, tengo 20 años y curso el sexto ciclo de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas. Tengo nivel intermedio en C++, C#, HTML y CSS, y básico en Python y Java. Seré responsable de la comunicación, planificación y desarrollo del proyecto junto a mi equipo. Me considero proactivo, responsable y con iniciativa para liderar en situaciones críticas. Me apasiona el desarrollo de software, especialmente en videojuegos y ciberseguridad, y mis conocimientos en programación y desarrollo web aportarán al éxito del proyecto. |
## 1.2 Solution Profile

El proyecto Sistema Inteligente de Registro y Alerta Neonatal (SIRAN) nace a partir de un problema muy real en el cuidado de recién nacidos: muchas veces las señales de alerta temprana pasan desapercibidas. Esto no ocurre por falta de interés, sino por situaciones comunes como el cansancio de los padres, la falta de experiencia, el desconocimiento de ciertos síntomas o simplemente no llevar un registro ordenado de lo que ocurre día a día. Todos estos factores hacen que sea difícil detectar a tiempo cambios importantes en la salud del bebé, como infecciones o deshidratación, lo que puede retrasar la atención médica en momentos clave. Por eso, el objetivo del proyecto es ayudar a identificar estos riesgos lo antes posible mediante una herramienta que permita registrar y analizar información importante en tiempo real. Como parte del alcance, también se considera que el sistema debe ser fácil de usar, proteger la información personal y adaptarse a estándares médicos.

Como solución, se propone desarrollar una plataforma digital con una base de datos centralizada donde se puedan registrar datos importantes del recién nacido, como su temperatura, peso, alimentación, coloración, entre otros. La idea es que funcione como un tablero de salud inteligente que no solo guarde la información, sino que también la analice automáticamente y avise cuando algo no esté dentro de lo normal. Además, el sistema podrá generar reportes gráficos que faciliten la revisión por parte de médicos. Está pensado tanto para clínicas y pediatras como para padres primerizos, buscando mejorar la toma de decisiones, reaccionar más rápido ante cualquier problema y crear un puente más claro de información entre el hogar y el centro de salud.

### 1.2.1 Antecedentes y problemática

Desarrollo de la preguntas clave usando el modelo 5Ws y 2Hs, importante para la identificar los Antecedentes y problematica.


| Pregunta | Pregunta formulada al problema | Respuesta a la pregunta |
| :--- | :--- | :--- |
| **Who?** | ¿Quiénes son afectados? | <p align ="justify"> Recién nacidos, padres (quienes enfrentan ansiedad y fatiga en el entorno hospitalario), enfermeras y pediatras en unidades neonatales. </p> |
| **What?** | ¿Cuál es el problema? |  <p align ="justify">La pérdida de información crítica entre turnos médicos y el estrés de los padres que, por falta de herramientas técnicas, no pueden comunicar con precisión lo que observan.</p> |
| **When?** | ¿Cuándo se presenta? |<p align ="justify"> Durante la estancia en la clínica, especialmente en las horas de descanso del personal o cuando los padres se quedan a cargo del monitoreo visual en la habitación.</p> |
| **Where?** | ¿Dónde ocurre? | <p align ="justify">En clínicas, hospitales y centros de maternidad, como paso previo y fundamental antes de que el bebé sea dado de alta para ir a casa.</p> |
| **Why?** | ¿Por qué ocurre? | <p align ="justify">Por la alta carga asistencial del personal clínico y el estado emocional de los padres, lo que facilita que síntomas sutiles pasen desapercibidos en los registros manuales.</p> |
| **How?** | ¿Cómo se va a solucionar? | Con una plataforma digital que permite a padres y personal registrar parámetros en tiempo real, validándolos con algoritmos médicos para generar alertas y reportes objetivos. |
| **How much?** | ¿Cuánto impacto tiene? | <p align ="justify">Aumenta la seguridad del paciente, reduce el error humano por agotamiento y brinda tranquilidad a los padres al participar activamente en un cuidado basado en datos. </p>|


### 1.2.2 Lean UX Process

#### 1.2.2.1. Lean UX Problem Statements

#### 1.2.2.2. Lean UX Assumptions

#### 1.2.2.3. Lean UX Hypothesis Statements

#### 1.2.2.4. Lean UX Canvas

## 1.3. Segmentos objetivo