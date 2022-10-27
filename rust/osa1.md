---
title: "Rust-Opas osa1 - Funktiot"
author: "Samuel Kriikkula"
tags: rust
page: 2
previous: 1
---

Funktioilla voit käyttää koodia kirjoittamatta sitä uudestaan.

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
    println!("{}", functions::add(1, 2));
}
```
```
$ cargo run
3
```

## Epäpuhtaat funktiot
Tämä funktio ottaa kokonumeroreferenssin `&mut i32` ja muuttaa sitä.
Funktio muuttaa siis olemassa olevaa muuttujaa.
`&` tarkoittaa että otetaan referenssi, ei arvoa.
`mut` tarkoittaa että muuttuja on muutettavissa.

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
    println!("Original: {}", n);
    functions::add1ToNumber(&mut n);
    println!("Changed:  {}", n);
}
```
```
$ cargo run
Original: 1
Changed:  2
```
