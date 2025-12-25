## Ejemplos de cálculo de la complejidad ciclomática

### Ejemplo 1: Función simple con una decisión

```{code-block} c
:linenos:
int max(int a, int b) {
    if (a > b)
        return a;
    else
        return b;
}
```

Vamos a calcular la complejidad ciclomática de esta función instrucción a instrucción, mostrando el grafo de control de flujo correspondiente. Cada línea de código, identificada por el número de línea, se representa como un nodo en el grafo. El flujo se representa como una arista dirigida en el grafo.

```{raw} html
<!-- Slider -->
<div style="display: flex; flex-direction: column; align-items: center;">
    <div>
        <label for="slider">Paso: </label>
        <input type="range" id="slider" min="1" max="5" value="1" />
    </div>
    <div>
        <!-- Grafo -->
        <svg id="graph" width="500" height="300"></svg>

        <!-- Cálculo -->
        <p style="text-align:center;" id="complexity">Complejidad ciclomática: 1</p>
    </div>

<!-- Script D3.js -->
<script src="https://d3js.org/d3.v7.min.js"></script>
<script>
const svg = d3.select("#graph");
const width = +svg.attr("width");
const height = +svg.attr("height");

// Nodos del grafo (simplificado): cada uno referencia líneas del código
const nodes = [
  {id: 0, label: "1"},
  {id: 1, label: "2"},
  {id: 2, label: "3"},
  {id: 3, label: "4,5"},
  {id: 4, label: "6"},
];

// Posiciones fijas
nodes[0].x = width/2; nodes[0].y = 40;
nodes[1].x = width/2; nodes[1].y = 100;
nodes[2].x = width/2 - 100; nodes[2].y = 150;
nodes[3].x = width/2 + 100; nodes[3].y = 150;
nodes[4].x = width/2; nodes[4].y = 200;

// Todas las aristas posibles (simplificado)
const allEdges = [
  {source: 0, target: 1},
  {source: 1, target: 2}, // True branch
  {source: 1, target: 3}, // False branch
  {source: 2, target: 4},
  {source: 3, target: 4},
];

// Función para calcular complejidad ciclomática: M = E - N + 2P
function calcComplexity(edges, nodes, P=1) {
  return edges.length - nodes.length + 2*P;
}

// Función para actualizar grafo según paso
function updateGraph(step) {
  svg.selectAll("*").remove(); // limpiar

  // según paso, mostrar más aristas y nodos
  let edges = [];
  let usedNodes = [];
  if (step == 1) {
    usedNodes = [nodes[0]];
    edges = [];
  } else if (step == 2) {
    usedNodes = [nodes[0], nodes[1]];
    edges = [allEdges[0]];
  } else if (step == 3) {
    usedNodes = [nodes[0], nodes[1], nodes[2]];
    edges = [allEdges[0], allEdges[1]];
  } else if (step == 4) {
    usedNodes = [nodes[0], nodes[1], nodes[2], nodes[3]];
    edges = [allEdges[0], allEdges[1], allEdges[2]];
  } else {
    usedNodes = nodes;
    edges = allEdges;
  }

  // dibujar aristas
  svg.selectAll("line")
    .data(edges)
    .enter()
    .append("line")
    .attr("x1", d => nodes[d.source].x)
    .attr("y1", d => nodes[d.source].y)
    .attr("x2", d => nodes[d.target].x)
    .attr("y2", d => nodes[d.target].y)
    .attr("stroke", "black")
    .attr("stroke-width", 2);

  // dibujar flechas en el medio de las aristas
  svg.selectAll("polygon")
    .data(edges)
    .enter()
    .append("polygon")
    .attr("points", d => {
      const x1 = nodes[d.source].x;
      const y1 = nodes[d.source].y;
      const x2 = nodes[d.target].x;
      const y2 = nodes[d.target].y;
      // Punto medio
      const mx = (x1 + x2) / 2;
      const my = (y1 + y2) / 2;
      // Ángulo de la línea
      const angle = Math.atan2(y2 - y1, x2 - x1);
      // Tamaño de la flecha
      const arrowSize = 8;
      // Calcular los tres puntos del triángulo
      const p1x = mx + arrowSize * Math.cos(angle);
      const p1y = my + arrowSize * Math.sin(angle);
      const p2x = mx + arrowSize * Math.cos(angle + 2.5);
      const p2y = my + arrowSize * Math.sin(angle + 2.5);
      const p3x = mx + arrowSize * Math.cos(angle - 2.5);
      const p3y = my + arrowSize * Math.sin(angle - 2.5);
      return `${p1x},${p1y} ${p2x},${p2y} ${p3x},${p3y}`;
    })
    .attr("fill", "black");

  // dibujar nodos
  svg.selectAll("circle")
    .data(usedNodes)
    .enter()
    .append("circle")
    .attr("cx", d => d.x)
    .attr("cy", d => d.y)
    .attr("r", 20)
    .attr("fill", "lightblue");

  // etiquetas
  svg.selectAll("text")
    .data(usedNodes)
    .enter()
    .append("text")
    .attr("x", d => d.x)
    .attr("y", d => d.y + 4)
    .attr("text-anchor", "middle")
    .text(d => d.label)
    .style("font-size", "10px");

  // actualizar complejidad
  const M = calcComplexity(edges, usedNodes);
  document.getElementById("complexity").innerText = "Complejidad ciclomática: M = E - N + 2 = " + M;
}

// inicial
updateGraph(1);

// evento slider
document.getElementById("slider").addEventListener("input", e => {
  updateGraph(+e.target.value);
});
</script>
```


