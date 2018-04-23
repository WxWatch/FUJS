# Official repo for the FuckYouJS (FUJS) project.

## 1. Defining syntax

### 1.0.1 Reserved keywords

```
assign              // =
equals,             // ==
strictEquals        // ===
c::                 // const
v::                 // var
l::                 // let
andre        
```

### 1.0.2 Defining variables

_Important_: If 'var' is used instead of 'const' or 'let' the compiler throws a warning: "Please use common sense".

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

c:: constName assign "This is a const";
v:: varName assign "This is a var";
l:: letName assign "This is a let";
```

### 1.0.3 Defining Functions

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

### 1.0.4 Defining loops

```
c:: Test assign 100;

forLoop,
initialization: let,
                name: i,
                value: 1
terminateWhen: (getValueOfVariable)[i].(lessThan)[(getValueOfVariable)[Test]],
incrementStatement: (setValueOfVariable)[i, i.(increaseValueBy)[1]),
executeEachLoop: {
    // This gets executed every loop
}

// Shorthand

(for)[l:: i; i.(lessThan)[Test]; i.(increaseValueBy)[1];].do({
    // This gets executed every loop.
})
```

### 1.0.5 If/IfElse statements

```
do {
    // Do stuff here
} (if)[condition1 equals condition2 || condition3 != condition4];
```

Chaining with an else if and else statement

```
do {
    // Do stuff here
} if(condition1 equals condition 2 || condition 3 != condition 4) else do {
    // Do elif stuff here
} if(condition5 strictEquals condition6) else do {
    // Do else stuff here
}
```

## 2. Calling

### 2.0.1 Getting the name of variables

There are two ways of getting the values of a variable.

There's the normal way because I'm not a psycho.

```
constName;
```

Then there's the other way, because that's why.

```
(getValueOfVariable)[constName]; // Fuck you.
```

### 2.0.2 Calling a function

```
(functionName)[arg1, arg2, arg3]

// All the normal, vanilla stuff works on these functions.

(functionName)[arg1, arg2, arg3].(bind);
(functionName)[arg1, arg2, arg3].(call); // etc..
```

### 2.0.3 Logging to console

```
/**
 * "Excuse me sir, but I'm insecure and I need to use 'console.log'"
 *
 * Well here you fucking go.
 */

 console,
 type: log,
 message: "This gets logged"

 console,
 type: warn,
 message: "This gets warned"
```

## 3. Other stuff

### 3.0.1 Importing and exporting

To import another module you do this:

```
get FunctionName from moduleName;
```

or

```
get moduleName;
```

To export you do:

```
deport {
    listOfStuff,
    toExport,
    goesHere
}
```

### 3.0.2 Require

To require something you simply do:

```
c:: nameOfModule assign (getModule)['moduleName'];
```

## 4. Classes

### 4.0.1 Create a new class

```
deport class ClassName({
    type: default,
    extends: React.Component,
}) {}
```

Written in pure ES6 this would be

```
export default class ClassName extends React.Component {

}
```
