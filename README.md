# music-player
 Learn some essential string and array methods like the find(), forEach(), map(), and join().
In this project, code a basic MP3 player using HTML, CSS, and JavaScript. The project covers fundamental concepts such as handling audio playback, managing a playlist, implementing play, pause, next, previous, and shuffle functionalities. Learn how to dynamically update your user interface based on the current song.

### Web Audio API
 All modern browsers support the Web Audio API, which lets you generate and process audio in web applications.

Use `const` to create a variable named `audio` and set it equal to `new Audio()`. This will create a new HTML5 `audio` element.

`play()` is a method from the web audio API for playing an mp3 file.

`pause()` is a method of the Web Audio API for pausing music files.

### Spread Operator
The spread operator (...) allows you to copy all elements from one array into another. It can also be used to concatenate multiple arrays into one. In the example below, both `arr1` and `arr2` have been spread into `combinedArr`:

```
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const combinedArr = [...arr1, ...arr2];
console.log(combinedArr); // Output: [1, 2, 3, 4, 5, 6]
```
### Arrow function
An arrow function is an anonymous function expression and a shorter way to write functions. Anonymous means that the function does not have a name. Arrow functions are always anonymous.
`() => {}`

To create a named arrow function, you can assign the function to a variable:
```
const exampleFunction = () => {
  // code goes here
}
```

To call a named arrow function expression, you can reference the function by its name.
`exampleArrowFunction();`

Just like regular functions, arrow functions can accept multiple parameters.
Here is an example of a named arrow function with one parameter:
```
const greet = (name) => {
  console.log(`Hello, ${name}!`);
};
```
If the function only has one parameter, you can omit the parentheses around the parameter list like this:
```
const greet = name => {
  console.log(`Hello, ${name}!`);
};
```

Just like regular functions, arrow functions can return values.

Here is an example of an arrow function returning the result of multiplying two numbers:
```
const multiplyTwoNumbers = (num1, num2) => {
  return num1 * num2;
}
// Output: 12
console.log(multiplyTwoNumbers(3, 4)); 
```

If the arrow function is returning a simple expression, you can omit the return keyword and the curly braces {}. This is called an implicit return.
`const multiplyTwoNumbers = (num1, num2) => num1 * num2;`

If your arrow function has multiple lines of code in the function body, then you need to use the return keyword and the curly braces {}.
```
const getTax = (price) => {
  const taxRate = 0.08;
  const tax = price * taxRate;
  return tax;
};
```
###  map() method
The map() method is used to iterate through an array and return a new array. It's helpful when you want to create a new array based on the values of an existing array. For example:
```
const numbers = [1, 2, 3];
const doubledNumbers = numbers.map((number) => number * 2); // doubledNumbers will be [2, 4, 6]
```

Notice that the `map()` method takes a function as an argument. This is called a **_callback function_**, which is a function that is passed to another function as an argument. In the example above, the callback function is `(number) => number * 2`, and it's run on each element in the `numbers` array. The `map()` method then returns a new array with the results.

###  join() method
The join() method is used to concatenate all the elements of an array into a single string. It takes an optional parameter called a separator which is used to separate each element of the array. For example:
```
const exampleArr = ["This", "is", "a", "sentence"];
const sentence = exampleArr.join(" "); // Separator takes a space character
console.log(sentence); // Output: "This is a sentence"
```

