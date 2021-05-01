# rad-arrays

```js
const rad = require('@hurly77/rad-arrays')

const myArray = rad.array('string', 20)
console.log(myArray)

//=>
[
  'm', 'd', 't', 'w', 'i',
  's', 'w', 'k', 'z', 'm',
  'r', 's', 'o', 'j', 'z',
  'u', 'q', 'q', 'q', 'r'
]
```

RadArrays take two arguments, data-type `string`, `array`, `integer`, `object`
and a integer of how many items you'd like in the array.

you can also specify a fixed data set such like so:
```js
const rad = require('@hurly77/rad-arrays')

const myArray = rad.fixedArray(10)
console.log(myArray)
//=>
[
  0, 0, 0, 0, 0,
  0, 0, 0, 0, 0
]
//or
const myArray = rad.fixedArray(10, {myObject: "hello"})
console.log(myArray)

//=>
[
  { myObject: 'hello' },
  { myObject: 'hello' },
  { myObject: 'hello' },
  { myObject: 'hello' },
  { myObject: 'hello' },
  { myObject: 'hello' },
  { myObject: 'hello' },
  { myObject: 'hello' },
  { myObject: 'hello' },
  { myObject: 'hello' }
]

//do to human error the first argument will be the number of Items and the second will be the fixed data set you'd like to be generated.
```

if your wanted to implement a pattern for example if you wanted to return `0, 1, 0, 1` pattern
all you'd have to do is call `Array.prototype.flat()`

```js
let a = [0, 1]
const myArray = rad.fixedArray(10, [0, 1]).flat()
console.log(myArray)
```

This is a custom library I'm working on for data structures and algorithms, I'm using it in a couple of files just to try and break my code.
