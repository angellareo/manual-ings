# Ingeniería de la Usabilidad

La **Ingeniería de la Usabilidad** es una metodología de desarrollo de software que prioriza la experiencia del usuario a lo largo de todo el proceso de diseño y construcción del sistema. Su objetivo es garantizar que los productos sean eficientes, intuitivos y accesibles, minimizando errores y maximizando la satisfacción del usuario.  

Se basa en la premisa de que la usabilidad no es un atributo que se añade al final del desarrollo, sino un aspecto fundamental que debe guiar el diseño desde el principio. Para ello, involucra a los usuarios en todas las fases del proceso, aplicando métodos de evaluación y pruebas iterativas.  

## Heurísticas de usabilidad de Nielsen

Supone la primera enumeración de las actividades necesarias para ser capaces de desarrollar sistemas interactivos con la componente usabilidad (y consecuentemente los usuarios) en el centro del problema. Nielsen propuso los **10 principios heurísticos** para evaluar interfaces:

1. **Visibilidad del estado del sistema**: el sistema siempre debe mantener informados a los usuarios sobre lo que está sucediendo, a través de comentarios apropiados dentro de un tiempo razonable.

2. **Relación entre el sistema y el mundo real**: el sistema debe hablar el idioma de los usuarios, con palabras, frases y conceptos familiares para el usuario, en lugar de términos orientados al sistema. Siga las convenciones del mundo real, haciendo que la información aparezca en un orden natural y lógico.

3. **Libertad y control por parte del usuario**: hay ocasiones en que los usuarios elegirán las funciones del sistema por error y necesitarán una “salida de emergencia” claramente marcada para dejar el estado no deseado al que accedieron, sin tener que pasar por una serie de pasos. Se deben apoyar las funciones de deshacer y rehacer.

4. **Consistencia y estándares**: los usuarios no deberían cuestionarse si acciones, situaciones o palabras diferentes significan en realidad la misma cosa; siga las convenciones establecidas.

5. **Prevención de errores**: mucho mejor que un buen diseño de mensajes de error es realizar un diseño cuidadoso que prevenga la ocurrencia de problemas.

6. **Reconocimiento antes que recuerdo**: se deben hacer visibles los objetos, acciones y opciones, El usuario no tendría que recordar la información que se le da en una parte del proceso, para seguir adelante. Las instrucciones para el uso del sistema deben estar a la vista o ser fácilmente recuperables cuando sea necesario.

7. **Flexibilidad y eficiencia de uso**: la presencia de aceleradores, que no son vistos por los usuarios novatos, puede ofrecer una interacción más rápida a los usuarios expertos que la que el sistema puede proveer a los usuarios de todo tipo. Se debe permitir que los usuarios adapte el sistema para usos frecuentes.

8. **Estética y diseño minimalista**: los diálogos no deben contener información que es irrelevante o poco usada. Cada unidad extra de información en un diálogo, compite con las unidades de información relevante y disminuye su visibilidad relativa.

9. **Ayudar a los usuarios a reconocer**: diagnosticar y recuperarse de errores: los mensajes de error se deben entregar en un lenguaje claro y simple, indicando en forma precisa el problema y sugerir una solución constructiva al problema.

10. **Ayuda y documentación**: incluso en los casos en que el sistema pueda ser usado sin documentación, podría ser necesario ofrecer ayuda y documentación. Dicha información debería ser fácil de buscar, estar enfocada en las tareas del usuario, con una lista concreta de pasos a desarrollar y no ser demasiado extensa.

## **Fases y Ciclo de Vida**  
La Ingeniería de la Usabilidad sigue un **ciclo de vida iterativo**, con fases interdependientes que aseguran la optimización continua del producto. Sus principales fases son:  

1. **Análisis de usuarios y contexto**  
   - Identificación de usuarios finales y sus características.  
   - Análisis de tareas y entorno de uso del sistema.  
   - Definición de requisitos de usabilidad.  

2. **Diseño conceptual**  
   - Creación de prototipos de baja fidelidad (bocetos, wireframes).  
   - Establecimiento de la arquitectura de la información.  
   - Diseño de la interacción y flujo de tareas.  

3. **Desarrollo del prototipo**  
   - Implementación de prototipos funcionales iterativos.  
   - Aplicación de principios de diseño centrado en el usuario.  
   - Inclusión de accesibilidad y estándares de usabilidad.  

4. **Evaluación de usabilidad**  
   - Pruebas con usuarios reales mediante test de usabilidad.  
   - Evaluaciones heurísticas (ej., principios de Nielsen).  
   - Recopilación de métricas de usabilidad (tiempo de tarea, tasa de éxito, satisfacción).  

5. **Iteración y refinamiento**  
   - Análisis de resultados de las pruebas y ajuste del diseño.  
   - Optimización del sistema en base a retroalimentación.  
   - Repetición del ciclo hasta alcanzar los objetivos de usabilidad.  

## **Ventajas**  
- **Mejor experiencia de usuario**: Diseños más intuitivos y accesibles.  
- **Reducción de errores**: Minimiza problemas de interacción antes del lanzamiento.  
- **Mayor eficiencia en tareas**: Permite a los usuarios realizar acciones más rápido.  
- **Menor curva de aprendizaje**: Interfaces más fáciles de entender.  
- **Ahorro en costos a largo plazo**: Reduce cambios y soporte técnico post-desarrollo.  

## **Desventajas**  
- **Mayor tiempo de desarrollo**: Implica iteraciones constantes.  
- **Requiere recursos adicionales**: Se necesita involucrar usuarios y realizar pruebas.  
- **Difícil de aplicar en proyectos con requisitos rígidos**: No es adecuada para entornos muy estructurados.  
- **Posibles conflictos con otras prioridades**: Puede generar tensiones con objetivos de negocio o costos.  

#### **Ejercicio**  
**Título**: Análisis y mejora de la usabilidad de una aplicación existente  

**Enunciado:**  

## Referencias

- Nielsen, J. (1994). Usability Engineering. Morgan Kaufmann.
- Nielsen, J. (1993). Usability Heuristics for User Interface Design.
- Norman, D. (2013). *The Design of Everyday Things*. Basic Books.  
- ISO 9241-210:2019. *Human-centred design for interactive systems*. 

<!-- 
## Ejercicios

### 1
- Selecciona una aplicación web de uso común (por ejemplo, una tienda en línea, un portal de noticias o un sistema de reservas).
- Evalúa su interfaz utilizando al menos 5 de los 10 principios heurísticos de Nielsen.
- Identifica tres problemas de usabilidad y propón mejoras basadas en los principios de usabilidad.
- Explica cómo estas mejoras impactarían en la experiencia del usuario.

### 2
Escoge una aplicación de uso cotidiano (por ejemplo, una app móvil o una página web). Realiza un análisis de usabilidad basado en los siguientes pasos:  
1. **Identifica tres problemas de usabilidad** presentes en la interfaz.  
2. **Clasifica cada problema según los atributos de usabilidad** (aprendizaje, eficiencia, memorabilidad, errores o satisfacción).  
3. **Propón mejoras concretas** para solucionar estos problemas.  
4. **Explica cómo evaluarías si las mejoras implementadas realmente mejoran la experiencia del usuario**.  
-->