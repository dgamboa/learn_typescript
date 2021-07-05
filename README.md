# Notes on TypeScript

## Codecademy
Source: [Codecademy Course](https://www.codecademy.com/courses/learn-typescript/lessons/introduction-to-typescript/exercises/from-javascript-to-typescript)

### From JavaScript to TypeScript
- Brief History: Microsoft developed TypeScript (released in 2012) to blend the flexibility of JavaScript with the advantages of stricter languages.
- TypeScript adds types, which allows the compiler to spot and call out bugs that might otherwise fail silently.
- Write the code in a `.ts` file and run `tsc` in the terminal to compile into `.js`.
- When a variable is assigned, the type of the assigned value is enforced for the life of the variable.
- We can also assign types directly (e.g. `let name : string`).
- TypeScript also enforces shape; that is, what properties and methods it has based on its type.
- We can avoid type assignment by declaring a variable with assigning it (e.g. `let onOrOff`).

### The tsconfig.json File
- Configuration file that contains the rules for the compiler to enforce
- The rules are expressed in JSON
- Allows compilation of TypeScript files by running `tsc` in the terminal
- Example of `tsconfig` file:
```
{
  "compilerOptions": {
    "target": "es2017",
    "module": "commonjs",
    "strictNullChecks": true
  },
  "include": ["**/*.ts"]
}
```

### Default Parameters
- In the context of functions, TypeScript can help enforce argument types.
- The basic syntax is `function greet(name : string) {...}`.
- Arguments without an explicit type will be type `any`.
- Optional parameters can be denotes with a `?` as in `...(name?: string)...`.
- Alternative, default parameters can be passed in, which will automatically set the argument's type to the default parameter and make the argument optional (e.g. `(name = 'Anonymous')`).
- Returns also imply a type that will be set for the variables assigned to a function call.

### Explicit Return Types
- We can enforce a function return type with `function greet(name : string): string {...}`.
- If a function doesn't return anything, its return type should be `void`.

