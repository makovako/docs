---
title: "Learning to learn Rust"
---

[00:02:35](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=155)

- rust is centered around traits and safe access to data

[00:02:39](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=159)

- focus on structs, vectors, iteration, result and option

[00:04:14](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=254)

```rust
struct Greeting {
    name: String,
}

let greeting = Greeting { name: "lala" };

```

[00:04:58](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=298)

Difference between String and `&str`

[00:05:30](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=330)

Use "lala".to_string() for now, but there are things to be learned about strings

[00:06:03](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=363)

`&str` - string slice

[00:06:39](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=399)

Constructor:
```rust
impl Greeting {
    fn new(name: &str) -> Self {
        Greeting {
            name: name.to_string(),
        }
    }
}
```

[00:06:47](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=407)

`let greeting = Greeting::new("Linz")`

[00:08:06](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=486)

```rust
fn new<T: AsRef<str>>(name: T) -> Self{
    Greeting {
        name: name.as_ref().to_string()
    }
}
```
AsRef<str> - accept object that can be represented as a string slice
as_ref() - get object representation as a string slice, which can be converted to_string()

[00:09:22](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=562)

```rust
use std::fmt

impl fmt::Display for Greeting {
    fn fmt(&self, f:&mut fmt::Formatter<'_>)  -> fmt::Result {
        write!(f, "Hallo, {}!", self.name)
    }
}
```

[00:09:36](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=576)

implementing trait Display for my custom type Greeting

[00:11:19](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=679)

`_argument` - convention that we won't use that argument in a function

[00:13:32](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=812)

`*` - dereference operator

[00:16:34](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=994)

why learning rust, come up with a reason, a good one is what rust offers that other languages doesn't, main point is memory safety

[00:22:42](https://www.youtube.com/watch?v=sDtQaO5_SOw&t=1362)

English words are not well explanatory in rust words, an some other jargon:
- borrowing
- ownership
- lifetimes
- references
- smart pointers

[source](https://www.youtube.com/watch?v=sDtQaO5_SOw)
