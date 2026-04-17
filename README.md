# 🐍 Snake Game 2D

A classic Snake game implementation using vanilla JavaScript, HTML5 Canvas, and CSS. No external libraries for game logic.

![Snake Game Screenshot](https://user-images.githubusercontent.com/82943826/235201219-c93b5e4e-0e6a-4d1f-86d7-2eb24f30243d.png)

---

## ENG

### Prerequisites

- Node.js (any recent version)
- npm
- A modern browser with HTML5 Canvas support

### How to run

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/snake-game-2d.git

# 2. Enter the project directory
cd snake-game-2d

# 3. Install dependencies
npm install

# 4. Start the local server
npm start

# 5. Open the game in your browser
#    Navigate to http://localhost:8080
```

### How to play

- **Arrow keys** — control the snake's direction
- **Goal** — eat the red food to grow longer and earn points
- **Avoid** — walls, static obstacles, and the snake's own body
- **Difficulty** — the game speeds up every 3 points

### Core classes

| Class   | Responsibility                                     |
| ------- | -------------------------------------------------- |
| `Snake` | Body segments, color, direction, growth            |
| `Food`  | Random grid-aligned positioning                    |
| `Walls` | Static obstacle layout                             |
| `Cell`  | Basic grid primitive                               |
| `Game`  | Engine, game loop, scoring, state management       |

### Tech stack

- **Frontend:** HTML5, CSS3, JavaScript (ES6+)
- **Rendering:** HTML5 Canvas
- **Dev server:** Node.js with `http-server`
- **Runtime dependencies:** none for the game logic

### Customization

The game can be tuned by editing:

- Canvas dimensions
- Snake initial speed and growth rate
- Obstacle layout in the `Walls` class
- Difficulty curve (score threshold, speed decrement)
- Visual styling via CSS


---


## ITA

### Panoramica

Remake browser del classico gioco arcade Snake. 

### Prerequisiti

- Node.js (qualsiasi versione recente)
- npm
- Un browser moderno con supporto HTML5 Canvas

### Come eseguirlo

```bash
# 1. Clona il repository
git clone https://github.com/yourusername/snake-game-2d.git

# 2. Entra nella directory del progetto
cd snake-game-2d

# 3. Installa le dipendenze
npm install

# 4. Avvia il server locale
npm start

# 5. Apri il gioco nel browser
#    Vai su http://localhost:8080
```

### Come giocare

- **Frecce direzionali** — controllano la direzione dello snake
- **Obiettivo** — mangia il cibo rosso per crescere e guadagnare punti
- **Evita** — muri, ostacoli statici e il corpo dello snake stesso
- **Difficoltà** — il gioco accelera ogni 3 punti

### Classi principali

| Classe  | Responsabilità                                     |
| ------- | -------------------------------------------------- |
| `Snake` | Segmenti del corpo, colore, direzione, crescita    |
| `Food`  | Posizionamento casuale allineato alla griglia      |
| `Walls` | Disposizione degli ostacoli statici                |
| `Cell`  | Primitiva di base della griglia                    |
| `Game`  | Motore, game loop, punteggio, gestione dello stato |

### Stack tecnico

- **Frontend:** HTML5, CSS3, JavaScript (ES6+)
- **Rendering:** HTML5 Canvas
- **Server di sviluppo:** Node.js con `http-server`
- **Dipendenze a runtime:** nessuna per la logica di gioco

### Personalizzazione

Il gioco può essere regolato modificando:

- Dimensioni del canvas
- Velocità iniziale e tasso di crescita dello snake
- Layout degli ostacoli nella classe `Walls`
- Curva di difficoltà (soglia di punteggio, decremento di velocità)
- Stile visivo tramite CSS