### Ejemplo 2: Función con bucle y múltiples decisiones

```{code-block} c
:linenos:
int classify(int score) {
    if (score >= 90)
        return 'A';
    else if (score >= 80)
        return 'B';
    else if (score >= 70)
        return 'C';
    else {
        for (int i = 0; i < score; i++) {
            if (i % 2 == 0)
                continue;
        }
        return 'D';
    }
}
```

```{raw} html
<!-- Slider -->
<div style="display: flex; flex-direction: column; align-items: center;">
    <div>
        <label for="slider2">Paso: </label> 
        <input type="range" id="slider2" min="1" max="10" value="1" />
    </div>
    <div>
        <!-- Grafo -->
        <svg id="graph2" width="600" height="550"></svg>
        <!-- Cálculo -->
        <p style="text-align:center;" id="complexity2">Complejidad ciclomática: 1</p>
    </div>
<!-- Script D3.js -->
<script src="https://d3js.org/d3.v7.min.js"></script>
<script>
const svg2 = d3.select("#graph2");
const width2 = +svg2.attr("width");
const height2 = +svg2.attr("height");

// Nodos del grafo (simplificado): cada uno referencia líneas del código
const nodes2 = [
  {id: 0, label: "1"},
  {id: 1, label: "2"},
  {id: 2, label: "3"},
  {id: 3, label: "4"},
  {id: 4, label: "5"},
  {id: 5, label: "6"},
  {id: 6, label: "7"},
  {id: 7, label: "8,9"},
  {id: 8, label: "10"},
  {id: 9, label: "11"},
  {id: 10, label: "12"},
  {id: 11, label: "13"},
];

// Posiciones fijas
nodes2[0].x = width2/2; nodes2[0].y = 40;
nodes2[1].x = width2/2; nodes2[1].y = 100;
nodes2[2].x = width2/2 - 150; nodes2[2].y = 150;
nodes2[3].x = width2/2; nodes2[3].y = 150;
nodes2[4].x = width2/2 + 150; nodes2[4].y = 150;
nodes2[5].x = width2/2; nodes2[5].y = 200;
nodes2[6].x = width2/2 - 100; nodes2[6].y = 250;
nodes2[7].x = width2/2; nodes2[7].y = 250;
nodes2[8].x = width2/2; nodes2[8].y = 300;
nodes2[9].x = width2/2; nodes2[9].y = 350;
nodes2[10].x = width2/2 + 100; nodes2[10].y = 400;
nodes2[11].x = width2/2 - 100; nodes2[11].y = 400;

// Todas las aristas posibles (simplificado)
const allEdges2 = [
  {source: 0, target: 1},
  {source: 1, target: 2}, // score >= 90
  {source: 1, target: 3}, // score >= 80
  {source: 3, target: 4}, // score >= 70
  {source: 3, target: 5}, // else
  {source: 5, target: 6}, 
  {source: 5, target: 7}, // for loop start
  {source: 7, target: 8}, // if (i % 2 == 0)
  {source: 7, target: 11}, // return D
  {source: 8, target: 9}, // continue
  {source: 9, target: 10}, // end for loop
  {source: 8, target: 10}, // not enter if
  {source: 10, target: 7}, // back to for loop
];

// Función para calcular complejidad ciclomática: M = E - N + 2P
function calcComplexity2(edges, nodes, P=1) {
  return edges.length - nodes.length + 2*P;
}

// Función para actualizar grafo según paso
function updateGraph2(step) {
  svg2.selectAll("*").remove(); // limpiar
  // según paso, mostrar más aristas y nodos
  let edges = [];
  let usedNodes = [];
  if (step == 1) {
    usedNodes = [nodes2[0]];
    edges = [];
  } else if (step == 2) {
    usedNodes = [nodes2[0], nodes2[1]];
    edges = [allEdges2[0]];
  } else if (step == 3) {
    usedNodes = [nodes2[0], nodes2[1], nodes2[2]];
    edges = [allEdges2[0], allEdges2[1]];
  } else if (step == 4) {
    usedNodes = [nodes2[0], nodes2[1], nodes2[2], nodes2[3]];
    edges = [allEdges2[0], allEdges2[1], allEdges2[2]];
  } else if (step == 5) {
    usedNodes = [nodes2[0], nodes2[1], nodes2[2], nodes2[3], nodes2[4]];
    edges = [allEdges2[0], allEdges2[1], allEdges2[2], allEdges2[3]];
  } else if (step == 6) {
    usedNodes = [nodes2[0], nodes2[1], nodes2[2], nodes2[3], nodes2[4], nodes2[5], nodes2[6]];
    edges = [allEdges2[0], allEdges2[1], allEdges2[2], allEdges2[3], allEdges2[4], allEdges2[5]];
  } else if (step == 7) {
    usedNodes = [nodes2[0], nodes2[1], nodes2[2], nodes2[3], nodes2[4], nodes2[5], nodes2[6], nodes2[7]];
    edges = [allEdges2[0], allEdges2[1], allEdges2[2], allEdges2[3], allEdges2[4], allEdges2[5], allEdges2[6]];
  } else if (step == 8) {
    usedNodes = [nodes2[0], nodes2[1], nodes2[2], nodes2[3], nodes2[4], nodes2[5], nodes2[6], nodes2[7], nodes2[8]];
    edges = [allEdges2[0], allEdges2[1], allEdges2[2], allEdges2[3], allEdges2[4], allEdges2[5], allEdges2[6], allEdges2[7]];
  } else if (step == 9) {
    usedNodes = [nodes2[0], nodes2[1], nodes2[2], nodes2[3], nodes2[4], nodes2[5], nodes2[6], nodes2[7], nodes2[8], nodes2[9], nodes2[11]];
    edges = [allEdges2[0], allEdges2[1], allEdges2[2], allEdges2[3], allEdges2[4], allEdges2[5], allEdges2[6], allEdges2[7], allEdges2[8], allEdges2[9]];
  } else if (step == 9) {
    usedNodes = [nodes2[0], nodes2[1], nodes2[2], nodes2[3], nodes2[4], nodes2[5], nodes2[6], nodes2[7], nodes2[8], nodes2[9], nodes2[10], nodes2[11]];
    edges = [allEdges2[0], allEdges2[1], allEdges2[2], allEdges2[3], allEdges2[4], allEdges2[5], allEdges2[6], allEdges2[7], allEdges2[8], allEdges2[9], allEdges2[10], allEdges2[11], allEdges2[12]];
  } else {  
    usedNodes = nodes2;
    edges = allEdges2;
  }

  // dibujar aristas
  svg2.selectAll("line")
    .data(edges)
    .enter()
    .append("line")
    .attr("x1", d => nodes2[d.source].x)
    .attr("y1", d => nodes2[d.source].y)
    .attr("x2", d => nodes2[d.target].x)
    .attr("y2", d => nodes2[d.target].y)
    .attr("stroke", "black")
    .attr("stroke-width", 2);

  // dibujar flechas en el medio de las aristas
  svg2.selectAll("polygon")
    .data(edges)
    .enter()
    .append("polygon")
    .attr("points", d => {
      const x1 = nodes2[d.source].x;
      const y1 = nodes2[d.source].y;
      const x2 = nodes2[d.target].x;
      const y2 = nodes2[d.target].y;
      // Punto medio
      const mx = (x1 + x2) / 2;
      const my = (y1 + y2) / 2;
      // Ángulo de la línea
      const angle = Math.atan2(y2 - y1, x2 - x1);
      // Tamaño de la flecha
      const arrowSize = 8;
      // Calcular los tres puntos del triángulo
      const p1x = mx + arrowSize * Math.cos(angle);
      const p1y = my + arrowSize * Math.sin(angle);
      const p2x = mx + arrowSize * Math.cos(angle + 2.5);
      const p2y = my + arrowSize * Math.sin(angle + 2.5);
      const p3x = mx + arrowSize * Math.cos(angle - 2.5);
      const p3y = my + arrowSize * Math.sin(angle - 2.5);
      return `${p1x},${p1y} ${p2x},${p2y} ${p3x},${p3y}`;
    })
    .attr("fill", "black");

  // dibujar nodos
  svg2.selectAll("circle")
    .data(usedNodes)
    .enter()
    .append("circle")
    .attr("cx", d => d.x)
    .attr("cy", d => d.y)
    .attr("r", 20)
    .attr("fill", "lightblue");

  // etiquetas
  svg2.selectAll("text")
    .data(usedNodes)
    .enter()
    .append("text")
    .attr("x", d => d.x)
    .attr("y", d => d.y + 4)
    .attr("text-anchor", "middle")
    .text(d => d.label)
    .style("font-size", "10px");

  const M = calcComplexity2(edges, usedNodes);
  document.getElementById("complexity2").innerText = "Complejidad ciclomática: M = E - N + 2 = " + M;
}
// inicial
updateGraph2(1);
// evento slider
document.getElementById("slider2").addEventListener("input", e => {
  updateGraph2(+e.target.value);
});
</script>
```
  