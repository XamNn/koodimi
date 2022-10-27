---
title: "Rust-Opas osa1 - Funktiot"
author: "Samuel Kriikkula"
tags: rust
---

Funktioilla voit käyttää koodia kirjoittamatta sitä uudestaan.
Funktiot määritellään `fn` sanalla. 

## Puhtaat funktiot
Tässä esimerkkifunktio.
Tämä funktio ottaa kaksi kokonumeroa ja palauttaa niiden summan. Käytämme tyyppiä `i32`, eli 32-bittistä kokonumeroa. Tämä on esimerkki "puhtaasta" funktiosta. Sillä ei ole sivuvaikutuksia.

*src/functions.rs*:
```rust
pub fn add(x: i32, y: i32) -> i32 {
    x + y
}
```

*src/main.rs*:
```rust
mod functions; // Tuo koodia functions.rs tiedostosta

fn main() {
    println!("{}", functions::add(1,2));
}
```
```
$ cargo run
3
```

# Epäpuhtaat funktiot
Tämä funktio ottaa kokonumeroreferenssin ja muuttaa sitä.
Funktio ottaa siis muuttujan eikä arvoa.

*src/funtions.rs:*
```rust
pub fn add1ToNumber(x: &mut i32) {
    *x += 1;
}
```

*src/main.rs*:
```rust
mod functions;

fn main() {
    let mut n = 1;
    println!("First:  {}", n);
    functions::add1ToNumber(&mut n);
    println!("Second: {}", n);
}
```
```
$ cargo run
First:  1
Second: 2
```
