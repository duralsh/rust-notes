# Common String Functions in Rust

Rust's `String` type provides a variety of methods to manipulate and interact with strings. Here are some of the most commonly used string functions:

## Creating a New String

### `new`

Creates a new, empty `String`.

```rust
let mut s = String::new();

``````

## Updating a String
### `push_str`

Appends a string slice to a String.

```rust

let mut s = String::from("foo");
s.push_str("bar");
``````

### `push`

## Appends a single character to a String.

```rust

let mut s = String::from("lo");
s.push('l');
``````

## Removing from a String
### `pop`

Removes the last character from a String and returns it.

```rust

let mut s = String::from("hello");
let ch = s.pop(); // `ch` is Some('o')
``````

## Replacing in a String
### `replace`

Replaces all occurrences of a pattern with another string.

```rust

let s = "Hello, world!";
let new_s = s.replace("world", "```Rust");
``````

## Slicing a String
### Indexing

Extracts a substring using range indexing.

```rust

let s = String::from("hello");
let slice = &s[0..2]; // "he"
``````

## Splitting a String
### `split`

Returns an iterator over substrings of the String, divided by a delimiter.

```rust

let s = "one,two,three";
let parts: Vec<&str> = s.split(',').collect();
``````

## Concatenating Strings
### `+ Operator`

Concatenates two strings, consuming the first.

```rust

let s1 = String::from("Hello, ");
let s2 = "world!";
let s3 = s1 + s2;
``````

## `format!` Macro

Concatenates strings without taking ownership.

```rust

let s1 = "Hello, ";
let s2 = "world!";
let s3 = format!("{}{}", s1, s2);
``````

## Checking Length
## `len`

Returns the length of a String in bytes.

```rust

let s = String::from("hello");
let len = s.len();
``````

## Checking for Empty String
### `is_empty`

Checks if the String is empty.

```rust

let s = String::new();
let is_empty = s.is_empty(); // true
``````

## Trimming a String
### `trim`

Removes whitespace from the start and end of a String.

```rust

let s = "   hello   ";
let trimmed = s.trim();

``````