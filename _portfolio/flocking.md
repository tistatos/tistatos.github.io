---
layout: portfolio
title:  Flocking algorithm
short: basic implementation of flocking algorithm in OpenGL
image_url: /assets/flocking.png
github_name: flocking
permalink: /portfolio/flocking/
---

A quick implementation of boid flocking algorithm in OpenGL.

Flocking behaviour depends on three simple rules for each boid:

1. *Separation* - Avoid crowding neighbours.
2. *Alignment* - Steer towards the average heading of neighbours.
3. *Cohesion* - Steer towards average position of neighbours.

It's still not perfect, the weighing of the rules could still need some tweaking.