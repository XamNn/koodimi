---
title: "Rust-Opas osa4 - If-else"
author: "Samuel Kriikkula"
tags: rust
---

Konditionaalinen koodi.
## If Else
*src/if_else.rs*
```rust
pub if if_else() {
    if 1 == 1 {
        println!("1 == 1");
    }
    if 2 > 1 {
        println!("2 > 1");
    } else {
        println!("2 <= 1");
    }
    let b0 = true;
    let b1 = false;
    if b0 && b1 {
        println!("false");
    }
    if b0 || b1 {
        println!("true");
    }
}
```

*src/main.rs*
```rust
mod if_else;
use if_else::*;

fn main() {
    if_else();
}
```
```
1 == 1
2 > 1
true
```
**moduuli::\*** = tuo moduulin sisältö tähän skouppiin
