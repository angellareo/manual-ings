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

También se llama desarrollo secuencial. Ordena rigurosamente las etapas del proceso para el desarrollo de software, de tal forma que el inicio de cada etapa debe esperar a la finalización de la etapa anterior. La palabra cascada sugiere, mediante la metáfora de la fuerza de la gravedad, el esfuerzo necesario para introducir un cambio en las fases más avanzadas de un proyecto. La versión original fue propuesta por Winston W. Royce en 1970 y posteriormente revisada por Barry Boehm en 1980 e Ian Sommerville en 1985.

Fases:
1. Análisis de requisitos.
2. Diseño del sistema.
3. Codificación.
4. Pruebas.
5. Despliegue del programa.
6. Mantenimiento.

## Ventajas
1. Fácil de implementar y entender
2. Bien conocido y utilizado con frecuencia
3. Requiere menos inversión en capital y herramientas para hacerlo funcionar
4. Buen funcionamiento en equipos débiles y productos maduros

## Desventajas
1. En la vida real, un proyecto rara vez sigue una secuencia lineal.
2. Hasta que el software no esté completo no se opera.
3. Requisitos no detectados: aumentan los costos del desarrollo.

