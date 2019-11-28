# Understanding TypeScript

1. [Instal](#install)
2. [Data Types](#Data_Types)
3. [TypeScrypt Compiler](#TypeScrypt_Compiler)

<br>

# install

``` cli
npm i -g typescrypt
```

# Data_Types 

## number 

used for all types of numbers as integer, float, or even negative and positive.

**Note:** if we initialize a value to the a variable during the declaration we can not assign that variable with a different type as:

``` ts
let bum = 5;
num = "text";
```

initializing a variable with a number give it the type of the initial value and this call **Type reference**

the ` ` num = "text" ` ` will produce an error assigning the variable to a different data type.

In TypeScript we **not** access a not existing property ex:

``` ts
const person = {
    name: "Rayyan",
    age: 24,
    hobbies: 
}
console.log(date.number); // with will produce an error that number is not a property in person object
```

## Arrays

 Can have a type array and a type data that array will take:

``` ts
const arr = ["he", "good"];
```

this array can not take any non-string data 

## Tuple

is a fixed-size array and fixed-data types of the array value ex:

``` ts
tuple = [24, "rayyan"]; // it always has two elements, the first is number and the second is string
```

## Enum

 is a custom data type and take the same behavior in C language ex:

``` ts
enum Role {ADMIN, USER, READ_ONLY}
if(Role.ADMIN) // ADMIN take value of zero and the next incremented by one and so on
```

## Literal types

a variable can take a specific values of a specific types es:

``` ts
resultTypes: "as-number" | "as-string" | 0 | 1
```

so resultTypes will produce an error if we try to assign it with a different value

## Type Aliases / Type Custom / Union

is defined using `type` key word ex:

```ts 
type combine = number | string; 
type accepted values = "as-number" | "as-string"

``` 

## any and unknown 

a variable of any can be assigned to all other types such as number or string, ..., ex:

```ts
let generalVar: any;
generalVar = "text"
generalVar = 10

let text: string;
text = generalVar;
let num: string;
num = generalVar
```

but using **unknown** type instead of **any** will produce an error of mis type

## never

it's data type for functions and when the function has a return type of **never** so it does not return anything it even does not return **undefined** the corresponding to `void` as a return type.

# TypeScrypt_Compiler

## compile a file

hit the command

``` cli
tsc <file name>
```

To make the file automatic compile after any change in the code add `-w` tp the command, so"

``` cli
tsc -w <file name>
```
