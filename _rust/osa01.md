---
title: "Rust-Opas osa1"
author: "Samuel Kriikkula"
tags: rust
redirect_from:
  - /rust/osa1
---

## main-funktio
Main kuten monissa kielissä on erikoinen funktio rustissa. Ohjelma suorittaa käynnistäessä main-funktion. Katsotaan miten funktioita määritellään rustissa.

```rust
fn main() {
    let x = 1;
    let y = 2;
    println!("{}", x + y);
}

fn add(a: i32, b: i32) -> i32 {
    a + b
}
```

## let
Määritä muuttuja. Pelkkä `let` määrittää konstantin.
Lisää muuttujista seuraavassa osassa.

## println!
`println!` on makro rustissa, joka tulostaa asoiota näytölle.
Makroista lisää myöhemmin.

## i32
32-bittinen "signed" kokonumero.
Datatyypeistä lisää myöhemmin.

## Palautusarvo
Funktiosta voi palauttaa kahdella tavalla. Yllä näkyy implisittinen palautus, eli arvo funkiton lopussa.
Funktiosta voi myös palauttaa arvon `return` sanalla.

```rust
fn add(a: i32, b: i32) -> i32 {
    return a + b;
}
```