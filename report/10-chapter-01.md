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
| **Who?** | ¿Quiénes son afectados? |  Recién nacidos, padres (quienes enfrentan ansiedad y fatiga en el entorno hospitalario), enfermeras y pediatras en unidades neonatales.  |
| **What?** | ¿Cuál es el problema? |  La pérdida de información crítica entre turnos médicos y el estrés de los padres que, por falta de herramientas técnicas, no pueden comunicar con precisión lo que observan. |
| **When?** | ¿Cuándo se presenta? | Durante la estancia en la clínica, especialmente en las horas de descanso del personal o cuando los padres se quedan a cargo del monitoreo visual en la habitación. |
| **Where?** | ¿Dónde ocurre? | En clínicas, hospitales y centros de maternidad, como paso previo y fundamental antes de que el bebé sea dado de alta para ir a casa. |
| **Why?** | ¿Por qué ocurre? | Por la alta carga asistencial del personal clínico y el estado emocional de los padres, lo que facilita que síntomas sutiles pasen desapercibidos en los registros manuales. |
| **How?** | ¿Cómo se va a solucionar? | Con una plataforma digital que permite a padres y personal registrar parámetros en tiempo real, validándolos con algoritmos médicos para generar alertas y reportes objetivos. |
| **How much?** | ¿Cuánto impacto tiene? | Aumenta la seguridad del paciente, reduce el error humano por agotamiento y brinda tranquilidad a los padres al participar activamente en un cuidado basado en datos. |


### 1.2.2 Lean UX Process

#### 1.2.2.1. Lean UX Problem Statements

El monitoreo neonatal durante la hospitalización de recién nacidos permite el seguimiento de su estado de salud por parte del personal médico, mientras que los padres dependen de la información que se les comunica para comprender la evolución del bebé.

Hemos observado un factor crítico que afecta la experiencia durante este proceso: el acceso limitado a información clara, continua y oportuna sobre el estado del recién nacido. Actualmente, tanto los padres como los profesionales médicos no siempre cuentan con una visión integral y fácilmente accesible del estado del bebé en todo momento.

¿Cómo mejorar la eficacia del monitoreo neonatal logrando que los padres registren información de manera constante y precisa, y que el personal de salud reciba datos confiables en tiempo real, para detectar señales de alerta temprana y actuar oportunamente, garantizando así la seguridad y bienestar del recién nacido y la satisfacción con el servicio?


#### 1.2.2.2. Lean UX Assumptions

User Assumption 

| # | Suposición |
|---|------------|
| 1 |  Los usuarios principales son pediatras, neonatólogos y personal de salud que monitorean recién nacidos, así como padres o cuidadores (especialmente primerizos) que necesitan apoyo para seguir la salud del bebé en casa.  |
| 2 |  Los usuarios tienen dificultad para identificar señales de alerta debido al cansancio, falta de experiencia y miedo a equivocarse.  |
| 3 |  Los usuarios necesitan funcionalidades como monitoreo sencillo (alimentación, sueño, temperatura, llanto), alertas inteligentes, registro guiado, interfaz simple y recomendaciones claras.  |
| 4 |  El producto encaja en la rutina diaria del monitoreo del recién nacido, tanto en entornos clínicos como en el hogar.  |
| 5 |  El producto será usado de forma continua en momentos clave como después de la alimentación, durante el descanso o ante cambios en el comportamiento del bebé, mediante un dashboard simple.  |
| 6 |  Los usuarios prefieren un sistema visualmente tranquilo, simple, confiable y que no genere estrés adicional.  |
| 7 |  Los usuarios necesitan una forma confiable y sencilla de monitorear la salud del bebé sin depender solo de su intuición o memoria.  |
| 8 |  Los usuarios valoran beneficios adicionales como tranquilidad, reducción de ansiedad, mejor comunicación con médicos e historial claro del bebé.  |
| 9 |  El valor principal que buscan es seguridad y tranquilidad al saber que su bebé está bien.  |
| 10 |  Estas necesidades pueden resolverse con una app intuitiva que combine registro de datos, análisis inteligente y alertas claras.  |
---

Business Assumptions

