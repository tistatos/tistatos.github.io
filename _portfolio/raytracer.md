---
layout: portfolio
title:  Raytracer
short: A Global illumination raytracer done in the course TNCG15
github_name: TNCG15-ray-tracer
permalink: /portfolio/raytracer/
image_url: /assets/big3h.png
---

# Raytracer
I made this raytracer individually in the course TNCG15: Advanced global illumination.

The raytracer has support for sphere and triangle intersection. It also includes reflective and
refractive surfaces. The surfaces are implemented with Lambertian BRDF as well as with Oren-Nayar. The raytracer uses Monte Carlo method to determine how the radiance is propagated within the scene. Each pixel is sampled with multiple subpixel samples with a randomized direction. The shadows in the scene is implemented with shadow rays to create the area light effect.

The raytracer uses OpenMP to make the rendering loop parallel.
