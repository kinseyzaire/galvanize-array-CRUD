Perform CRUD (create, read, update, delete) operations with arrays.

### Create elements

To create an array, we type two characters: an open square bracket and a closing square bracket:

```javascript
[]
```

Similar to primitive types, we need to set our array to a variable if we want to access it at a later time. Let's rewrite the above code with a `var` statement:

```javascript
var myArray = [];
```

The syntax we're using to create our array is referred to as an array literal. To be more specific, our array literal is considered to be an empty array literal. We describe it as empty because arrays are designed to store sequences of data, which include reference types, primitives types, or both.

Let's create an array literal and store four strings inside of it:

```javascript
var myArray = ["Yoda", "Vader", "Skywalker", "Leia"];
```

For the syntax to be valid, each value needs to be delimited with commas.

### Read Elements

To access and read each element in the array, we need to use square bracket notation with an index. Indexes are typically Numbers.

```javascript
var myArray = ["Yoda", "Vader", "Skywalker", "Leia"];

myArray[0] // "Yoda"
myArray[1] // "Vader"
myArray[2] // "Skywalker"
myArray[3] // "Leia"
```

Notice that the index starts with `0` and then increments by `1` This sequence gives us a great mental model of an element's index. Moreover, it gives us a glimpse into how an array's elements are stored in memory--as a block.

### Update elements

To update a value stored at a specific index, we need to take a two step process. First, we need to access the desired element. Second, we need to set that element to a new value:

```javascript
var myArray = ["Yoda", "Vader", "Skywalker", "Leia"];

myArray[0] = "Obi-Wan";
=> ["Obi-Wan", "Vader", "Skywalker", "Leia"];
```

### Delete elements

To delete a value stored at a specific index, we'll use `splice` with the following syntax:

```javascript
var myArray = ["Obi-Wan", "Vader", "Skywalker", "Leia"];

myArray.splice(1, 1)
=> [ 'Vader' ]
```
Notice, the `splice` function returns to us the item that was deleted (in this case Vader because he is evil), not the array it was removed from. It is also important to note that the `slice` function mutates the original array and myArray now returns `[ 'Obi-Wan', 'Skywalker', 'Leia' ]`
