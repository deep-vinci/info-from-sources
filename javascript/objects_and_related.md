### Objects

- object constructors - to replicate same objects multiple instances, this saves the data just like closures but more inefficiently
- object prototype 
```
[[prototype]] 
- all the native and user built objects have this property by default
- can be accessed using Object.getProtoypeOf(objX) / objX.__proto__
- for object constructors like Array, Date they can be accessed using Array.prototype
- protypal inheritance is set using Object.setPrototypeOF(inherit ,inheriting from) 
- this basically saves the prototype of second obj to first one so if you have a function in the first object it will be inherited to second object

- isPrototypeOf(), instanceof()
```
#### uses of proto
- functions can be attached to objects .prototype to minimize mem usage as it's function is not initiated with every new object instance
- instances can inherit properties from the parent objects


[[1]](https://www.theodinproject.com/lessons/node-path-javascript-objects-and-object-constructors) [[2]](https://www.digitalocean.com/community/tutorials/understanding-prototypes-and-inheritance-in-javascript) [[3]](https://javascript.info/class#not-just-a-syntactic-sugar)

### Closure
[bro code closure, yt](https://www.youtube.com/watch?v=80O6L2Ez3GM)
```
Closures 
    A function with preserved data.
    Gives you access to an outer function's scope from inner function.

    - state of variable in outer scope are "saved" (lexical environemnt - which has all the local variables decl inside it)

    - variable in outer scope are "private" unless returned expicitly (ex 1)

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
##### fantastic usecase of closures
```js
const Player = (name, level) => {
    let health = level * 2;
    const getLevel = () => level;
    const getName  = () => name;
    const die = () => {
      // uh oh
    };
    const damage = x => {
      health -= x;
      if (health <= 0) {
        die();
      }
    };
    const attack = enemy => {
      if (level < enemy.getLevel()) {
        damage(1);
        console.log(`${enemy.getName()} has damaged ${name}`);
      }
      if (level >= enemy.getLevel()) {
        enemy.damage(1);
        console.log(`${name} has damaged ${enemy.getName()}`);
      }
    };
    return {attack, damage, getLevel, getName};
  };
  
  const jimmie = Player('jim', 10);
  const badGuy = Player('jeff', 5);
  jimmie.attack(badGuy);
```
#### Closures vs Function Factories
```
- All functions in JavaScript are closures so by having a function you also have a closure. 

-Factory functions are a specialized kind of function whose purpose is to create new objects. 

Not all functions are factories but all factories, since they're functions, are closures. Additionally not all factories would make use of closure variables so if they aren't dependent on themselves being closures.

```
#### Factory function
they levy the power of closures. Instead of using the new keyword to create an object, factory functions set up and return the new object when you call the function. 

#### encapsulation 

```
using IIFE we can create namespaces that reduce variable name pollution in the main code base

- for this module pattern exists as well, where you can use different files for different functions and just invoke them
```

