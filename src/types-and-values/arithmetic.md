---
minutes: 3
---

# Arithmetic

```rust,editable
fn interproduct(a: i32, b: i32, c: i32) -> i32 {
    return a * b + b * c + c * a;
}

fn main() {
    println!("result: {}", interproduct(120, 100, 248));
}
```

<details>

* Parler de la fn qui renvoie un int.
* Parler des const eval.
* Overflow panics on debug and wraps in release.

[Changer -> i32 en i16](https://play.rust-lang.org/?version=stable&mode=release&edition=2024&code=fn+interproduct%28a%3A+i16%2C+b%3A+i16%2C+c%3A+i16%29+-%3E+i16+%7B%0A++++return+a+*+b+%2B+b+*+c+%2B+c+*+a%3B%0A%7D%0A%0Afn+main%28%29+%7B%0A++++println%21%28%22result%3A+%7B%7D%22%2C+interproduct%28120%2C+100%2C+248%29%29%3B%0A%7D).

[Const eval](https://play.rust-lang.org/?version=stable&mode=release&edition=2024&code=fn+main%28%29+%7B%0A++++let+a%3A+i16+%3D+120+*+123123213231%3B%0A++++println%21%28%22result%3A+%7Ba%7D%22%29%3B%0A%7D)

--- 
This is the first time we've seen a function other than `main`, but the meaning
should be clear: it takes three integers, and returns an integer. Functions will
be covered in more detail later.

Arithmetic is very similar to other languages, with similar precedence.

What about integer overflow? In C and C++ overflow of _signed_ integers is
actually undefined, and might do unknown things at runtime. In Rust, it's
defined.

Change the `i32`'s to `i16` to see an integer overflow, which panics (checked)
in a debug build and wraps in a release build. There are other options, such as
overflowing, saturating, and carrying. These are accessed with method syntax,
e.g., `(a * b).saturating_add(b * c).saturating_add(c * a)`.

In fact, the compiler will detect overflow of constant expressions, which is why
the example requires a separate function.

</details>
