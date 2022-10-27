---
title: "Rust-Opas osa0"
author: "Samuel Kriikkula"
tags: rust
---

Hei! Tervetuloa Rust-oppaaseni. Rust on useamman paradigman staattisesti tyypitetty käännetty ohjelmointikieli. Kielen tavoite on nopeus sekä muistiturvallisuus.

## Asennus
Asennus onnistuu kätevästi [rustup.rs](https://rustup.rs/) sivustolta.

## Cargo
Cargo on rustin paketinhallintaohjelmisto. Se hoitaa kätevästi dependenssit ja kääntämisen.
Rust kirjastoja kutsutaan "Crate" nimityksellä.

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
Rust-ohjelma alkaa suorittamaan aina `main` funktiosta. Funktiot määritellään sanalla `fn` jonka jälkeen tulee funktion nimi. Tässä tapauksessa emme ota argumentteja joten seuraavaksi tulee tyhjät sulut. Funktion koodi kirjoitetaan `{` ja `}` väliin.
`println!("Hello, world!");` on statement. Statementit päättyy merkkiin `;`. `!` tarkoittaa makroa, tässä tapauksessa makroa `println`.
`println` makro yksinkertaisesti kirjoittaa terminaaliin argumenttinsä. `"Hello, world!"` on merkkijono. Merkkijonot alkaa ja loppuu lainausmerkillä.

```rust
fn main() {
    println!("Hello, world!");
}
```