| # | Suposición |
|---|------------|
| 1 | Los centros de salud y el personal médico estarán dispuestos a adoptar esta tecnología dentro de sus procesos de monitoreo neonatal.|
| 2 |  Si los profesionales de salud no adoptan el sistema, el proyecto perderá gran parte de su valor.  |
| 3 |  La solución será un sistema inteligente que registre datos del bebé y genere alertas tempranas basadas en patrones y cambios relevantes.  |
| 4 |  Existe el riesgo de que los usuarios perciban el sistema como complicado o innecesario y dejen de usarlo.  |
| 5 |  La competencia incluye apps de seguimiento de bebés, consultas pediátricas tradicionales e información informal como internet o recomendaciones familiares.  |
| 6 |  La ventaja competitiva será el enfoque en prevención y alertas inteligentes, no solo en el registro de datos.  |
| 7 |  El modelo de negocio se basará en suscripciones premium, servicios adicionales y alianzas con clínicas.  |
| 8 |  Los clientes serán adquiridos mediante redes sociales, recomendaciones médicas y marketing digital.  |
| 9 |  Los clientes iniciales serán centros de salud con áreas neonatales, su personal médico y padres primerizos.  |


#### 1.2.2.3. Lean UX Hypothesis Statements

### **Hipótesis 1 – Registro de datos**


Creemos que si los padres pueden registrar fácilmente información diaria del bebé (alimentación, sueño, temperatura, etc.),  
entonces podrán identificar mejor cambios o comportamientos inusuales,  
sabremos que esto es cierto cuando al menos el 70% de los usuarios registre datos de forma constante durante la primera semana.


---

### **Hipótesis 2 – Alertas tempranas**


Creemos que si el sistema genera alertas automáticas ante posibles señales de riesgo,  
entonces los padres reaccionarán más rápido ante situaciones importantes,  
sabremos que esto es cierto cuando los usuarios respondan o revisen las alertas en menos de 5 minutos en la mayoría de los casos.


---

### **Hipótesis 3 – Reducción de ansiedad**


Creemos que si los padres reciben orientación clara y acompañamiento mediante la app,  
entonces se sentirán más seguros y menos ansiosos en el cuidado del recién nacido,  
sabremos que esto es cierto cuando al menos el 60% de los usuarios reporten una mejora en su tranquilidad o confianza.


---

### **Hipótesis 4 – Facilidad de uso**


Creemos que si la aplicación tiene una interfaz simple e intuitiva,  
entonces los usuarios la utilizarán de forma continua,  
sabremos que esto es cierto cuando más del 75% de los usuarios activos regresen a usar la app diariamente.


---

### **Hipótesis 5 – Valor para profesionales de salud**


Creemos que si los datos registrados pueden compartirse con profesionales de salud,  
entonces estos podrán tomar decisiones más informadas,  
sabremos que esto es cierto cuando profesionales indiquen que la información les resulta útil en al menos el 50% de los casos.


---

### **Hipótesis 6 – Modelo de negocio**

Creemos que si ofrecemos funciones avanzadas (como análisis inteligente o seguimiento detallado),  
entonces algunos usuarios estarán dispuestos a pagar por estas características,  
sabremos que esto es cierto cuando al menos el 20% de los usuarios activos considere o adquiera una versión premium.



#### 1.2.2.4. Lean UX Canvas

![LeanUXCanva](assets/LeanUXCanva.png)

## 1.3. Segmentos objetivo

### **Pediatras y Especialistas Neonatales**


Este segmento está compuesto por profesionales de la salud que realizan el seguimiento ambulatorio o de control del recién nacido. Son un objetivo clave porque el SIRAN resuelve su mayor punto de dolor: la toma de decisiones basadas en relatos subjetivos, incompletos o sesgados por la ansiedad de los padres.  

El proyecto se dirige a ellos porque necesitan optimizar el tiempo de consulta y contar con evidencia paramétrica (gráficos y tendencias) para diagnosticar con precisión infecciones, deshidratación o problemas de crecimiento, transformando la consulta de una charla anecdótica a un análisis técnico de datos reales.


---

### **Padres primerizos y jóvenes con acceso a tecnología**


El segmento objetivo está compuesto por padres primerizos y jóvenes que cuentan con acceso y familiaridad con la tecnología, ya que combinan la necesidad de orientación en el cuidado del recién nacido con la disposición a usar herramientas digitales. Este grupo suele enfrentar inseguridad y falta de experiencia, por lo que requiere apoyo práctico y accesible. SIRAN se adapta a sus hábitos tecnológicos para brindarles monitoreo, organización y alertas en tiempo real.

