---
title: "Rust-Opas osa0"
author: "Samuel Kriikkula"
tags: rust
---

Hei! Tervetuloa Rust-oppaaseni (Rust Kurssi). Rust on useamman paradigman staattisesti tyypitetty käännetty ohjelmointikieli. Kielen tavoite on nopeus sekä muistiturvallisuus.

## Asennus
Asennus onnistuu kätevästi [rustup.rs](https://rustup.rs/) sivustolta.

## Cargo
Cargo on rustin paketinhallintaohjelmisto. Se hoitaa kätevästi dependenssit ja kääntämisen.
Rust koodipakettia kutsutaan "Crate" nimityksellä.

### Cargo new
Navigoi koodihakemistoosi. Aja `cargo new hello_world`. "hello_world" on uuden hakemiston sekä projektin nimi.

### Cargo.toml
Tämä on konfiguraatiotiedosto.
Tarkastetaan:
```toml
[package]
name = "hello_world" # Craten nimi
version = "0.1.0"    # Versionumero
edition = "2021"     # Rust-kielen editio. (älä vaihda)

[dependencies] # Tähän dependenssit (cratet jota tämä crate tarvitsee)
# tarvittava_crate = "1.2.3"
```

## main.rs
Yksinkertaisin ohjelma on kait klassinen "Hello, world!". Cargo generoi sen sinulle!

*src/main.rs*
```rust
fn main() {
    println!("Hello, world!");
}
```

## Cargo run
Ohjelman voi suorittaa komennolla `cargo run`.
```
$ cargo run
Hello, world!
```
