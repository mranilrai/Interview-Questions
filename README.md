# Front-End: Interview-Questions
Interview questions asked related to Javascript, ReactJs, Design System, UI Design Patterns(MVC, MVVM, MVP), Design Patterns, General

# Javascript
  ```
  Question: Explain how 'this' works in javascript.
  
  Answer: The value of this depends on how the function is called. The following rules are applied:
  
    1. If the 'new' keyword is used when calling the function, this inside the function is a brand new object.
    2. If apply, call, or bind are used to call/create a function, this inside the function is the object
       that is passed in as the argument.
    3. If a function is called as a method, such as obj.method() — this is the object that the function is 
       a property of.
    4. If a function is invoked as a free function invocation, meaning it was invoked without any of the 
       conditions present above, this is the global object. In a browser, it is the window object.
       If in strict mode ('use strict'), this will be undefined instead of the global object.
    5. If multiple of the above rules apply, the rule that is higher wins and will set the this value.
    6. If the function is an ES2015 arrow function, it ignores all the rules above and receives the this
       value of its surrounding scope at the time it is created.
  ```
  ```
  Question: Explain how prototypal inheritance works.
  
  Answer: JavaScript only has one construct: objects. Each object has a private property (__proto__, 
  prototype in case of function) which holds a link to another object called its prototype. That prototype object 
  has a prototype of its own, and so on until an object is reached with null as its prototype. By definition, 
  null has no prototype, and acts as the final link in this prototype chain.
  ```
  ```
  Question : What is call and apply?
  
  Answer: Both .call and .apply are used to invoke functions and the first parameter will be used as the value
  of this within the function. However, .call takes in comma-separated arguments as the next arguments 
  while .apply takes in an array of arguments as the next argument. 
  
  
  function add(a, b) {
    return a + b;
  }
  console.log(add.call(null, 1, 2)); // 3
  console.log(add.apply(null, [1, 2])); // 3
  
  Second Example:
  const user = {
  	fname: "Anil",
	lname: "Rai"
  };
  
  function greet(greeting){
  	return greeting + ' ' + this.fname + ' ' + this.lname;
  }
  console.log(greet.call(user, 'Hi')); // Hi Anil Rai
  console.log(greet.apply(user, ['Hi'])); // Hi Anil Rai
  ```
  ```
  Question : What is bind?
  ```
  ```
  Question : Differance between let and var?
  ```
  ```
  Question : What is hoisting?
  ```
  ```
  Question : What is closure?
  ```
  ```
  Question : What is IFFI?
  ```
  ```
  Question : What is prototype?
  ```
  ```
  Question : What is event loop?
  ```
  ```
  Question : What is event delegation?
  
  Answer: Event delegation is a technique where we bind the event listener to the parent element instead
  of the child element.That event listener analyzes bubbled events to find a match on child elements.
  ```
  ```
  Question : What is event propagation?
  
  Answer: Event propagation deals with three event phases capturing, target and bubbling. In the capturing phase,
  events propagate from the Window down through the DOM tree to the target node. In the bubbling phase event 
  bubbles back up the DOM tree, from the target element up to the Window.
  ```
  <img width="300" alt="Event propagation" src="https://user-images.githubusercontent.com/4344538/93660959-aaae0080-fa71-11ea-8977-e01ddfcf0231.png">
  
  ```
  Question : What is Object.is?
  ```
  ```
  Question : What is Debounce and throttling, write code for both?
  ```
  ```
  Question : Write polyfill for map, filter and reduce method?
  ```
  ```
  Question : Write polyfill for bind, call and apply?
  ```
  ```
  Question : Write code for add(1)(2)(), add(1,2)(3)()?
  ```
  ```
  Question : Write code for add(1)(2)(3), add(1,2)(3)?
  ```
  ```
  Question : What will be the value of this in below code?
	
		const a = {
			getMe(){
				console.log(this);
			},
			getMeAgain: () => {
				console.log(this);	
			}
		}
		a.getMe();
		a.getMeAgain();
		
		const b = () => {
			console.log(this);
		};
		a.c = b;
		a.c();
	
  ```
# ReactJs
  ```
  Question : What is virtual DOM?
  ```
  ```
  Question : How lifecycle methods are available to class components?
  ```
  ```
  Question : Why lifecycle methods where not available to functional components?
  ```
  ```
  Question : What we import React in functional components?
  ```
  ```
  Question : How we can do deep check in useeffect dependency array?
  ```
  ```
  Question : What will happen if we execute three setState({a: 1})?;
  ```
  ```
  Question : Lifecycle methods in react?
  ```
  ```
  Question : How to achive lifecycle methods in functional components?
  ```
  ```
  Question : What is higher order component?
  ```
  ```
  Question : Lifecycle methods in react?
  ```
  ```
  Question : What is pure component?
  ```
  ```
  Question : What is controlled and uncontrolled component in react?
  ```
  ```
  Question : How to do route and component level code spliting?
  ```
  ```
  Question : How to do SSR?
  ```
  ```
  Question : Why do we need a key property? Give an example when a bad key causes an error.?
  ```
# Redux
 ```
 Question : How redux works?
 ```
 ```
 Question : Whether redux lifecycle is synchronous or asynchronous?
 ```
 ```
 Question : How to achive asynchronous in redux?
 ```
 ```
 Question : What is middleware in Redux?
 ```

# Design System

# UI Design Patterns(MVC, MVVM, MVP)
	```
	Question: What is MVC, MVVM, MVP?
	```

# Design Patterns

# Genaral
	```
	How to make a component bug free in production?
	```
	```
  	Question : How to do performance optimization?
  	```
