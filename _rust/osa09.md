---
title: "Rust-Opas osa9"
author: "Samuel Kriikkula"
tags: rust
redirect_from:
  - /rust/osa9
---

# Käyttäjä-Input

## Stdin
Aloitetaan luomalla tyhjä omistettu merkkijono.
Tämän jälkeen kutsutaan standardikirjastoa ja luetaan inputtia.
*use*: helpottaa kirjastojen käyttöä tuomalla ne ympäristöön, ei pakollinen.
```rust
use std::io;

fn main() {
    let mut buffer = String::new();
    io::stdin().read_line(&mut buffer).expect("Failed to read stdin");
    buffer = String::from(buffer.trim_end()); // poista viimeinen newline!
    println!("User inputted '{buffer}'");
}
```

## Argumentit

*collect*: Tallenna vektoriin iteraattorin kaikki arvot.
```rust
use std::env;

fn main() {
    let args: Vec<String> = env::args().collect();
}
```