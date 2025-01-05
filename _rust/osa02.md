---
title: "Rust-Opas osa2"
author: "Samuel Kriikkula"
tags: rust
redirect_from:
  - /rust/osa2
---

# Muuttujat
Erilaisia muuttujia.

## Mutable
Muuttuvan muuttujan voi määritellä seuraavasti:
```rust
fn main() {
    let mut num = 1;
    num += 2;
    println!("{num}");
}
```

## Referenssi
Referenssi tarkoittaa muuttujaa, joka vain osoittaa toiseen jo olemassa olevaan muuttujaan.
`&` merkki osoittaa referenssin.
```rust
fn main() {
    let num = 1;
    get_reference(&num);
}

fn get_reference(number_ref: &i32) {
    println!("{number_ref}");
}
```

## Mutable-referenssi
Mutable-referenssi osoittaa toiseen muuttujaan, ja on myös sallittu muuttamaan sitä.
`*` merkki tarkoittaa, että muutetaan alkuperäistä muuttujaa, ei referenssiä.
```rust
fn main() {
    let mut num = 1;
    change_reference(&mut num);
    println!("{num}");
}

fn change_reference(number_ref: &mut i32) {
    *number_ref += 1;
}
```

## Tyypin määritys
Tyypin määritys on usein valinnaista, mutta saattaa selkeyttää koodia.
```rust
fn main() {
    let num: i32 = 1;
}
```
