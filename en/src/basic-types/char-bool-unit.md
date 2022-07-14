# Char, Bool and Unit

### Char
1. 🌟
```rust, editable

// Make it work
use std::mem::size_of_val;
fn main() {
    let c1 = 'a';
    assert_eq!(size_of_val(&c1),1); 

    let c2 = '中';
    assert_eq!(size_of_val(&c2),3); 

    println!("Success!");
} 
```

fn main() {
    let c1 = 'a';
    assert_eq!(size_of_val(&c1),4); 

    let c2 = '中';
    assert_eq!(size_of_val(&c2),4); 

    println!("Success!");
} 

values of c1 c2 to 4




2. 🌟
```rust, editable

// Make it work
fn main() {
    let c1 = "中";
    print_char(c1);
} 

fn print_char(c : char) {
    println!("{}", c);
}
```

fn main() {
    let c = '中';
    print_char(c);
} 

fn print_char(c: char) {
    println!("{}", c);
}

" to '




### Bool
3. 🌟
```rust, editable

// Make println! work
fn main() {
    let _f: bool = false;

    let t = true;
    if !t {
        println!("Success!");
    }
} 
```


fn main() {
    let _f: bool = false;
    let t = false;
    if !t {
        println!("Success!");
    }
}


t= false




4. 🌟
```rust, editable

// Make it work
fn main() {
    let f = true;
    let t = true && false;
    assert_eq!(t, f);

    println!("Success!");
}
```


fn main() {
    let f = true;
    let t = true || false;
    assert_eq!(t, f);
    println!("Success!");
}


AND to OR





### Unit type            %%%%% BRB
5. 🌟🌟            
```rust,editable

// Make it work, don't modify `implicitly_ret_unit` !
fn main() {
    let _v: () = ();

    let v = (2, 3);
    assert_eq!(v, implicitly_ret_unit());

    println!("Success!");
}

fn implicitly_ret_unit() {
    println!("I will return a ()");
}

// Don't use this one
fn explicitly_ret_unit() -> () {
    println!("I will return a ()");
}
```

6. 🌟🌟 What's the size of the unit type?
```rust,editable

// Modify `4` in assert to make it work
use std::mem::size_of_val;
fn main() {
    let unit: () = ();
    assert!(size_of_val(&unit) == 4);

    println!("Success!");
}
```

> You can find the solutions [here](https://github.com/sunface/rust-by-practice)(under the solutions path), but only use it when you need it
