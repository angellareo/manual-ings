# Introducción

## Proceso software

El **proceso software** o **proceso de desarrollo de software** es el conjunto coherente de actividades ordenadas que se destinan a producir un sistema software. Como sabemos, el objetivo de la Ingeniería del Software ha sido, desde sus inicios, estudiar y optimizar este proceso software.

De acuerdo al [estándar ISO/IEC 12207](https://es.wikipedia.org/wiki/ISO/IEC_12207), todos los procesos software deben incorporar **cuatro tipos de actividad** fundamentales:
- ```{dropdown} Actividades de acuerdo
    Son actividades **de acuerdo** aquellas que implican a varias organizaciones. Incluye actividades relacionadas con el establecimiento de un acuerdo entre un proveedor y un cliente, como son la adquisición y el suministro de software.

- ```{dropdown} Actividades organizativas habilitantes de proyectos
    Son actividades **organizativas habilitantes de proyectos** aquellas relacionadas con la propia organización desarrolladora y sus proyectos. Incluye las actividades de gestión de procesos, la cartera de proyectos, la asignación de recursos (infraestructura, recursos humanos, conocimiento) y el aseguramiento de la calidad en los procesos.
    ```

- ```{dropdown} Actividades de gestión y control
    Actividades referidas a un proyecto específico e incluyen tareas como:

        - Evaluación y control de proyectos.
        - Gestión de decisiones.
        - Gestión de riesgos.
        - Gestión de configuraciones.
        - Gestión de la información.
        - Proceso de garantía de calidad.
    ```

- ```{dropdown} Actividades técnicas
    Son actividades también referidas al proyecto e incluyen tareas como:

        - Análisis de los requisitos del software.
        - Diseño de la arquitectura del software.
        - Diseño detallado del software.
        - Construcción del software.
        - Integración del software.
        - Pruebas del software.
        - Integración del sistema.
        - Pruebas del software.
    ```

Históricamente, se ha dividido el **proceso software** en **6 fases** más una fase inicial de planificación, lo que se conoce como **ciclo de vida software**:
- 0. Planificación y actividades tempranas
- 1. Análisis
- 2. Diseño
- 3. Codificación
- 4. Pruebas
- 5. Despliegue
- 6. Mantenimiento

Como hemos visto, existe una gran variedad de sistemas software (drivers de dispositivos, aplicaciones móviles o web, suites de ofimática o diseño...). Por ello, aunque uno de los objetivos de la Ingeniería del Software era unificar criterios para convertir el desarrollo de software en un proceso industrial universalizable, lo cierto es que no existe un proceso software aplicable a todos los casos. Es responsabilidad del Ingeniero de Software establecer la metodología más apropiado a utilizar en un determinado proyecto.

Para poder decidir de manera informada qué metodología de desarrollo de software escoger, debemos conocer los distintos tipos existentes, así como sus ventajas e inconvenientes.

%%HTML
<div align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/SaCYkPD4_K0?si=FXcYf4mYAJkTJxF5" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

## Metodologías de desarrollo de software
Una **metodología** es el conjunto de métodos que se utilizan en una determinada actividad con el fin de formalizarla y optimizarla. De modo que una **metodología de proceso software** determina los pasos a seguir, su orden y cómo realizarlos para optimizar el proceso y el producto software.

Cualquier proceso software implica una serie de fases ordenadas. Denominamos **ciclo de vida** al *conjunto de fases* por las que pasa el software desde que nace la idea inicial hasta que el software es retirado o reemplazado. En cada **fase** tienen lugar una serie de **actividades** que permiten convertir los **elementos de entrada** de dicha fase en los **elementos de salida**.

Así pues, el ciclo de vida determina las **fases** del proceso software. No obstante, cuando describimos una metodología, además de ordenar el ciclo de vida (sus fases y actividades), es también importante describir:
- **quién** está involucrado en cada fase y sus **responsabilidades**.
- las **entradas** y **salidas** de cada fase.
- **qué condiciones** o **criterios** influencian la secuencia de actividades.

Todos estos aspectos describen una **metodología de proceso software** o **modelo de proceso software**. Existen [multitud de metodologías para el desarrollo de software](https://es.wikipedia.org/wiki/Lenguaje_unificado_de_modelado). Algunas son guías generales, mientras que otras definen el proceso de desarrollo de manera muy concreta. En este libro hemos dividido las metodologías a estudiar en 3 grupos:
- ```{dropdown} Metodologías tradicionales
    - [Cascada](tradicionales/cascada.md)
    - [Incremental](tradicionales/incremental.md)
    - [Iterativa](tradicionales/iterativa.md)
    - [Incremental-Iterativa](tradicionales/incremental-it.md)
    - [Espiral](tradicionales/espiral.md)
    - [Metrica v.3](tradicionales/metricav3.md)
    ```
- ```{dropdown} Metodologías ágiles
    - [SCRUM](agiles/scrum.md)
    - [eXtreme Programming (XP)](agiles/xp.md)
    - [Lean](agiles/lean.md)
    - [Kanban](agiles/kanban.md)
    ```
- ```{dropdown} Metodologías emergentes:
    - DevOps.
    - Guiadas por pruebas.
    - Centradas en el usuario.
    ```