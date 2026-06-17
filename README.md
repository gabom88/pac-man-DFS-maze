# 🟡 Pac-Man DFS Maze

Un clon moderno de **Pac-Man** desarrollado con **HTML5, CSS y JavaScript puro**, donde cada partida ocurre en un laberinto generado proceduralmente mediante el algoritmo **Depth-First Search (DFS)**.

A diferencia del juego original, este proyecto crea un **laberinto único y aleatorio en cada nivel**, ofreciendo una experiencia diferente en cada partida.

## 🎮 Jugar en línea

Prueba el juego aquí:

**🔗 Demo:** *Agrega aquí la URL de GitHub Pages*

---

## ✨ Características

* 🧩 Generación procedural de laberintos.
* 🔄 Cada nivel es completamente diferente.
* 🌐 Algoritmo DFS para garantizar laberintos siempre resolubles.
* 🔁 Adición de ciclos extra para mejorar la jugabilidad.
* 👻 Fantasmas con persecución basada en búsqueda de rutas (BFS).
* 📱 Compatible con dispositivos móviles y escritorio.
* 🎵 Efectos de sonido generados con Web Audio API.
* 📶 Funciona como aplicación web progresiva (PWA).
* 🎚️ Tres niveles de dificultad.

---

## 🧠 El corazón del proyecto: DFS Maze Generation

La característica principal del juego es su sistema de generación de laberintos basado en el algoritmo **Depth-First Search (DFS)**, también conocido como **Recursive Backtracking**.

Este algoritmo permite crear **laberintos perfectos**, es decir:

* Existe un camino entre cualquier par de celdas.
* No hay zonas inaccesibles o aisladas.
* No existen ciclos durante la generación inicial.
* Cada laberinto es único.

### ¿Cómo funciona?

1. Se crea una cuadrícula completamente llena de muros.
2. Se marcan las celdas impares como posibles caminos.
3. Se selecciona una celda inicial.
4. El algoritmo explora aleatoriamente las celdas vecinas no visitadas.
5. Al avanzar, elimina los muros intermedios para crear corredores.
6. Cuando llega a un callejón sin salida, retrocede utilizando una pila (*stack*).
7. El proceso continúa hasta visitar todas las celdas.

```text
Inicio → Explorar → Sin vecinos disponibles → Retroceder → Continuar
```

Este enfoque garantiza que el laberinto siempre sea resoluble y tenga una estructura orgánica e impredecible.

---

## 🔄 Mejora de la jugabilidad: creación de ciclos

Aunque un laberinto perfecto es interesante desde el punto de vista algorítmico, puede resultar demasiado lineal para un juego de persecución como Pac-Man.

Por ello, después de generar el laberinto con DFS, el proyecto agrega conexiones adicionales entre corredores:

* Se identifican muros candidatos.
* Se elimina un porcentaje de ellos de forma aleatoria.
* Se crean rutas alternativas y atajos.

El resultado es un equilibrio entre:

* 🧠 Exploración estratégica.
* 👻 Persecuciones más dinámicas.
* 🔀 Mayor rejugabilidad.

---

## 👾 Inteligencia de los fantasmas

Los fantasmas utilizan el algoritmo **Breadth-First Search (BFS)** para encontrar la ruta más corta hacia Pac-Man.

La combinación de:

* **DFS** para generar el entorno.
* **BFS** para navegarlo.

crea una experiencia desafiante y diferente en cada partida.

---

## 🛠️ Tecnologías utilizadas

* HTML5 Canvas
* CSS3
* JavaScript (ES6+)
* Web Audio API
* Service Workers
* Progressive Web App (PWA)

---

## 🚀 Ejecutar localmente

Clona el repositorio:

```bash
git clone https://github.com/tu-usuario/pac-man-dfs-maze.git
```

Accede al directorio:

```bash
cd pac-man-dfs-maze
```

Abre `pac-man.html` en tu navegador o utiliza un servidor local:

```bash
python -m http.server
```

Luego visita:

```text
http://localhost:8000
```

---

## 📂 Estructura del proyecto

```text
├── index.html (pac- man)
├── sw.js
├── manifest.webmanifest
├── icon-180.png
├── icon-192.png
└── icon-512.png
```

---

## 📚 Algoritmos implementados

| Algoritmo                  | Función                     |
| -------------------------- | --------------------------- |
| DFS (Depth-First Search)   | Generación del laberinto    |
| BFS (Breadth-First Search) | Navegación de los fantasmas |
| Fisher-Yates Shuffle       | Aleatorización de vecinos   |

---

## 📄 Licencia

Este proyecto es de código abierto y está disponible bajo la licencia que el autor decida incorporar.

---

Desarrollado por **Gabriel M.**