### sort() method
The sort() method converts elements of an array into strings and sorts them in place based on their values in the UTF-16 encoding.
```
const names = ["Tom", "Jessica", "Quincy", "Naomi"];
names.sort() // ["Jessica", "Naomi", "Quincy", "Tom"]
```
To sort alphabetical order, you will need to pass in a compare callback function into your sort() method.
####  In alphabetical order
Example 1: Sorting Strings Lexicographically
```
const fruits = ['Banana', 'Apple', 'Cherry'];

fruits.sort((a, b) => {
    if (a < b) return -1; // `a` comes before `b`
    if (a > b) return 1;  // `a` comes after `b`
    return 0;             // `a` and `b` are equal
});

console.log(fruits);
// Output: ['Apple', 'Banana', 'Cherry']
```
Example 2: Sorting Numbers
```
const numbers = [40, 100, 1, 5, 25, 10];

// Sort numbers in ascending order
numbers.sort((a, b) => a - b);

console.log(numbers);
// Output: [1, 5, 10, 25, 40, 100]
```
#### Randomize an array
Another use case for the callback function is to randomize an array.
One way to randomize an array of items would be to subtract 0.5 from Math.random() which produces random values that are either positive or negative. This makes the comparison result a mix of positive and negative values, leading to a random ordering of elements.
```
const names = ["Tom", "Jessica", "Quincy", "Naomi"];
names.sort(() => Math.random() - 0.5);
// Output: ['Naomi', 'Quincy', 'Jessica', 'Tom']
```
### optional chaining operator
Without Optional Chaining
```
const userData = null;
console.log(userData.songs); 
// Throws an error: Cannot read properties of null (reading 'songs')
```
With Optional Chaining
```
const userData = null;
console.log(userData?.songs); 
// Output: undefined (no error)
```
### find() method
The find() method retrieves the first element within an array that fulfills the conditions specified in the provided callback function. If no element satisfies the condition, the method returns undefined.
```
const numbers = [10, 20, 30, 40, 50];

// Find the first number greater than 25
const foundNumber = numbers.find((number) => number > 25);
console.log(foundNumber); // Output: 30
```
###  indexOf() method
The indexOf() array method returns the first index at which a given element can be found in the array, or -1 if the element is not present.
```
const animals = ["dog", "cat", "horse"];
animals.indexOf("cat") // 1
```
### forEach method
The forEach method is used to loop through an array and perform a function on each element of the array. For example, suppose you have an array of numbers and you want to log each number to the console.
```
const numbers = [1, 2, 3, 4, 5];

// Using forEach to iterate through the array
numbers.forEach((number) => {
  console.log(number); // 1, 2, 3, 4, 5
});
```
### textContent
`textContent` sets the text of a node and allows you to set or retrieve the text content of an HTML element.
```
<div id="example">This is some text content</div>

const element = document.getElementById('example');
console.log(element.textContent); // Output: This is some text content
```
### filter() method
 used to create a new array containing all the elements of the original array that pass a specified condition (predicate function). This method does not modify the original array and returns a new array.
 ```
 const numArr = [1, 10, 8, 3, 4, 5]
const numsGreaterThanThree = numArr.filter((num) => num > 3);

console.log(numsGreaterThanThree) // Output: [10, 8, 4, 5]
```
### createElement()
`createElement()` is a DOM method you can use to dynamically create an element using JavaScript. To use createElement(), you call it, then pass in the tag name as a string:
```
// syntax
document.createElement(tagName)

// example
document.createElement('div')
```
You can also assign it to a variable:
```
const divElement = document.createElement('div')
```
The `createTextNode()` method is used to create a text node. To use it, you call it and pass in the text as a string:
```
const myText = document.createTextNode("your text")
```

### Setting id and aria-label
```
// Create an element
const button = document.createElement("button");

// Set id and aria-label attributes
button.id = "submitButton";
button.ariaLabel = "Submit the form";

// Add text content
button.textContent = "Submit";

// Append to the body (or another element)
document.body.appendChild(button);

console.log(button); 
// <button id="submitButton" aria-label="Submit the form">Submit</button>
```

### appendChild()
`appendChild()` lets you add a node or an element as the child of another element. In the example below, the text "Click me" would be attached to the button:
```
const parentElement = document.createElement("button")
const parentElementText = document.createTextNode("Click me")

// attach the text "Click me" to the button
parentElement.appendChild(parentElementText)
```