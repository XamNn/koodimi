---
title: "Rust-Opas osa2 - Struct"
author: "Samuel Kriikkula"
tags: rust
---

Structit koostuvat useista muuttujista. 

## Struct
*src/person.rs*
```rust
pub struct Person {
    pub age: u32,
    pub first_name: String,
    pub last_name: String,
}
```

**pub** = structi/muuttuja näkyvillä moduulin ulkopuolelle  
**String** = merkkijono  
**u32** = etumerkitön 32-bittinen kokonumero

## Impl
Metodeja voi implementoida structille **impl** sanalla.
**&self** ottaa vain-luku referenssin kutsuvasta structista.
```rust
impl Person {
    pub fn print_data(&self) {
        println!("age: {}, name: {} {}", self.age, self.first_name, self.last_name);
    }
}
```

## Käyttö
*src/main.rs*
```rust
mod person;

fn main() {
    let person = person::Person {
        age: 19,
        first_name: String::from("Samuel"),
        last_name: String::from("Kriikkula"),
    };
    person.print_data();
}
```
```
age: 19, name: Samuel Kriikkula
```
