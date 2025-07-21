# Espiral

```{mermaid}
flowchart TD
    Inicio([Inicio]) --> Planificacion[Planificación]
    Planificacion --> Analisis[Análisis de riesgos]
    Analisis --> Desarrollo[Desarrollo y validación]
    Desarrollo --> Evaluacion[Evaluación del cliente]
    Evaluacion --> Decidir{¿Continuar?}
    Decidir -- Sí --> Planificacion
    Decidir -- No --> Fin([Fin])

    %% Opcional: estilos para resaltar el ciclo
    style Planificacion fill:#e3f2fd,stroke:#2196f3,stroke-width:2px
    style Analisis fill:#fffde7,stroke:#fbc02d,stroke-width:2px
    style Desarrollo fill:#e8f5e9,stroke:#43a047,stroke-width:2px
    style Evaluacion fill:#fce4ec,stroke:#d81b60,stroke-width:2px
```

La metodología en espiral prioriza la gestión de riesgos. Está basado en ciclos de planificación, desarrollo, evaluación y gestión de riesgos. Estos ciclos se repiten hasta lograr un sistema estable. 

No hay producto operativo hasta el final y está especialmente recomendado para el desarrollo de software crítico como sistemas aeroespaciales, bancarios o médicos donde la seguridad es prioritaria.

