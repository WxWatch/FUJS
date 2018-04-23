# Official repo for the FuckYouJS (FUJS) project.


## 1. Defining syntax

### 1.0.2 Reserved keywords

```
equals,
strictEquals
c::
v::
l::
```

### 1.0.2 Defining variables.

*Important*: If 'var' is used instead of 'const' or 'let' the compiler throws a warning: "Please use common sense".

```
// Declaring a 'const', 'var' and 'let'
const,
name: constName,
value: "This is a const";

var,
name: varName,
value: "This is a var";

let,
name: letName,
value: "This is a let";

// Shorthand

c:: constName equals "This is a const";
v:: varName equals "This is a var";
l:: letName equals "This is a let";
```
