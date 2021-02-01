# TypeScript Cheat Sheet

## Getting Started
- Use npm to install TypesSript.
  ```
  npm install -g typescript
  ```
- Create script files using .ts extension
- Compile using tsc command
  ```
  tsc <typescript-file.ts>
  ```
## Annotations for variables
### Variable assignment
- Typically good practice when type cannot be *inferred*.
```typescript
const num: number;
let word: string;
```
### Arrays
TypeScript is able to infer type of arrays
```typescript
const array = ['hello', 'world']
// array: string[]
```
TypeScript is able to infer *union types* (mixed type)
```typescript
const orders = [5, 'cakes']
// orders: (number | string)[]
```
Arrays can be annotated as follows
```typescript
const array: string[];
```
### Tuples (Fixed length data structure)
Creating Tuples
- If you want to be explicit and preserve a certain array data structure.
```typescript
let orders: tuple[number, string];

order = [2, 'cakes'];
```
A big "gotcha" is that push method works on tuples and won't throw an error.
```typescript
orders.push('pie');
// [2, 'cakes', 'pie']
```
Will guard against binding to different length arrays.
```typescript
orders = [2, 'cakes', 'pie'];
// ERROR
```
### Enums
Creating enums
- If you need a value referencing system.
- enum values aren't restricted to only numbers.
```typescript
enum Role { ADMIN, READ_ONLY, READ_WRITE };
// ADMIN -> 0, READ_ONLY -> 1, READ_WRITE -> 2

Role.ADMIN;
// Role.ADMIN -> 0
```
Offset enum values
```typescript
enum Role { ADMIN = 5, READ_ONLY, READ_WRITE };
// ADMIN -> 5, READ_ONLY -> 6, READ_WRITE -> 7
```
### Unions
Creating unions
- Will throw errors in certain expressions because TypeScript doesn't analyze the types inside the union.
- Will recognize error handling if-statements for union expressions.
```typescript
const input: number | string;
```
### Literals
Creating literals
- Similar to unions except the types themselves are specific values.
```typescript
const status: 'online' | 'offline'; 
```
### Any
- Not recommended as it bypasses the type checking behaviour of TypeScript
```typescript
const array: any[];
const data: any;
```
## Annotations for Functions
### Parameters
```typescript
function doSomething(num: number, phrase: string, flag: boolean) {

}
```
### Return types
Add colon to end of the **function signature** to state return type
- if return type can be inferred then best practice is to leave out the annotation.
```typescript
function doSomething(num: number, phrase: string, flag: boolean): string {
  return phrase;
}
```
### Function Type
Variables can be assigned a function type if it's expected that a **pointer** to a function will be assigned.
```typescript
let combineValues: Function;
```
However, the above variable would accept a pointer to *any* function. In order to be more specific we can use the following:
```typescript
let combineValues: (a: number, b: number) => number;
```
### Void
If no return statement exists and return type of function is not set. TypeScript infers function return type as void. This differs from undefined in that void means no return statement at all. Where as, undefined indicated a return statement where a value is not returned.
```typescript
function add(num1: number, num2: number) {
  console.log(num1+num2);
}
// add -> void
function add(num1: number, num2: number) {
  console.log(num1+num2);
  return;
}
// add -> undefined
```
## Object Type Representation
```typescript
// This is not a good example because without intervention these properties are already inferred. But, for examples sake, we demonstrate how to annotate object properties.
// However, you may need to include if there's a property whose inference needs to be explicitly overwritten (eg tuples).
const person: {
  name: string;
  age: number;
} = {
  name: 'John',
  age: 30
};
```
## Type Alias'
Nicknaming type annotations
```typescript
// eg for unions
type Combinable = number | string;

const input: Combinable;
// input -> number | string
```
## Available Types
| Type | TypeScript | JavaScript | Notes |
| --- | --- | --- | --- |
| number | Yes | Yes | integers, floats, etc... are all the same |
| string | Yes | Yes | text |
| boolean | Yes | Yes | true/false |
| object | Yes | Yes | key: <value> pair |
| array | Yes | Yes | [element1, element2, ...] |
| tuple | Yes | No | [name, age] - fixed **length** and **type** |
| enum | Yes | No | enum { NEW, OLD } - enumerated lists, a list of label-value pairs |
| any | Yes | No | takes on any type (default JavaScript behaviour) |
| union | Yes | No | mixed type variables |
| literal | Yes | No | an exact value as a type (eg 2, "pair", 6.6) | 
| void | Yes | No | No return statement (vs return statement without a value, ie undefined) |
| function | Yes | No | a function |

## Notes
- TypeScript's type system only helps you *during development* (ie before the code gets compiled). It's a *sanity check*.
- By default, TypeScript does not block compilation into JavaScript if errors are present.
- Although TypeScript can statically type variables during development, it can still fail at runtime because it's compiled to JavaScript. 
  However, it's still advantageous because we know that the error can be narrowed down to issues caused at runtime rather than during development 
  (ie eliminating a set of possible   causes). This saves a lot of troubleshooting time.
 - Variable assignment doesn't require explicit definition of their type because TypeScript has a feature called **type inference**. TypeScript does its best to understand which    type is being assigned. However, it's good practice to include when a value hasn't been clearly defined for the variable (ie when type cannot be inferred).

## Tips
- When working in TypeScript keep the compiled JavaScript file closed to prevent error messages on duplicate implementations.
- Explicitly annotating an object as 'object' will throw errors if you try to access the properties. This is because 'object' doesn't provide information about the properties.
