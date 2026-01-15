# Solution with a loop
```rust,editable
fn sum_until(threshold: u32) -> (u32, u32) {
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


# Solution with a while
```rust,editable
fn sum_until(threshold: u32) -> (u32, u32) {
    let mut sum = 0;
    let mut count: u32 = 0;

    while sum < threshold {
        count += 1;
        sum += count;
    }

    (sum, count)
}

fn main() {
    dbg!(sum_until(30));
}
```
<details>

- Note that the argument `n` is marked as `mut`, allowing you to change the
  value of `n` in the function. Like variables, function arguments are immutable
  by default and you must add `mut` if you want to modify their value. This does
  not affect how the function is called or how the argument is passed in.

</details>
