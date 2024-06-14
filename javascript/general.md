#### overview of how different attributes work for loading javascript

![](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript/async-defer.jpg)


#### OOP principles 

- Single responsibility principle
- loose coupling using the pub/sub principles

[[1]](https://www.theodinproject.com/lessons/node-path-javascript-oop-principles#single-responsibility) [[2]](https://www.ayweb.dev/blog/building-a-house-from-the-inside-out) [[3]](https://sandimetz.com/products)


### Async code

#### promises

no need of explanation when code is the best explanation.
```js
var p = new Promise(function(resolve, reject) {
	
	// Do an async task async task and then...

	if(/* good condition */) {
		resolve('Success!');
	}
	else {
		reject('Failure!');
	}
});

p.then(function(result) { 
	/* do something with the result */
}).catch(function() {
	/* error :( */
}).finally(function() {
   /* executes regardless or success for failure */ 
});
```