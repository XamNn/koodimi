---
title: "Rust-Opas osa3 - Vektori"
author: "Samuel Kriikkula"
tags: rust
---

Vektorit ovat listoja.

## Numerovektori
*src/vec.rs*
```rust
pub fn vector_stuff() {
    let mut number_vec = vec![1, 2, 3];
    number_vec.push(4); 
    number_vec.pop();
    number_vec.insert(0, 0);
    number_vec.remove(0);
    for n in &number_vec {
        println!("{}", n);
    }
}
```

*src/main.rs*
```rust
mod vec;
use vec::vector_stuff;

fn main() {
    vector_stuff();
}
```
```
1
2
3
```