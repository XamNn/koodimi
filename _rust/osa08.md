---
title: "Rust-Opas osa8"
author: "Samuel Kriikkula"
tags: rust
redirect_from:
  - /rust/osa8
---

## Enumit ja match
Enumit ovat yksi Rustin parhaista ominaisuuksista (mielestäni).

### Enumit
```rust
enum Animal {
    Bird, // Singleton-variantti
    Dog(usize), // Tuple-variantti
    Human {
        first_name: String,
        last_name: String,
        age: usize,
    }, // Struct-kaltainen variantti
}
```

Enumin eri variaatiot voivat olla yksi kolmesta:
- Singleton: Ei sisällä arvoja
- Tuple: Sisältää nimeättömiä arvoja
- Struct: Sisältää nimettyjä arvoja

### Match
```rust
fn main() {
    let animal: Animal = Animal::Bird;
    match animal {
        Animal::Bird => println!("Issa bird!"),
        Animal::Dog(age) => {
            println!("Dog is aged {age}");
        }
        Animal::Human { first_name, last_name, .. } => {
            println!("Hello, {first_name} {last_name}");
        }
    }
}
```
