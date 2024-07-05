## Recursion

Every function has a **execution context**. Execution context is just a internal data structure storing the details of function execution (somewhat like lexical enviroment for closures)

A function has only one **execution context**.

>**Base Case** is the only explicit solution of the recursive function.

### Nested Functions Working

1. Function is paused
2. Execution context is saved for the current function in **Execution stack**.

3. Nested function executes
4. Old function is executed for which execution context is saved.

So the way recursion works is the function stops when the next function is called and that execution context is pushed to the stack for later execution

#### Uses of recursion

Linked lists, DOM Tree traversing

[https://javascript.info/recursion](https://javascript.info/recursion)