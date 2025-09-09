# Metodologías ágiles

En 2001, un grupo de destacados desarrolladores de software firmaron el [«Manifiesto para el desarrollo ágil de software»](https://agilemanifesto.org/iso/es/manifesto.html), en el que defendían 
> **Individuos e interacciones** sobre procesos y herramientas
> **Software funcionando** sobre documentación extensiva
> **Colaboración con el cliente** sobre negociación contractual
> **Respuesta ante el cambio** sobre seguir un plan

Sus propuestas, también conocidas como **Agile** son un [conjunto de principios](https://agilemanifesto.org/iso/es/principles.html) que promueven la entrega iterativa, incremental y evolutiva de software, la colaboración con el cliente y la capacidad de adaptación a cambios.

Agile no es en sí mismo, por tanto, una metodología, sino un marco conceptual para guiar metodologías y prácticas ligeras para el desarrollo de software. Algunas de las metodologías más relevantes que implementan las metodologías ágiles son [SCRUM](./agiles/scrum.md), [eXtreme Programming (XP)](./agiles/xp.md), [Kanban](./agiles/kanban.md) o [Lean]((./agiles/lean.md)). La Agile Alliance mantiene un [Glosario Agile](https://agilealliance.org/agile101/agile-glossary/),​ un compendio de código abierto y en constante evolución de las definiciones funcionales de las prácticas, términos y elementos ágiles, junto con interpretaciones y directrices sobre experiencias de la comunidad mundial de profesionales de Agile.
<!--**XP** es una metodología ágil con un fuerte enfoque en técnicas de programación, mientras que **Lean** busca eliminar desperdicios y maximizar la eficiencia en los procesos de desarrollo. Por otro lado, **Design Sprint** es un enfoque intensivo para diseñar y validar soluciones rápidamente dentro de las metodologías ágiles. -->



## Metodologías ágiles

Un resumen de sus diferencias:
| Enfoque | Propósito Principal | Características Clave | Diferencia Principal |
|---------|---------------------|----------------------|---------------------|
| **SCRUM** | Metodología ágil basada en iteraciones y roles definidos | Sprints, roles (Scrum Master, Product Owner, Dev Team), reuniones diarias | Enfoque estructurado con ciclos de trabajo fijos (Sprints) |
| **Kanban** | Método visual para gestionar el flujo de trabajo | Tableros visuales, enfoque en el flujo continuo, Work In Progress (WIP) limitado | No tiene iteraciones fijas, optimiza la entrega continua |
| **XP** | Metodología ágil centrada en calidad de código | TDD, programación en pareja, integración continua | Metodología concreta con énfasis en prácticas técnicas |
| **Lean Software Development** | Optimización de procesos de desarrollo | Eliminación de desperdicios, eficiencia, aprendizaje continuo | Enfocado en optimización y eficiencia, más que en iteraciones |


## Referencias

[Manifiesto por el Desarrollo Ágil de Software](https://agilemanifesto.org/iso/es/manifesto.html)

<!-- 
## LEAN Software Development
## Design Sprint
## Agile

## Ejercicios 

1. Supón que estás desarrollando una aplicación de cálculo matemático en la que necesitas implementar una función `es_primo(n)` que determine si un número es primo. Siguiendo el enfoque de XP y TDD, realiza los siguientes pasos:  

    1. Escribe una primera prueba unitaria para verificar el comportamiento esperado de `es_primo(n)`.  
    2. Implementa la función con el código mínimo necesario para pasar la prueba.  
    3. Refactoriza el código si es necesario, asegurándote de mantener todas las pruebas exitosas.  
    4. Agrega nuevas pruebas para más casos de uso y repite el ciclo.  

Puedes usar cualquier lenguaje de programación, pero se recomienda Python o Java con frameworks de pruebas como `pytest` o `JUnit`. -->