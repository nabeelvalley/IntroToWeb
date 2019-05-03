# Arrays, Loops and Events

# Arrays

Before we get into loops, there's something we haven't discussed yet

- Used in many different programming languages
- Store a collection of items

```js
var myArray = [1,2,3,4]
```

- An array can story any collection of objects
- Contained in `[]`
- Elements separated by `,`

```js
var students = [
    {
        name: 'John',
        age: 12
    },
    {
        name: 'Jenny',
        age: 72
    }
]
```

We can also access a specific value of an array using `[index]`

```js
var john = students[0]
var jenny = students[1]
```

> Indexes start at `0`

Arrays also have a variety of properties and functions such as

```js
var array = [5,1,'hello',4]

var howManyItems = array.length

var sortedArray = array.sort()
```

> Let's make an array and see what we can do

Some array functions make use of a function that we create in order to do something with the array, such a `map`

```js
var students = [
    {
        name: 'John',
        age: 12
    },
    {
        name: 'Jenny',
        age: 72
    },
    {
        name: 'Jeff',
        age: 3
    }
]

function studentToNames(student){
    var studentName = student.name
    document.write(studentName, '</br>')

    return studentName
}

var names = students.map(studentToNames)

document.write(names, '</br>')
```

# Loops

Loops allow us to repeat something multiple times, we have a few different kinds of loops

In this class we will cover For Loops

## For Loops

They consist of the following:

- Counter - `index`
- Start Value - `var index = 1`
- End Value - `index < 10`
- Stuff to do

```js
for (var index = 0; index < 10; index++) {
    const value = index
    document.write(value, '</br>')
}
```

Or, we can iterate through an array one element at a time

```js
for (var index = 0; index < array.length; index++) {
    const element = array[index];
    document.write(element, '</br>')
}
```

# Events

As we saw before, elements like buttons have events that we can use to make stuff happen such as `onclick`

We can do stuff when an `event` happens by `listening` to our webpage and then doing something with an `event handler`

An `event listener` can be created with

```js
function eventHandler(){
    console.log(event, '</br>')
}

document.addEventListener('click', eventHandler)
```

> There's a lot of them, [listed here](https://www.w3schools.com/jsref/dom_obj_event.asp)