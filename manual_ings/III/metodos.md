# Definición de estándares, métodos, técnicas y herramientas

Una vez seleccionado el ciclo de vida, el siguiente paso en la planificación es **establecer el cómo del proyecto**: las tácticas de equipo y los instrumentos de trabajo.

## Estándares

Los estándares son convenciones y normas acordadas que pretenden aseguran la consistencia, la interoperabilidad y la calidad en todos los productos y procesos del proyecto. Proporcionan un lenguaje común y un marco de referencia.

### Normas Internacionales (de *compliance*):
- [**ISO/IEC 12207** - Procesos del Ciclo de Vida del Software](https://es.wikipedia.org/wiki/ISO/IEC_12207): Es el marco de referencia fundamental. Define un conjunto completo de procesos, actividades y tareas aplicables en la adquisición, suministro, desarrollo, operación y mantenimiento de software. Nos ayuda a identificar qué procesos debemos tener.
- **ISO/IEC 25010** - Modelo de Calidad de Producto de Software: Actualiza y detalla las características de calidad (funcionalidad, fiabilidad, usabilidad, eficiencia, mantenibilidad, portabilidad, seguridad, compatibilidad). Nos da el lenguaje para definir nuestros criterios de calidad. La última versión es de 2023. Hablaremos más sobre este estándar en la [sección de aseguramiento de calidad](X/intro.md).

### Estándares internos (de ejecución):
Son protocolos específicos de la organización o del proyecto. Incluyen:
- Guías de estilo de código: Convenciones de nomenclatura, formato y estructura (ej: PEP 8 para Python).
- Estándares de documentación: Plantillas y formatos para requisitos, diseños, informes de pruebas, actas de reunión.
- Protocolos de comunicación: Normas para commits, estructura de emails, formatos de informes.

Los estándares no buscan la rigidez, sino la **eficiencia en la colaboración y el mantenimiento**. Un código escrito bajo un estándar es más fácilmente legible por cualquier miembro del equipo, reduciendo esfuerzos y riesgos.

## Métodos y técnicas

Son las prácticas específicas que se utilizarán en la ejecución de las actividades del proyecto.

- Métodos de **modelado**:
    - **UML (Lenguaje Unificado de Modelado)**: La técnica estándar para visualizar y documentar un sistema software. Se empleará principalmente en las fases de análisis y diseño (Diagramas de Casos de Uso, de Clases, de Secuencia...).
    - **BPMN (Notación de Modelado de Procesos de Negocio)**: Diagramas para modelar procesos de negocio.

- Técnicas de **gestión de requisitos**:
    - **Historias de Usuario**: Descripciones breves y simples de una funcionalidad desde la perspectiva del usuario final: "*Como \[rol], quiero \[objetivo] para \[beneficio]*". . Utilizadas en metodologías ágiles, constituyen la base del backlog.
    - **Casos de Uso**: Técnica más formal y estructurada que describe la interacción entre un actor y el sistema para lograr un objetivo, incluyendo flujos normal y alternativos. Es común en enfoques más tradicionales o para especificar subsistemas críticos.

- Técnicas de **estimación**:
    - **Modelos Paramétricos (COCOMO, Constructive Cost Model)**: Utiliza fórmulas matemáticas basadas en el tamaño del proyecto (líneas de código o puntos de función) y un conjunto de factores de coste (experiencia del equipo, complejidad) para predecir esfuerzo y tiempo. Es útil en fases tempranas y para proyectos con similitudes históricas.
    - **Técnicas de Consenso Ágil (Planning Poker)**: Técnica de estimación colaborativa donde el equipo utiliza barajas con números (usualmente la serie de Fibonacci) para estimar la complejidad relativa de las tareas (historias de usuario). Fomenta la discusión colectiva.
    - **Puntos de función**: Mide la funcionalidad entregada al usuario basándose en los requisitos funcionales. Es independiente del lenguaje de programación y tecnología, lo que lo hace útil para estimaciones tempranas.

- Técnicas de **aseguramiento de calidad**:
    - **Revisiones por pares**: Evaluaciones sistemáticas del trabajo de un colega para identificar defectos y áreas de mejora.
    - **Pruebas automatizadas**: Uso de frameworks (JUnit, Selenium) para ejecutar pruebas repetitivas y garantizar la estabilidad del software.

## Herramientas

Son el soporte tecnológico que automatiza, facilita y controla la ejecución de los métodos bajo los estándares definidos.

- **Control de versiones**: **Git** es el estándar de facto. Permite gestionar cambios en el código fuente, trabajar en ramas paralelas, fusionar trabajo y mantener un historial completo. Además, plataformas como **GitHub, GitLab o Gitea** añaden gestión de repositorios, revisión de código y CI/CD.
- **Gestión de proyectos y de colaboración**: Herramientas que permiten planificar, asignar y monitorear tareas, facilitando la colaboración y visibilidad del progreso.
    - **Jira**: Popular en entornos ágiles, permite gestionar sprints, historias de usuario y tareas.
    - **OpenProject**: Herramienta de código abierto para gestión de proyectos con soporte para metodologías ágiles y tradicionales.
    - **Trello**: Basado en tableros Kanban, es ideal para equipos pequeños y proyectos menos complejos.
- **Integración continua y despliegue continuo (CI/CD)**: Automatizan la construcción, prueba y despliegue del software.
    - **Jenkins**: Plataforma de automatización extensible para CI/CD.
    - **GitLab CI/CD**: Integrada en GitHub, permite definir flujos de trabajo automatizados.
- **Entornos de desarrollo integrado (IDE)**: Facilitan la escritura, depuración y prueba del código.
- **Gestión de la documentación**: Herramientas para crear, organizar y mantener la documentación del proyecto.
    - **Confluence**: Plataforma colaborativa para documentar requisitos, diseños y decisiones.
    - **MkDocs**: Generador de sitios estáticos para documentación técnica basado en Markdown.

Definir estos elementos durante la planificación es una inversión estratégica que permite al equipo centrar su energía en lo que realmente importa: construir software de valor.

````{important}
La selección adecuada de estándares, métodos, técnicas y herramientas permite establecer un **entorno de trabajo unificado**: un ecosistema predecible y repetible donde cualquier miembro del equipo puede trabajar de manera eficiente.
````