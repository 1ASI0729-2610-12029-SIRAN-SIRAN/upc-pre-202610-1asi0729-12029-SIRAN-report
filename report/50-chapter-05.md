# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

### 5.1.1. Software Development Environment Configuration

A continuación, se detallan las soluciones tecnológicas empleadas en el desarrollo de SIRAN. Estas herramientas fueron fundamentales para gestionar el diseño, la organización del equipo, el control de versiones y el despliegue del sistema.

- **Herramientas para UX/UI Design**
  - Figma: Herramienta principal para el desarrollo de prototipos de alta fidelidad. 
  - Canva: Plataforma para la colaboración de diseños de exposiciones.
  - Miro: Utilizado para el diseño del Design Event Storming.

- **Editor de Código (IDE)**
  - Visual Studio Code: Entorno de desarrollo sin lincencia, usado por parte de los miembros por interfaces simples.
  - WebStorm: Entorno de desarrollo que soporta HTML, CSS y TypeScript, usado por los miembros por aumento de eficiencia por herramientas como el 'Generator'.
  - IntelliJ IDEA: Entorno de desarrollo de Java, no se usa aún.

- **Gestión de versiones y repositorios**
  - Git: Herramienta de control de versiones locales.
  - GitHub: Herramientas de control de versiones remotas, asimismo, añade gráficos para la validación de trabajo de los miembros. 

- **Herramientas de despliegue y Framework**
  - Angular: Framework para el desarrollo próximo del Front End y Landing Page, aún sin uso real.
  - GitHub Pages: Proveedor vinculado a GitHub para el Deploy de Landing Page.

Adicionalmente, se adoptó la metodología GitFlow para gestionar el flujo de trabajo y garantizar una distribución eficiente de las tareas. Asimismo, se implementó el estándar de Conventional Commits, asegurando un historial de cambios profesional, semántico y detallado

### 5.1.2. Source Code Management

La gestión del código fuente se centralizó en GitHub, plataforma que facilitó el alojamiento remoto del proyecto y garantizó un control de versiones riguroso. En el *Anexo 2* se detalla el acceso a la organización del proyecto y la estructura de sus repositorios.

Reglas impuestas en el proyecto:

- Los roles distribuidos entre los miembros serán limitados para que no ajusten las reglas de la organización.
- Ningún miembro puede hacer un push a la rama principal, sin antes pasar por un Pull Request.
- Se trabaja en las ramas feature para luego hacer un merge en la rama de desarrollo.
- Para la creación de tablas, debido a limitaciones de Markdown, se recomienda el uso de HTML para mantener consistencia.

### 5.1.3. Source Code Style Guide & Conventions

Por un lado, siguiendo la metodología de GitFlow hemos adoptado el trabajo de ramas:

- main: rama principal, representa el proyecto que esta en producción. Por ello, presenta cambios solamente cuando ya paso una revisión.
- develop: rama de desarrollo, representa donde se hará el desarrollo del proyecto antes de pasar a producción.
- release: rama que es el paso previo a la producción, se verifica que todo el código este correcto y no haya errores.
- feature: rama efímera, se usa para agregar caracteristicas a la rama develop. Cuando el develop se fusiona con la rama, debe pasar a borrarse.
- hotfix: rama de emergencia, busca solucionar cualquier error que haya pasado el filtro del release.

Por otro lado, con la finalidad de generar commits descriptivos y limpios. Hemos seguido los 'Conventional Commits' para la documentación:

- feat: caracteristicas agregadas al sistema.
- docs: cambios generados en el informe.
- fix: arreglo de errores que podría lanzar el sistema.
- refactor: cambios de estructura sin romper o cambiar la lógica ya creada.
- chore: estructuración del contenido en el entorno de desarrollo.

Finalmente, la notación de archivos se hará usando ***Kebab-Case***, para el nombre de nuestras entidades u objetos usaremos ***CamelCase***.

### 5.1.4. Software Deployment Configuration

En esta sección, se describe la configuración del software para el despliegue en la nube.

- Configuración para el despliegue de Landing Page:
  - Se uso GitHub Pages para el despliegue del Lading Page.
  - Se llevo todo el contenido a la rama main, pues se simula que esta en producción.
  - Se configuró GitHub Pages para que haga lectura de la rama main.

Siguiendo esa configuración, logramos el despligue de nuestra Landing Page. Veasé el Anexo 3 para acceder al Lading Page.

## 5.2. Landing Page, Services & Applications Implementation

### 5.2.1. Sprint 1

#### 5.2.1.1. Sprint Planning 1

#### 5.2.1.2. Aspect Leaders and Collaborators

#### 5.2.1.3. Sprint Backlog 1

#### 5.2.1.4. Development Evidence for Sprint Review

#### 5.2.1.5. Execution Evidence for Sprint Review

#### 5.2.1.6. Services Documentation Evidence for Sprint Review

#### 5.2.1.7. Software Deployment Evidence for Sprint Review

#### 5.2.1.8. Team Collaboration Insights during Sprint