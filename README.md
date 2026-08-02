# 🧩 MazeAI Pathfinder & Real-World Map Visualizer

[![Django Version](https://img.shields.io/badge/Django-5.1.7-green.svg)](https://www.djangoproject.com/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Live Demo](https://img.shields.io/badge/Live_Site-Render-00d4ff.svg)](https://maze-visualizer.onrender.com/)

**MazeAI Pathfinder** is a modern, web-based interactive platform for visualizing classic graph traversal and shortest-path algorithms. It features two powerful visualizer engines: a **2D Grid Maze Pathfinder** and a **Real-World Interactive Map Visualizer** spanning Indian state road networks.

---

## 🌟 Key Features

### 🧩 1. 2D Grid Maze Visualizer
- **Interactive Grid System**: Dynamically place Start and End nodes, draw obstacles/walls in real-time, or generate random mazes.
- **Multiple Search Algorithms**:
  - 🔍 **Breadth-First Search (BFS)** (Guarantees shortest path for unweighted graphs)
  - 🧭 **Depth-First Search (DFS)** (Explores deep paths first)
  - ⚡ **Dijkstra's Algorithm** (Weighted graph shortest path)
  - 🎯 **A* Search** (Heuristic-guided optimal pathfinding)
  - 🚀 **Greedy Best-First Search** (Fast heuristic search)
  - 🔄 **Bidirectional BFS** (Searches simultaneously from Start and End)
- **Live Algorithm Execution**: Real-time animation of visited cells, path discovery, backtracks, and active frontiers.
- **Interactive Cell Coordinates**: Clear coordinate indicators (`(x,y)`) on cells with high contrast.

---

### 🗺️ 2. Real-World Map Visualizer
- **Geographic Network Pathfinding**: Real-world route calculation across Indian state capitals and major transit nodes powered by **Leaflet.js** and CartoDB Dark basemaps.
- **Route Setup**: Select Source State and Destination State with auto-zoom and animated camera follow mode.
- **Algorithm Comparison Engine**: Compare **A* Search** vs **Dijkstra's Algorithm** side-by-side with live execution charts, states visited metrics, and performance winner declarations.
- **Interactive Step-by-Step Playback**: Pause, step forward, step backward, or scrub through state transitions.

---

### 📊 3. Performance Analytics & Live Data Structures
- **Memory State Inspector**: Real-time stack, queue, and priority queue monitoring showing active memory states during algorithm execution.
- **Pseudocode Execution Box**: Live syntax-highlighted line tracking corresponding to the currently executing step.
- **Path Metrics & Coordinates List**: Full breakdown of steps, path length, visited count, execution time (ms), and exact coordinate sequence.

---

### 🎨 4. Design & User Experience
- **Cyberpunk Dark Mode & Glassmorphism Aesthetic**: Rich HSL glowing cyan themes, glassmorphic cards, and sleek dark modes.
- **Mobile-Responsive**: Fully optimized mobile layouts with auto-scaling grids, mobile-scoped touch scrollbars, and single-column responsive cards.

---

## 🛠️ Technology Stack

- **Backend**: Python 3.10+, Django 5.1.7, Gunicorn, WhiteNoise
- **Frontend**: HTML5, Vanilla CSS3 (Custom Design System with CSS Tokens), JavaScript ES6+
- **Mapping & Icons**: Leaflet.js 1.9.4, FontAwesome 6, Google Fonts (*Orbitron* & *Inter*)
- **Deployment**: Render Web Services (`https://maze-visualizer.onrender.com/`)

---

## 📁 Project Structure

```
maze_visualizer/
├── core/
│   ├── static/
│   │   ├── css/
│   │   │   ├── landing_deep.css  # Landing page stylesheet
│   │   │   ├── maze.css          # 2D Grid visualizer stylesheet
│   │   │   └── map_style.css     # Real-world map visualizer stylesheet
│   │   └── js/
│   │       ├── maze.js           # 2D Maze pathfinding engine & UI
│   │       └── map_data.js       # Map pathfinding engine & Leaflet integration
│   ├── templates/
│   │   ├── global_landing.html   # Main Landing Page
│   │   ├── index.html            # Landing / developer profile
│   │   ├── maze.html             # 2D Grid Visualizer page
│   │   └── map_home.html         # Real-World Map Visualizer page
│   └── views.py                  # Django view handlers
├── maze_visualizer/
│   ├── settings.py               # Django configuration
│   ├── urls.py                   # URL routing
│   └── wsgi.py                   # WSGI deployment entry point
├── build.sh                      # Render build script
├── Procfile                      # Gunicorn process config
├── render.yaml                   # Render deployment manifest
├── requirements.txt              # Python dependencies
└── manage.py                     # Django CLI utility
```

---

## ⚙️ Installation & Local Setup

### Prerequisites
- Python 3.10 or higher
- `pip` (Python package manager)
- `git`

### Step-by-Step Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/rahul9512/maze_visualizer.git
   cd maze_visualizer
   ```

2. **Create and Activate a Virtual Environment**:
   - **Windows**:
     ```bash
     python -m venv venv
     venv\Scripts\activate
     ```
   - **macOS / Linux**:
     ```bash
     python3 -m venv venv
     source venv/bin/activate
     ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run Database Migrations**:
   ```bash
   python manage.py migrate
   ```

5. **Start the Development Server**:
   ```bash
   python manage.py runserver
   ```

6. **Access the App**:
   Open your browser and navigate to `http://127.0.0.1:8000/`.

---

## 🚀 Deployment

The project is configured for one-click deployment on **Render**:

- **Build Command**: `./build.sh` (runs `pip install`, `collectstatic`, and `migrate`)
- **Start Command**: `gunicorn maze_visualizer.wsgi:application`
- **Live URL**: [https://maze-visualizer.onrender.com/](https://maze-visualizer.onrender.com/)

---

## 👤 Developer Profile

Developed with ❤️ by **Rahul Shukla**
- 🌐 **Live Web Application**: [maze-visualizer.onrender.com](https://maze-visualizer.onrender.com/)
- 💻 **GitHub Profile**: [github.com/rahul9512](https://github.com/rahul9512)

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).
