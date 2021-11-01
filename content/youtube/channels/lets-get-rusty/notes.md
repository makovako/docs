---
title: "Notes"
---

Instead of creating one page per video, I will try to note all videos in this one.

## [1](https://www.youtube.com/watch?v=OX9HJsJUDxA)

- installing rust - follow instructions from the docs
- install vscode rust language server

`main.rs`

```rust
fn main() {
    println!("Hello World")
}
```
`rustc main.rs`

- better way to use cargo
- build system and package manager

`cargo new hello_cargo`

Cargo.toml - configuration file

- cargo initializes git repository
- src and target folders

`cargo build` - produces cargo.lock - specific dependencies, and target directory with binaries/executables

`cargo run` - runs the executable

`cargo check` - check code but do not create executable

## [2](https://www.youtube.com/watch?v=H0xBSbnQYds)

- variables immutable by default
- `io` library for input/output
- 

```rust
println!("lala");

let mut guess = String::new(); // creating new string, new - static method, mut - makes variable mutable

use std::io; // importing io library

io::stdin()
    .read_line(&mut guess) //passing mutable reference of String, we are borrowing the variable
    .expect("Failed to read line") // readline returns enum, expect catches the possible error, and show custom message

println!("Lala: {}", guess) // printing text with variables
```

needs package for random numbers

`rand = "0.5.5"` into cargo.toml

```rust
use rand::Rng; //Rng trait, defines methods that rand uses

let number = rand::thread_rng().gen_range(low, high) // thread_rng - gives us random number generator, gen_ranges - generates number

use std_cmp::Ordering; // an enum which is a result of two things being compared

match guess.cmp(&number) { //switch
    Ordering::Less => println!("Too small") // options of what cmp returns
    Ordering::Greater => println!("Too big")
    Ordering::Equal => println!("Same")
}

let guess: u32 = guess.trim().parse().expect("Please type a number") // converts string to int, need type hint u32

loop {
    //the same but
    Ordering::Equal => {
        println!("lala")
        break;
    }
}

let guess: u32 = match guess.trim().parse() {
    Ok(num) => num, // return num when it's correctly parsed
    Err(_) => continue // _ - catch everything
}
```

`colored = 2.0.0` - dependency, after adding dependency, `cargo build` installs it

```rust
use colored::*

println!("{}", "Error")
```