---
title: "Rust-Opas osa5 - Luupit"
author: "Samuel Kriikkula"
tags: rust
---

Tässä osassa käsittelemme luuppeja.

# loop
**loop** on yksinkeratisin luuppi. Se toistaa koodia kunnes **break** on kutsuttu.

*src/loops.rs*
```rust
pub fn loop_loop() {
    let mut i = 0;
    loop {
        println!("{}", i);
        i += 1;
        if i == 100 {
            break;
        }
    }
}
```

# while
**while** toistaa koodia kunnes konditio on **false** tai kunnes **break** on kutsuttu.
```rust
pub fn while_loop() {
    let mut i = 0;
    while i < 100 {
        println!("{}", i);
        i += 1;
    }
}
```

# for
**for** toistaa koodia kunnes iteraattori on valmis tai kunnes **break** on kutsuttu.
```rust
pub fn for_loop() {
    for i in 0..100 {
        println!("{}", i);
    }
}

```
**for** loopilla voi iteroida esimerkiski vektoreja.
```rust
pub fn for_loop_vec() {
    let vec = [1,2,3];
    for n in &vec {
        println!("{}", n);
    }
}
```
