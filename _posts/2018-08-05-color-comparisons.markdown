---
layout: post
title:  Comparing Colors
description: "How do you know if two colors are close to each other on the color wheel? Is it better to use RGB, HSV or ...."
date:   2018-08-05 11:33:23 +0100
permalink: color_comparisons
---
Let's say you have two colors to compare in order to determine if they are close to each other on the color wheel.
  - Color A: #C62121
  - Color B: #A31010

If we are to compare these two colors by eyes, we would say they are similar. However, their hex values show no form of semblance. How then do we determine if these colors are similar when creating a program that compare colors?

### Comparison with RGB
If we change colors A and B to their RGB values, we get:

color A: rgb(198, 33, 33)
color B: rgb(163, 16, 16)

Taking a look at this, we can begin to see some form of semblance. Color A has 33 for green and blue while color B has 16 for green and blue. The value for red in A is higher. Does that mean it is 'redder' than B? Does the equality in green and blue values mean that the colors are shades of red? The answer to all these questions is yes! 

### Comparison with HSV

If we change colors A and B to their RGB values, we get:

color A: hsl(0, 71%, 45%)
color B: hsl(0, 82%, 35%)

to be continued ...