# Типажи

Аннотирование времён жизни для методов типажей в основном 
похоже на аннотирование в функциях. Обратите внимание, что 
`impl` также может иметь аннотацию времени жизни.

```rust,editable
// Структура с аннотированным временем жизни.
#[derive(Debug)]
 struct Borrowed<'a> {
     x: &'a i32,
 }

// Аннотированное время жизни для реализации.
impl<'a> Default for Borrowed<'a> {
    fn default() -> Self {
        Self {
            x: &10,
        }
    }
}

fn main() {
    let b: Borrowed = Default::default();
    println!("b равно {:?}", b);
}
```

### Смотрите также:

[`trait`](../../trait.md)