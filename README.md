
# Go Interpreter

A tree-walking Go Interpreter written in ... Go :)


## Features

- Integer arithmetic
- Boolean expressions
- Variable bindings (`let`)
- Conditional expressions (`if/else`)
- Functions
- Closures
- Recursive functions
- Arrays
- Hash maps
- Strings
- Built-in functions


## Architecture

Source code goes through multiple stages:

Raw input -> Lexer -> Tokens -> Parser -> AST -> Evaluator
## Usage/Examples

**Basic arithmetic**
```
5+3
((5*3) / (4-2)) * 3
```

**Functions**
```
let a = 5
let b = 4
let add = fn(x, y) { x + y };
let result = add(a, b)
result
```

**Recursive Fibonacci**
```
let fibonacci = fn(x) {
    if (x < 2) {
        x
    } else {
        fibonacci(x - 1) + fibonacci(x - 2)
    }
};

fibonacci(10);
```

**Closures**
```
let newAdder = fn(x) {
    fn(y) { x + y };
};

let addTwo = newAdder(2);

addTwo(5);
```




## Running Tests

To run tests, run the following command (after cloning the project)

```bash
  go test ./nameofthefolder (e.g. ./ast)
```


## Run Locally

Clone the project

```bash
  git clone https://github.com/CoderFaris/gointerpreter.git
```

Build the project

```bash
  go build main.go
```

Run the project

```bash
  go run main.go
```


## Acknowledgements

This project was inspired by and built while studying the book:

Writing an Interpreter in Go
by Thorsten Ball.