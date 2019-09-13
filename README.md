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
