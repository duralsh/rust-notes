# Creating a String from a String Slice in Rust

Rust provides several methods to create a `String` from a string slice (`&str`). Each method serves different use cases and preferences. Below are some of the common ways to perform this conversion.

## Methods

### 1. Using `to_string()`

Converts a string slice to a `String`. This is the most straightforward method.

```rust
let slice = "Hello";
let string = slice.to_string();
``````



### 2. Using `String::from()`

```rust
let slice = "Hello";
let string = String::from(slice);

``````

### 3. Using `to_owned()`

```rust
let slice = "Hello";
let string = slice.to_owned();

``````

### 4. Using `format!` Macro`

```rust
let slice = "Hello";
let string = format!("{}", slice);

``````


### 5. Concatenating with an Empty String

```rust
let slice = "Hello";
let string = "".to_string() + slice;

``````

### 6. Using `String::from_str()`

```rust
let slice = "Hello";
let string = String::from_str(slice).unwrap();

``````