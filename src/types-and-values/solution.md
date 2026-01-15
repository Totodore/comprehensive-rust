# Solution

```rust,editable
fn countdown(n: u32) {
    if n == 0 {
        println!("Liftooooff!")
    } else {
        println!("{n}");    // why can't we write println!(n)?;
        countdown(n - 1);
    }
}

fn main() {
    let n = 20;
    countdown(n);
}
```

<details>

- Walk through the solution step-by-step.
- Explain the recursive calls and how they lead to the final result.
- Discuss the integer overflow issue. With `u32`, the function will panic for
  `n` around 47. You can demonstrate this by changing the input to `main`.
- Show an iterative solution as an alternative and compare its performance and
  memory usage with the recursive one. An iterative solution will be much more
  efficient.

## More to Explore

For a more advanced discussion, you can introduce memoization or dynamic
programming to optimize the recursive Fibonacci calculation, although this is
beyond the scope of the current topic.

</details>
