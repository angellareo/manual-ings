# Definición de hitos

En la planificación, no basta con tener una larga lista de tareas. Necesitamos **puntos de referencia** que nos permitan evaluar el progreso y destacar los avances significativos. Estos puntos son los **hitos**, elementos fundamentales para el seguimiento y control del proyecto.

## ¿Qué es un hito?

Un **hito** (o *milestone*) es un punto específico en el tiempo que marca la **consecución de un objetivo clave**. Representa un evento o un estado, no un objeto. Por ejemplo, serían hitos la validación final del Diseño de Arquitectura o la primera integración exitosa.

Es relevante diferenciar los hitos de los entregables. Un entregable es un producto tangible como el Documento de Especificación de Requisitos. Un hito, en cambio, es un punto en el tiempo que indica que se ha alcanzado un objetivo importante, como la finalización de la fase de Análisis. Solo en algunos casos un hito puede coincidir con la validación final de un entregable.

## Técnicas para identificar hitos

Para definir hitos relevantes y bien ubicados en el tiempo, utilizamos técnicas de descomposición y planificación temporal.

- Descomposición de Objetivos del Proyecto (WBS - Work Breakdown Structure): La WBS descompone el trabajo total del proyecto en paquetes de trabajo manejables y jerárquicos. Los hitos naturales surgen al finalizar los paquetes de trabajo de nivel más alto o aquellos que representan un resultado significativo.
- Diagramas de Gantt y Cronogramas: Son herramientas visuales para ubicar los hitos en la línea de tiempo. En un Gantt, los hitos se representan con un símbolo distintivo (como un diamante o un triángulo invertido) y no tienen duración (día específico). La planificación con un Gantt obliga a pensar en las dependencias lógicas: "No podemos alcanzar el Hito 'Diseño Completado' hasta que todas las tareas de diseño estén terminadas y validadas".

## Hitos típicos en proyectos software
- **Fase de Planificación:**
    -   Aprobación del **Acta de Constitución del Proyecto** (*Kick-Off*).
    -   Validación del **Plan de Proyecto** (IEEE 1058).
- **Fase de Análisis:**
    -   Validación del **Documento de Especificación de Requisitos** del software.
- **Fase de Diseño:**
    -   Validación del **Documento de Diseño de Arquitectura (ADS)**. Es un hito crítico, ya que los errores aquí son costosos de corregir después.
- **Fase de Codificación:**
    -   **Primer Prototipo Funcional / Primer Sprint Revisado (en ágil).** Demuestra viabilidad y genera feedback temprano.
    -   **Integración Exitosa de Todos los Módulos / "Code Freeze" (Congelación del Código).** Marca el fin del desarrollo de nuevas funcionalidades y el inicio de la fase de estabilización.
- **Fase de Pruebas/Validación:**
    -   Versión **alfa interna:** Primera versión con todas las funcionalidades principales, para pruebas intensivas internas.
    -   Versión **beta** (*Release to Customers*): Versión entregada a un grupo limitado de usuarios reales para pruebas en su entorno.
- **Fase de Despliegue:**
    -   **Aceptación formal del cliente** (*Customer Sign-Off*).
    -   **Despliegue en producción** (*Go-Live*).
    -   **Cierre oficial del proyecto**.

## Relación de hitos con gestión de riesgos

Los hitos no son solo marcadores de progreso; son **puntos vitales de control para la gestión de riesgos**. Esta relación es bidireccional:

1.  Los hitos como **puntos de revisión de riesgos** (*Risk Checkpoints*):
    *   La consecución de cada hito es el **momento natural para reevaluar el panorama de riesgos** del proyecto. ¿Los riesgos identificados se materializaron? ¿Han aparecido nuevos? ¿Han cambiado las probabilidades o impactos?
    *   La revisión en un hito permite decidir si se **continúa al siguiente hito, se replanifica o incluso se cancela el proyecto** (si los riesgos son inmanejables), minimizando así pérdidas futuras.

2.  Los hitos como **generadores de riesgos**:
    *   **El incumplimiento de un hito es en sí mismo un riesgo (de tipo "cronograma" o "objetivo")** que puede desencadenar otros riesgos (sobrecoste, penalizaciones, pérdida de confianza del cliente).
    *   Un retraso en un hito clave (ej: "Diseño de Arquitectura") suele tener un **efecto dominó** sobre el resto del cronograma, aumentando la presión y la probabilidad de errores posteriores.

3.  Los hitos como objetivos para **mitigar riesgos**:
    *   Podemos definir **hitos intermedios específicos para mitigar riesgos técnicos**. Por ejemplo, si existe el riesgo de que una tecnología nueva no funcione, un hito temprano puede ser "Prototipo de Concepto de la Tecnología X Validado".


````{admonition}Una planificación inteligente de hitos...
transforma un cronograma lineal en una **serie de puertas de control** (*stage-gates*). Cada hito es una oportunidad para **parar, evaluar, aprender y decidir** con información actualizada.
````