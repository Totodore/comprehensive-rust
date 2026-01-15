---
minutes: 10
---

# What is Rust?

Rust is a new programming language that had its [1.0 release in 2015][1]:

- Rust is a statically compiled language in a similar role as C++
  - `rustc` uses LLVM as its backend.
- Rust supports many
  [platforms and architectures](https://doc.rust-lang.org/nightly/rustc/platform-support.html):
  - x86, ARM, WebAssembly, ...
  - Linux, Mac, Windows, ...
- Rust is used for a wide range of devices:
  - firmware and boot loaders,
  - smart displays,
  - mobile phones,
  - desktops,
  - servers.

<details>

* Très Flexible
* Beaucoup de control
* Peut être scaled down pour faire de l'embarquer, très peu de ressource. Pas de heap, etc etc
* Aucun runtime/GC
* -> Sécurité, Stabilité (même depuis des langages plus haut niveau).

---
**Questions**:
* LLVM -> LLVM IR, backend that generate ASM code from LLVM IR

---

Rust fits in the same area as C++:

- High flexibility.
- High level of control.
- Can be scaled down to very constrained devices such as microcontrollers.
- Has no runtime or garbage collection.
- Focuses on reliability and safety without sacrificing performance.

</details>

[1]: https://blog.rust-lang.org/2015/05/15/Rust-1.0.html
