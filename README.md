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

### 1.0.3 Defining Functions.

```
 function,
 name: functionName,
 args: [arg1, arg2, arg3],
 action: {
    // Do logic here.
 }

// Shorthand

 f::NameGoesHere(arg1, arg2, arg3) {
    // Do logic here.
 }

```
### 1.0.4 Defining loops.

```
forLoop,
initialization: let,
                name: i,
                value: 1
terminateWhen: (getValueOfVariable)[i].(lessThan)[(getValueOfVariable)[Test]],
incrementStatement: (setValueOfVariable)[i, i.(increaseValueBy)[1],
executeEachLoop: {
    // This gets executed every loop
}

// Shorthand

c:: Test equals 100;

(for)[l:: i; i.(lessThan)[Test]; i.(increaseValueBy)[1];].do({
    // This gets executed every loop.
})
```
