# TypeScript

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
## Syntax
### Annotations
Function parameters
```typescript
function doSomething(num: number, phrase: string, flag: boolean) {

}
```
Variable assignment
- Typically good practice when type cannot be *inferred*.
```typescript
const num: number;
let word: string;
```
## Available Types
| Type | TypeScript | JavaScript | Notes |
| --- | --- | --- | --- |
| number | Yes | Yes | integers, floats, etc... are all the same |
| string | Yes | Yes | text |
| boolean | Yes | Yes | true/false |
| object | Yes | Yes | key: <value> pair |

## Notes
- TypeScript's type system only helps you *during development* (ie before the code gets compiled). It's a *sanity check*.
- By default, TypeScript does not block compilation into JavaScript if errors are present.
- Although TypeScript can statically type variables during development, it can still fail at runtime because it's compiled to JavaScript. 
  However, it's still advantageous because we know that the error can be narrowed down to issues caused at runtime rather than during development 
  (ie eliminating a set of possible   causes). This saves a lot of troubleshooting time.
 - Variable assignment doesn't require explicit definition of their type because TypeScript has a feature called **type inference**. TypeScript does its best to understand which    type is being assigned. However, it's good practice to include when a value hasn't been clearly defined for the variable (ie when type cannot be inferred).
 - Explicitly annotating an object as 'object' will throw errors if you try to access the properties. This is because being explicit indicates we have an object where we don't      give any information to TypeScript.

## Tips
- When working in TypeScript keep the compiled JavaScript file closed to prevent error messages on duplicate implementations.

