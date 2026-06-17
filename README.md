# 🟡 Pac-Man DFS Maze

> Un clon moderno de **Pac-Man** desarrollado con **HTML5, CSS y JavaScript puro**, donde cada partida ocurre en un laberinto generado proceduralmente mediante el algoritmo **Depth-First Search (DFS)**. Diseñado para **dispositivos móviles y escritorio**, el juego puede instalarse como una **Progressive Web App (PWA)**, permite controlar a Pac-Man mediante **gestos táctiles o las teclas de dirección**, e incluye **tres niveles de dificultad** para adaptar la experiencia de juego.

![DFS](https://img.shields.io/badge/algoritmo-DFS%20Maze-8b5cf6)
![BFS](https://img.shields.io/badge/IA-BFS-ef4444)
![PWA](https://img.shields.io/badge/PWA-instalable-22c55e)
![Controles](https://img.shields.io/badge/controles-Gestos%20%7C%20Flechas-0ea5e9)
![Dificultad](https://img.shields.io/badge/dificultad-Fácil%20%7C%20Normal%20%7C%20Difícil-f97316)
![Stack](https://img.shields.io/badge/stack-HTML5%20Canvas%20JavaScript-f59e0b)
![Dependencias](https://img.shields.io/badge/dependencias-ninguna-16a34a)
![Licencia](https://img.shields.io/badge/licencia-PolyForm%20Noncommercial%201.0.0-blue)

A diferencia del juego original, este proyecto crea un **laberinto único y aleatorio en cada nivel**, ofreciendo una experiencia diferente en cada partida.

## 🎮 Jugar en línea

**Juego completo:** https://gabom88.github.io/pac-man-DFS-maze/

---

## ✨ Características

* 🧩 Generación procedural de laberintos mediante **DFS (Depth-First Search)**.
* 🔄 Cada nivel crea un laberinto completamente nuevo.
* 🌐 Laberintos siempre resolubles, sin zonas aisladas.
* 🔁 Adición de ciclos extra para mejorar la exploración y la jugabilidad.
* 👻 Fantasmas con persecución basada en **BFS (Breadth-First Search)**.
* 📱 Instalación en dispositivos móviles y escritorio como **Progressive Web App (PWA)**.
* 👆 Controles táctiles mediante gestos de deslizamiento (*swipe*).
* ⌨️ Compatibilidad con teclado usando las flechas de dirección y las teclas **WASD**.
* 🎚️ Tres niveles de dificultad: **Fácil, Normal y Difícil**.
* 🎵 Efectos de sonido generados con **Web Audio API**.
* 📶 Funcionamiento sin conexión gracias a **Service Workers**.
* 🚫 Sin dependencias ni frameworks externos.

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
git clone https://github.com/gabom88/pac-man-DFS-maze.git
```

Accede al directorio:

```bash
cd pac-man-DFS-maze
```

Abre `index.html` en tu navegador o utiliza un servidor local:

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
├── index.html
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

Distribuido bajo la licencia **PolyForm Noncommercial 1.0.0**. Su uso está permitido únicamente con **fines no comerciales** (por ejemplo, uso personal, educativo, académico o de investigación).

Consulta el archivo `LICENSE` o visita:

https://polyformproject.org/licenses/noncommercial/1.0.0/

para más detalles.

---

**Copyright © 2026 Gabriel Barradas**
