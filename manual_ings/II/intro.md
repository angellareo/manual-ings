# Introducción

## Proceso software

El **proceso software** o **proceso de desarrollo de software** es el conjunto coherente de actividades ordenadas que se destinan a producir un sistema software. Como sabemos, el objetivo de la Ingeniería del Software ha sido, desde sus inicios, estudiar y optimizar este proceso software.

De acuerdo con el estándar **IEEE 1074-2006** (que adopta y se alinea con [ISO/IEC 12207](https://es.wikipedia.org/wiki/ISO/IEC_12207)), las actividades para el ciclo de vida del software se organizan en **cinco categorías principales**:

```{dropdown} 1. Gestión del proyecto (Project Management)
Actividades para iniciar, monitorear y controlar un proyecto de software a lo largo de todo su ciclo de vida.
- **Iniciación del proyecto:**
    - Desarrollar el ciclo de vida del proyecto software (CVPS) (Requerido)
    - Realizar estimaciones (Requerido)
    - Asignar recursos del proyecto (Requerido)
    - Definir métricas (Requerido)
    - Determinar objetivos de seguridad (Requerido)
- **Planificación del proyecto:**
    - Planificar evaluaciones (Requerido)
    - Planificar la gestión de configuración (Requerido)
    - Planificar la transición del sistema (si aplica)
    - Planificar la instalación
    - Planificar la documentación (Requerido)
    - Planificar la capacitación
    - Planificar la gestión del proyecto (Requerido)
    - Planificar la integración
    - Planificar la gestión de lanzamientos
- **Monitoreo y control del proyecto:**
    - Gestionar riesgos (Requerido)
    - Gestionar el proyecto (Requerido)
    - Identificar necesidades de mejora del CVPS (Requerido)
    - Retener registros (Requerido)
    - Recopilar y analizar datos de métricas (Requerido)
    - Cerrar el proyecto (Requerido)
```

```{dropdown} 2. Pre-desarrollo (Pre-Development)
Actividades que exploran y asignan los requisitos del sistema antes de que comience el desarrollo del software.
- **Exploración de conceptos:**
    - Identificar ideas o necesidades (Requerido)
    - Formular enfoques potenciales (Requerido)
    - Realizar estudios de factibilidad (Requerido)
    - Refinar y finalizar la idea o necesidad (Requerido)
- **Asignación del sistema:**
    - Analizar las funciones del sistema
    - Desarrollar la arquitectura del sistema
    - Asignar los requisitos del sistema
- **Importación de software:**
    - Identificar requisitos de software importado
    - Evaluar fuentes de importación de software
    - Definir el método de importación de software
    - Importar software
```

```{dropdown} 3. Desarrollo (Development)
Actividades realizadas durante el desarrollo y mejora del proyecto de software.
- **Requisitos del software:**
    - Definir y desarrollar los requisitos del software
    - Definir los requisitos de interfaz
    - Priorizar e integrar los requisitos del software
- **Diseño:**
    - Realizar el diseño arquitectónico
    - Diseñar la base de datos (si aplica)
    - Diseñar las interfaces
    - Realizar el diseño detallado
- **Implementación:**
    - Crear código ejecutable
    - Crear la documentación de operación
    - Realizar la integración
    - Gestionar los lanzamientos de software
```

```{dropdown} 4. Post-desarrollo (Post-Development)
Actividades para instalar, operar, dar soporte, mantener y retirar un producto software.
- **Instalación:**
    - Distribuir el software
    - Instalar el software
    - Aceptar el software en el entorno operativo
- **Operación y soporte:**
    - Operar el sistema
    - Proporcionar asistencia técnica y consultoría
    - Mantener el registro de solicitudes de soporte
- **Mantenimiento:**
    - Identificar necesidades de mejora del software
    - Implementar el método de reporte de problemas
    - Reaplicar el CVPS
- **Retiro:**
    - Notificar al usuario
    - Realizar operaciones en paralelo (si aplica)
    - Retirar el sistema
```

```{dropdown} 5. Soporte (Support)
Actividades transversales necesarias para completar con éxito las funciones del proyecto y asegurar su calidad.
- **Evaluación:**
    - Realizar revisiones (Requerido)
    - Crear la matriz de trazabilidad
    - Realizar auditorías
    - Desarrollar procedimientos de prueba
    - Crear datos de prueba
    - Ejecutar pruebas
    - Reportar resultados de la evaluación (Requerido)
    - Confirmar la acreditación de seguridad (Requerido)
- **Gestión de la configuración del software:**
    - Desarrollar la identificación de la configuración (Requerido)
    - Realizar el control de configuración (Requerido)
    - Realizar el estado de cuentas de configuración (Requerido)
- **Desarrollo de documentación:**
    - Implementar la documentación (Requerido)
    - Producir y distribuir la documentación (Requerido)
- **Capacitación:**
    - Desarrollar materiales de capacitación
    - Validar el programa de capacitación
    - Implementar el programa de capacitación
```

Históricamente, se ha dividido el **proceso software** en **6 fases** (más una fase inicial de planificación), lo que se conoce como **ciclo de vida del proyecto software** (CVPS, o SDLC por sus siglas en inglés: Software Development Life Cycle). Estas fases son:
- 0. Planificación (actividades tempranas en el desarrollo de software)
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
    - [DevOps](emergentes/devops.md).
    - [Guiadas por pruebas](emergentes/tdd.md).
    - [Centradas en el usuario](emergentes/user-centered.md).
    ```

## Objetivos de aprendizaje
Al finalizar este tema, el estudiante será capaz de:
- Definir **qué es un proceso software** y sus actividades fundamentales.
- Explicar las **fases del ciclo de vida** software.
- Diferenciar entre las distintas **metodologías** de desarrollo de software.
- Analizar las **ventajas** e **inconvenientes** de las distintas metodologías de desarrollo de software.
- Analizar y **seleccionar el modelo de ciclo de vida** adecuado para un proyecto de software.
