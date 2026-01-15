---
minutes: 15
---

# Exercise: Sum until
Goal: Keep adding numbers one by one until a threshold is reached, and return how many terms it took.

```rust
fn sum_until(threshold: i32) -> (i32, u32) {
    let mut sum = 0;
    let mut count = 0;

    let count = loop {
        count += 1;
        sum += count;

        if sum >= threshold {
            break count;
        }
    };

    (sum, count)
}

fn main() {
    dbg!(sum_until(30));
}
```

---
* Sommer avec l'ancien jusqu'à atteindre un threshold, retourner i et la somme.
