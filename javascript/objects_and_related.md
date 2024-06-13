
[bro code closure, yt](https://www.youtube.com/watch?v=80O6L2Ez3GM)
```
Closures 
    A function with preserved data.
    Gives you access to an outer function's scope from inner function.

    - state of variable in outer scope are "saved" (lexical environemnt - which has all the local variables decl inside it)

    - variable in outer scope are "private" unless returned explicitly (ex 1)

```

```js
function outer() {
    const outerVariable = 1;

    return { outerVariable }
}

// this is valid as the variable is returned and can only be called from method closure, making it private
let closure = outer();
closure.outerVariable;
```

