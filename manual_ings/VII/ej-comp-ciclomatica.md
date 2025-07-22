## Ejemplo de cálculo de la complejidad ciclomática

```{code-block} c
:linenos:
int max(int a, int b) {
    if (a > b)
        return a;
    else
        return b;
}
```

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
  {id: 3, label: "5"},
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
    .attr("stroke", "black");

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
