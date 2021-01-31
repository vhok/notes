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

## Available Types
| Type | TypeScript | JavaScript | Notes |
| --- | --- | --- | --- |
| number | Yes | Yes | integers, floats, etc... are all the same |
| string | Yes | Yes | text |
| boolean | Yes | Yes | true/false |
| object | Yes | Yes |  |

## Notes
- TypeScript's type system only helps you *during* development (ie before the code gets compiled). It's a *sanity check*.
- By default, TypeScript does not block compilation into JavaScript if errors are present.
- Although TypeScript can statically type variables during development, it can still fail at runtime because it's compiled to JavaScript.  
  However, it's still advantageous because we know that the error can be narrowed down to issues caused at runtime rather than during development  
  (ie eliminating a set of possible causes). This saves a lot of troubleshooting time.

## Tips
- When working in TypeScript keep JavaScript file closed to prevent error message of duplicate implementations.

