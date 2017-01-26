---
layout: portfolio
title:  Supersonic Sunshine
short: An implementation of Linear Transformed Cosine.
github_name: supersonic-sunshine
permalink: /portfolio/supersonicsunshine/
image_url: /assets/supersonic.png
rank: 2
---

# Supersonic Sunshine
Supersonic Sunshine was a project made in the course TSBK03: Advance Game Programming.
The project is an implementation of Real-time polygonal-light shading with Linear
Transformed Cosine(LTC) proposed by Heitz et al.

The idea behind the LTCs is to use linear transforms on a BRDF distribution that has a known
analytical solution. By pre-computing the transforms for difference view angles and surface
roughness, the LTC can be retrieved in real-time without the need of numerical methods. This
achieves specular highlights from area lights with resonable frame rates.

The implementation was done in OpenGL.
