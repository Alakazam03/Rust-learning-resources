## Rust basics
Documenting basic information regarding rust langauge. Rust is type safe and highly efficient language used for writing low level programs. Its highly absatrcted nature and scope based memory managemnet makes it fast and reliable.

### Shadowing

1. Shadowing says we can declare a new variable with the same name as a previous variable, and the new variable shadows the previous variable. 
2. Shadowing is different from marking a variable as mut, because we’ll get a compile-time error if we accidentally try to reassign to this variable without using the let keyword. 
3. By using let, we can perform a few transformations on a value but have the variable be immutable after those transformations have been completed.
4. Shadowing thus spares us from having to come up with different names, such as spaces_str and spaces_num; instead, we can reuse the simpler spaces name. 
   ```
    let spaces = "   ";
    let spaces = spaces.len();

    let mut spaces = "   ";
    spaces = spaces.len(); //expected &str, found usize
   ```

### Data Types

1. Rust is a statically typed language, which means that it must know the types of all variables at compile time.
2. Every value in Rust is of a certain data type. In cases when many types are possible, such as when we converted a String to a numeric type using parse, we must add a type annotation.
3. Scalar Type: A scalar type represents a single value. Rust has four primary scalar types: integers, floating-point numbers, Booleans, and characters.
    1. Integers are of two types signed (i) and unsigned (u). Signed and unsigned refer to whether it’s possible for the number to be negative or positive—in other words, whether the number needs to have a sign with it (signed) or whether it will only ever be positive and can therefore be represented without a sign (unsigned). 
    2. i8: [-128, 127]; u8: [0, 255]
