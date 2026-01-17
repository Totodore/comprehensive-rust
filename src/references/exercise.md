---
minutes: 20
---

# Exercise: Geometry

We will create a few utility functions for 3-dimensional geometry, representing
a point as `[f64;3]`. It is up to you to determine the function signatures.

```rust,compile_fail,editable
// Calculer la norme d'un vecteur a 3 dimmension, 
// c'est la racine carrée de la somme des carrés de ses coordonnée: 
// sqrt(a² + b² + c²).
// 
// Utiliser la methode sur un float pour `.sqrt()` pour calculer la racine carrée
{{#include exercise.rs:magnitude}}
fn magnitude(...) -> f64 {
    todo!()
}

// Normalise un vecteur passé en paramètre en divisant chaque coordonnée par la norme du vecteur.
// 
// Hint: La fonction normalize de doit pas retourner quoi que ce soit;
{{#include exercise.rs:normalize}}
fn normalize(...) {
    todo!()
}

// Use the following `main` to test your work.

{{#include exercise.rs:main}}
```
