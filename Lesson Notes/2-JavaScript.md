# Introduction to JavaScript

Programming languages are how we tell the computer to do things

Javascript allows us to do things on our Web Pages

We include Javascript in a `script` tag on our Website

> Say hello by adding a `script` tag to our page:

```html
<script>
    document.write('<h1>Hello, Javascript!</h1>')
</script>
```

`document.write` is a `function` that allows us to add content to a page, we'll learn more about functions in a bit

### Objects

> EVERYTHING IS AN OBJECT

Some examples of objects are

```js
83            // Number Obect

"Hello world" // String Object

{             // Person Object
    name: "John",
    age: 82,
    email:  "john@mail.com"
}
```

`document` is an object, this object has a `function` called `write`

> Looks a bit like CSS right?

### Variables

Variables in programming are like in math, they simply allow us to save a specific object

Variables allow us to save an object and use it later

We use `let` and the name of our variable to create a variable

```js
let number = 83
let text = "Hello world"
let person = {
    name: "John",
    age: 82,
    email:  "john@mail.com"
}
```

> Let's create and print a variable to the screen using `document.write`

```html
<script>
    let greeting = "Hello, World!"
    document.write(greeting)
</script>
```

> Variables can be used in place of objects as we can see above

### Functions

Functions are just like other objects. We crreate a function using the `function` keyword, and including its `parameters`

```js
let print = function (stuffToPrint) {
        document.write(stuffToPrint)
    }
        
print("Hello, World")
```

### Events

JavaScript is `event-driven`, we use events to devide what to do, this is done with 

```js
doument.addEventListener('event name', eventHandler)
```

However different HTML elements have their own built-in events, such as a button which has an `onclick` event which we can chose to use a function to deal with - this can be done as follows

```html
<button onclick="doStuff()"></button>
<script>
    let doStuff = function() {
        // Do some stuff
    }
</script>
```

### Updating HTML Elements

Using JS we can update the Elements that are on our page by using the `document.getElementById` function which takes in a name of an element we want to use

We can save an element to a variable with

```js
let myElement = document.getElementById('myElementId')
```

We can then update things such as the element's HTMl or InnerText with

```js
myElement.innerHTML = '<h1>Hello World</h1>'
myElement.innerText = 'Hello World'
```

In the case of Input Elements we can also get the current value from our input, this can be done as follows

```js
let inputElement = document.getElementById('myInputElementId')
console.log(inputElement) // Will print the content of the input element
```