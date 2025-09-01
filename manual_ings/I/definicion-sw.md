# ¿Qué es el software?

Podemos definir el software como un conjunto de tres elementos:
1. **Programa**: Un listado de instrucciones codificadas de modo que, cuando son ejecutadas por un procesador, realizan una serie de operaciones para la obtención de un resultado.
2. **Datos**: Estructurados en modo tal que permiten que el código lo transforme de la manera deseada para la obtención del resultado.
3. **Documentación**: Información descriptiva, en formato de texto u otro, que describen las operaciones, los usos y los resultados esperados por un programa.

`````{admonition} Definición de Software
:class: tip
Software = Programa + Datos + Documentación
`````

El software es un **elemento lógico**, no físico. Por tanto, es **desarrollado** y no fabricado. Aunque cada vez más (gracias a la aplicación de la ingeniería del software) se avanza hacia diseños modulares, con componentes reutilizables, la mayor parte del software **se diseña a medida**. Además, el software está sujeto a actualizaciones (en seguridad o infraestructura), a avances sociales y cambios legislativos o, incluso, a modas estéticas. Como consecuencia, el software **se deteriora**. Decimos, por ello, que el software es un **proceso vivo** y en **constante evolución**.

## Tipos de software

Podemos dividir los tipos de software en siete grandes categorías en función de sus características.
- **Software embebido o incrustado**: Entrarían dentro de este grupo los controladores de dispositivos hardware que implementan funciones y características específicas del dispositivo. Normalmente programados en lenguajes de bajo nivel.
- **Software de sistemas**: Programas que dan servicio a otros programas. Algunos de estos programas procesan entradas deterministas, como los compiladores. Otro software de sistemas trabaja con entradas no determinista, como las implementaciones de protocolos de red o los componentes de un sistema operativo.[^1]
- **Software de análisis de datos en ingeniería y ciencia**: Implementaciones de algoritmos para el tratamiento de grandes cantidades de datos, con un alto coste computacional, para la simulación de procesos en distintas áreas de la ciencia y la ingeniería. Al tratarse de cómputos altamente complejos, en el borde de lo que resulta factible computar, tradicionalmente este software no se ha operado de manera interactiva. Implementaciones modernas donde este tipo de datos se procesan en tiempo real toman características del software de aplicación o de sistemas.
- **Software de aplicación**: Programas aislados que resuelven una necesidad genérica aplicable en campos variados (el diseño, el ocio o la ofimática) y ofrecido para el uso de muchos actores diferentes. Por razones que abarcan desde la compatibilidad al modelo de negocio de las desarrolladoras, cada vez más encontramos versiones web de este tipo de software.
- **Software de gestión**: e trata de programas aislados que resuelven necesidades específicas para una entidad, cubriendo una función que está íntimamente relacionada con las características de la propia entidad. Incluye aplicaciones de contabilidad o recursos, de gestión de personal, de participación de ciudadanos o usuarios y otros. En ocasiones se trata de variantes variantes específicas del software de aplicación aplicada en la gestión de una entidad. De nuevo, cada vez encontramos más versiones web de este software.
- **Aplicaciones web**: Se trata de software de aplicación y de gestión que opera de manera remota a través de la web. Mediante el navegador web se construye la interfaz de la aplicación (lo que se ha venido a llamar *frontend*), mientras el grueso de la lógica de trabajo se encuentra en servidores (*backend*).
- **Software de aprendizaje automático**: Popularmente conocido como inteligencia artificial, es un tipo de software no desarrollado: sus respuestas no son programadas de manera explícita o directa, sino que emergen a partir de conjunto inicial de reglas cuyos parametros se ajustan (*entrenamiento*) utilizando un proceso estadístico sobre un gran conjunto de datos.

Además de las versiones cerradas comerciales suelen existir versiones libres o abiertas de cualquiera de estos tipos de software (aunque la definición de software libre en el caso del software de aprendizaje automático está aún por definirse). 

[^1]: El software es *determinista* si es posible predecir el orden y momento de las entradas, el procesamiento y las salidas. El software es *no determinista* si no pueden predecirse el orden y momento en que ocurren éstos