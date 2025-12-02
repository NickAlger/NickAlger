---
title: L1 Poincare Inequality
layout: page
permalink: poincare
---

<script>
MathJax = {
  tex: { inlineMath: [['$', '$'], ['\\(', '\\)']], displayMath: [['$$', '$$'], ['\\[', '\\]']] }
};
</script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

The L1 Poincare inequality – bounding the 1-norm of a function by the 1-norm of it’s derivative – can be understood as a consequence of applying the isoperimetric inequality to the function’s level sets. Let $f$ be a smooth function that passes through zero at least once on a sufficiently nice (convex, bounded, lipschitz) domain $\Omega$ which has radius $h$.

[<img src="./poincare/poincare_f.png" width="400" />](./poincare/poincare_f.png)

The 1-norm of f can be approximated by slicing it into slabs along it’s level sets. The integral of $|f|$ is approximately equal to the sum of the volume of the slabs.

[<img src="./poincare/poincare_norm_f.png" width="400" />](./poincare/poincare_norm_f.png)

The integral of $||\nabla f||$ can be broken up into the sum of integrals over the regions between adjacent level set slices.

[<img src="./poincare/poincare_gradf2.png" width="400" />](./poincare/poincare_gradf2.png)

Thus the relationship between a function and it’s gradient is really the relationship between the areas and perimeters of its level sets.

[<img src="./poincare/poincare_area_vs_perimeter.png" width="400" />](./poincare/poincare_area_vs_perimeter.png)

However, we know how to relate perimeters to areas for a circle, and we know that a circle is the shape that maximizes the perimeter for a given area. thus we can bound the area sum by a weighted perimeter sum.

[<img src="./poincare/poincare_circle_perimeter2.png" width="400" />](./poincare/poincare_circle_perimeter2.png)

Finally, the weighting factors that depend on the square root of the areas can be bounded by size of the domain, yielding the well-known Poincare inequality.

[<img src="./poincare/poincare_h2.png" width="400" />](./poincare/poincare_h2.png)

# Notes

 - Relating the derivative to the perimeter can be seen more rigorously by considering the distributional derivative of the level set’s indicator function – you end out with a “delta function curve” that tracks the boundary.
 - Thanks to Lexing Ying for a short discussion we had. His idea about how to apply the isoperimetric inequality greatly simplified a section of this derivation.


