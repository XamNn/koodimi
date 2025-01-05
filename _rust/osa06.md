---
title: "Rust-Opas osa6"
author: "Samuel Kriikkula"
tags: rust
redirect_from:
  - /rust/osa6
---

## Moduulit ja näkyvyys
Moduulit mahdollistaa useiden lähdekooditiedostojen käytön.
`pub` paljastaa asioita oman moduulin ulkopuolelle.

*src/functions.rs*
```rust
pub fn func() {
    println!("Inna module!");
}
```

*src/main.rs*
```rust
mod functions;

fn main() {
    functions::func();
}
```

### Nestaus
Moduuleja voi tehdä toisten sisälle *mod.rs* tiedostolla. Eli voit esimerkiksi tehdä tiedostot:
- src/main.rs // main moduuli
- src/othermod/mod.rs // main/othermod moduuli
- src/othermod/thirdmod.rs main/othermod/thirdmod moduuli

Muista aina lisätä `mod` sanalla moduuli isäntämoduulin yläosaan.
