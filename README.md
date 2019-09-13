## Table Of Contents

1. [Var, let and Const]()
2. [Template literals]()
3. [Default Arguments]()
4. [Arrow Functions]()
5. [Array and Object Destructuring]()
6. [Iterables and Looping]()
7. [Array - Map, Reduce, Filter]()
8. [Rest and Spread Operator]()
9. [Object Literals]()
10. [Classes in ES6]()
11. ["this" and "new" keyword]()
12. [Promises and Callback Hell]()
13. [Async and Await]()
14. [Map and Weak Map]()
15. [Sets and WeakSets]()

### 1. Var, let and const

**1.1 VAR**

- var keywords

**1.2 LET**

- "let" is used when you have to change the value of the variable later in the code.
- It has block scope.
- It can be re-initialised but not re-declared.

```
    let a = 10;

    // re-initialization
    a = 30; // Updating a value to 30.

    //re-declartion
    let a = 20; // Throws Error

    // Block 1
    {
    	 let c = 10;
    	 console.log(c); // c=10
    }

    console.log(c); // Throws Error, c not defined.
```

**1.3 CONST**

- Const is used to define a constant variable which can't be changed throught the code.
- It has block scope.
- You can neither be re-initiased nor re-declared.

```
    const a = 10;

    // re-initialization
    a = 30; // Throws Error, CONST variable can't be changed

    //re-declartion
    const a = 20; // Throws Error

    // Block 1
    {
    	 const c = 10;
    	 console.log(c); // c=10
    }

    console.log(c); // Throws Error, c not defined.
```

### 2. Template Literals (Template Strings )

---

Template literals are string literals allowing embedded expressions. You can use multi-line strings and string interpolation features with them. They were called "template strings" in prior editions of the ES2015 specification.

Template literals are basically the formatting of string in javascript. In ES5, formatting string was a tedious task as it involved a very manual formatting syntax.

Let's see an example how we used to format string in ES5.

```
    # TEMPLATE STRING (WITHOUT ES6)

    function greet(name){
    	const greeting = 'Hello,' + ' ' + name + ' ' + Welcome to JavaScript Course;
    	return greeting;
    }

    greet('Deepak');

    // Hello, Deepak Welcome to JavaScript Course.
```

```
    # TEMPLATE STRING (WITH ES6)

    function greet(name){
    	const greeting = `Hello, ${name} Welcome to JavaScript Course`;
    	return greeting;
    }

    greet('Deepak');

    // Hello, Deepak Welcome to JavaScript Course.

```

Now, you see the diffference how easy it is to use format string with ES6 new syntax.

**RECAP**

- Template String are enclosed by back tick(``) instead of single or double quote.
- Template literals can contain placeholders. These are indicated by the dollar sign and curly braces (\${expression}). The expressions in the placeholders and the text between the back-ticks (``) get passed to a function.

### 3. Default Arguments

---

Default argument or default parameter is the new feature in ES6. It allows you to set a default value for your function parameter/argument if **no value** or **undefined** of is passed.

**Handling Default Argument with ES5**

```
    function add(a, b){
    		return a + b;
    }

    add() // NaN

    // Handling Default Argument without ES6.

    function add(a, b){
    	const a = (typeof(a) !== 'undefined') ? a : 5;
    	const b = (typeof(b) !== 'undefined') ? b : 10;
      return a+b;
    }

    add() // Returns 15
```

When no parameter is passed you can see we have to explicitly handle the error by setting default values of a & b. This doesn't look like a favourable way of handling default arguments.

**Handling Default Argument with ES6**

```
    function add(a=5, b=10){
    	return a+b;
    }

    add(); // a=5, b=10, sum = 15;

    add(2, 3); // a=2, b=3, sum = 5;

    add(4); // a=4, b=10, sum=14 ;
```

Default value of A and B will be only used when no parameter is passed.

### 4. Arrow Functions

---

An arrow function is a syntactically compact alternative to a regular function expression without its own binding to `this`, `super`,

```
**Using Regular Function Express (ES5)**

    // Example 1
    function add(a, b){
    	return a+b;
    }

    add(5, 10);

    // Example 2

    const x = [1, 2, 3, 4, 5];

    const square = x.map(function(x){
    	return x*x;
    });

    console.log(sqaure);
```

**Using Arrow Functions (ES6)**

```
    // Example 1
    const add = (a, b) => {
    		return a+b;
    }

    add(5, 10)

    //Example 2

    const x = [1, 2, 3, 4, 5];

    const square = x.map(num => num*num);
    console.log(sqaure);
```

### 5. Array and Object Destructuring

Destructuring is a new feature introduced in ES6 to unpack values from arrays or properties from object. It helps in improving the readability and performance of our code.

**Destructuring in ES5**

```
    // Example 1 - Object Destructuring

    var user = {
    	name : 'Deepak',
      username : 'dipakkr',
      password : 12345
    }

    const name = user.name; // Deepak
    const username = user.username; // dipakkr
    const password = user.password // 12345

    //Example 2 - Array Destructing

    *c*onst fruits = ["apple", "mango", "banana", "grapes"];

    const fruit1 = fruits[0];
    const fruit2 = fruits[1];
    const fruit3 = fruits[2];
```

**Destructuring in ES6**

```
    // Example 1 - Object Destructuring

    var user = {
    	name : 'Deepak',
      username : 'dipakkr',
      password : 12345
    }

    const {name, username, password} = user;
    console.log(name);
    console.log(username);
    console.log(password);

    //Example 2 - Array Destructing

    const fruits = ["apple", "mango", "banana", "grapes"];

    const [fruit1, fruit2, fruit3] = fruits;

    console.log(fruit1); // apple
    console.log(fruit2); // mango
    console.log(fruit3); // banana
```

---

### [About the Author]()

Hi, I am Deepak Kumar, a Full Stack JavaScript Developer, Freelancer and an aspiring Entrepreneur. I love building product that has real impact in society.

Let's connect here to know more about me.

Follow me on - | [LinkedIn]() | [Instagram]() | [Twitter]()

---
