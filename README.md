# Murmur

**Version: v0.11**

**Murmur** is an interactive playground for exploring the beauty of collective motion. Abstract wing and fin silhouettes move according to three simple local rules: separation, alignment, and cohesion.

## Run

Open `index.html` in a modern browser. No build step or installation is required. Google Fonts is optional; system fonts work offline.

Alternatively, serve this directory:

```sh
python -m http.server 8000
```

Then open http://localhost:8000.

## Play

- Attract, repel, or swirl the flock with your pointer or touch.
- Release more birds into the simulation.
- Try Murmuration, Schooling, Wild & free, or Orbital presets.
- Adjust separation, alignment, cohesion, speed, and population.
- Toggle luminous trails and the explanatory math overlay.
- Enter the immersive flock view or save a PNG of the canvas.
- Press Space to pause, R to reset, and Escape to exit the immersive view.

## The math

Each bird senses nearby neighbors. Separation pushes away from close neighbors; alignment steers toward their average velocity; cohesion steers toward their average position. Weighted steering vectors change velocity, then velocity changes position. The edges wrap around.

The page includes plain-language explanations and a visual inspection mode showing one bird's neighborhood and steering contributions. Inspired by Craig Reynolds' Boids model.

## Implementation

A single HTML file contains the interface, styles, and Canvas 2D simulation. A spatial grid limits neighbor searches. No runtime JavaScript libraries or backend are required.
