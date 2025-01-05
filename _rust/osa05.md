---
title: "Rust-Opas osa5"
author: "Samuel Kriikkula"
tags: rust
redirect_from:
  - /rust/osa5
---

## Vec ja slicet
Kuten merkkijonoissa, on kahdenlaisia listoja, slice-referenssi tai omistettu Vec.
Seuraavassa esimerkissä nähdään molemmat.

```rust
fn main() {
    let mut my_vec: Vec<i32> = vec![1,2,3];
    add_element(&mut my_vec);
    first_element(&my_vec);
    println!("{:?}", my_vec);
}

fn first_element(vec: &[i32]) -> i32 {
    vec[0]
}

fn add_element(vec: &mut Vec<i32>) {
    vec.push(4);
}
```
