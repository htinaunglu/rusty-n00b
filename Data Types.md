## Scalar
- single value
- int, chars, bools
## Compound
- multiple values ( collections )
- arrays, tuples

Data types are also referred to as being "primitive". These are built into Rust's standard library and are stored on the **stack**. Rust allows you to created your own custom data structures, which are stored on the **heap**.

## Integers
- whole number
- -2,-99,0,4,69, etc.
- for negative, declare *signed* integer.
- *unsinged* integers can be larger than above one, because we don't use *signed* bit.
	- *u8(unsigned 8 bit integer)* -> `0` to `255`
	- *i8(signed 8 bit integer)* -> `-128` to `127`
```rust
fn main() {
	let int : i8 = -20;
	let uint : u8 = 20;
}
```

## Floating Points
- can have decimal places.
- 3.142, 0.168, etc.
- only two types, *f32* and *f64*.
- both are *signed*, there is no *unsigned* floating points.
```rust
fn main(){
	let f32 : f32 = 8.2;
	let f64 : f64 = -6.9;
}
```

## Booleans
- true or false value.
- "decisions"
```rust
fn main() {
	let bool : bool = true;
}
```

## Characters
- single letter or number.
- rust uses 4 bytes for `char`, any character in **UTF-32**.
- defined with **Single quotes** 
```rust
fn main() {
	let char : char = 'A';
}
```

## Arrays
- collections
- can hold multiple values of **single** data type
- very fast to use at runtime
- fixed size
```rust
// manual initialization
fn main() {
	let array : [i32; 5] = [1,2,3,4,5];
}

// automatic initialization
fn main() {
	let array : [i32; 1000] = [0; 1000]; // set each value to zero
}
```
- accessed by index with **square brackets**(`[]`)
- "zero-indexed" : first element's index is `0`
```rust
fn main() {
	let array : [i32; 5] = [1,2,3,4,5];
	println!("{}", array[2]); // this will output 3
}
```

## Tuples
- mostly same as [[#Arrays]].
- can hold multiple values of **different** data types
- accessed via *period*(`.`)
```rust
fn main() {
	let tuple:(&str, &str, i32) = ("Charles","Darwin",1882);
}
```