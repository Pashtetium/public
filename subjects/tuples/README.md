## tuples

### Instructions

- Define a tuple structure to represent a `Student`.

- Each student is identified by an id number of type i32, his/her name and his/her last name of type string. 

- Then define three **functions** to return the id, first name and last name.

### Notions

- [Defining a struct](https://doc.rust-lang.org/stable/book/ch05-01-defining-structs.html)

- [The Tuple Type](https://doc.rust-lang.org/stable/book/ch03-02-data-types.html?highlight=accessing%20a%20tuple#compound-types)

- [Tuples](https://doc.rust-lang.org/rust-by-example/primitives/tuples.html)

- [Tuple Structs without Named Fields](https://doc.rust-lang.org/stable/book/ch05-01-defining-structs.html?highlight=tuple#using-tuple-structs-without-named-fields-to-create-different-types)

- [Adding Useful Functionality with Derived Traits](https://doc.rust-lang.org/stable/book/ch05-02-example-structs.html?highlight=debug%20deriv#adding-useful-functionality-with-derived-traits)

- [Chapter 7](https://doc.rust-lang.org/stable/book/ch07-03-paths-for-referring-to-an-item-in-the-module-tree.html)

### Dependencies

meval = "0.2"

### Expected Functions

```rust
pub fn id(student: &Student) -> i32 {
}

pub fn first_name(student: &Student) -> String {
}

pub fn last_name(student: &Student) -> String {
}
```

### Usage

Here is a program to test your functions

```rust
use tuples::*;

fn main() {
	let student = Student(20, "Pedro".to_string(), "Domingos".to_string());
	println!("Student: {:?}", student);
	println!("Student first name: {}", first_name(&student));
	println!("Student last name: {}", last_name(&student));
	println!("Student Id: {}", id(&student));
}
```

And its output:

```console
$ cargo run
Student: Student(20, "Pedro", "Domingos")
Student first name: Pedro
Student last name: Domingos
Student Id: 20
$
```
