# Promises-in-js
Promises in the JavaScript 

Promises in JavaScript are used to use the javascript Single Threaded very wisely.
in which a promise takes a argument as a function (a call back) with 2 parameters namely 

1. Resolve
2. Reject

+ Resolve in sense that the callback is a sucess.
+ Reject in sense that the callback is a failure.

so Defining a simple promise loks like this 

```javascript
let mypromise=new Promise(function(resolve,reject){
        //resolve();
        //or
        //reject();
});
```
# Using a promise in the program
  
  promises are mainly used in the program when we want a task to be started only the other task is completed
  usually events are used to do this kind on stuff in js, but it becoms messy for large number of events so
  promises may be used to improve the readability of the program and reduces nightmares
  
  using a promise in a js program is as follows
```javascript
//defining a promise
let mypromise=new Promise(function(resolve,reject){
			var d = new Date();
			console.log("called a function at the time of "+d.getSeconds());
			setTimeout(function(){return resolve();}, 2000);
 	    	  });

//using the promise
mypromise.then(function(){
 			var d = new Date();
			console.log("promise resolved at "+d.getSeconds());
	  })
	 .catch(function(){
	  	var d = new Date();
	  	console.log("promise failed "+d.getSeconds())
	});
```

#output:-
```html
 called a function at the time of 54
 promise resolved at 56
```

in the above program when the promise is resolved then the then callback is executed and if it is rejected catch callback is executed
as the promise alwase resolve the then call back is executed.

# Where promises are used 
+ Promises are mostly used in place of events when two functions are dependent on each other.
+ Service Worker Api mainly uses the promises .

# Best video explanation
<a href="https://www.youtube.com/embed/s6SH72uAn3Q?list=PLYswWC54mIBiBNczi4gcc4yjBIHh4OhDz&amp;ecver=1">Promise Explained The Best Video </a>
