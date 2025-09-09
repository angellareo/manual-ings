# Cascada

```{mermaid}
block-beta 
    columns 6
    A["Análisis"] space space space space space
    space B["Diseño"] space space space space
    space space C["Codificación"] space space space
    space space space D["Pruebas"] space space
    space space space space E["Instalación"] space
    space space space space space F["Mantenimiento"]

    %% Posicionamiento para simular la cascada
    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
```

También conocida como desarrollo secuencial, ordena rigurosamente las etapas del proceso para el desarrollo de software, de tal forma que el inicio de cada etapa debe esperar a la finalización de la etapa anterior. La palabra cascada sugiere, mediante la metáfora de la fuerza de la gravedad, el esfuerzo necesario para introducir un cambio en las fases más avanzadas de un proyecto. La versión original fue propuesta por Winston W. Royce en 1970 y posteriormente revisada, primero, por Barry Boehm en 1980 y, después, por Ian Sommerville en 1985.

Las fases del desarrollo en cascada coinciden con las fases del ciclo de vida del software:
1. Análisis de requisitos.
2. Diseño del sistema.
3. Codificación.
4. Pruebas.
5. Instalación/Despliegue/Operación
6. Mantenimiento.

## Ventajas
1. Fácil de implementar y entender
2. Requiere menos inversión en capital y herramientas para hacerlo funcionar
3. Modelo habitual en contextos de gestión pública.

## Desventajas
1. En la vida real, un proyecto rara vez sigue una secuencia lineal.
2. Entrega demorada: Hasta que el software no esté completo no se opera.
3. Requisitos no detectados aumentan considerablemente los costos del desarrollo, lo que puede derivar en riesgos y fracasos.


# Cascada con iteración
```{mermaid}
block-beta
    columns 6
    A["Análisis"] space space space space space
    space B["Diseño"] space space space space
    space space C["Codificación"] space space space
    space space space D["Pruebas"] space space
    W[" "] X[" "] Y[" "] Z[" "] E["Operación"] space
    space space space space space  F["Mantenimiento"]

    %% Posicionamiento para simular la cascada
    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    E --- W
    W --> A
    E --- X
    X --> B
    E --- Y
    Y --> C
    E --- Z
    Z --> D

    style W height:0px;
    style X height:0px;
    style Y height:0px;
    style Z height:0px;
```

La cascada con iteración es una evolución de la metodología en cascada según la cual, una vez llegada la fase de operación, puede iterarse desde cualquiera de las fases hasta llegar de nuevo a la operación. Sigue siendo un modelo bastante lineal, pero de esta forma los productos finales se van refinando en cada una de las iteraciones.

Las ventajas y desventajas son las mismas que para la cascada, pero se integra el conocimiento de que no es sencillo completar todas las fases en una sola iteración (secuencia no lineal). Esto permite planificar de antemano los costes de iteraciones sucesivas, reduciendo los riesgos.