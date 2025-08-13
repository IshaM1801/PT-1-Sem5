JavaScript Objects
In JavaScript, an object is a standalone entity that holds multiple values in the form of properties and methods. A property is an association between a name (or key) and a value, and a method is a function stored as a property of an object. Objects allow developers to group related data and functionality together, making programs more organized and easier to maintain.
Objects can represent real-world entities (like a car, a student, or a book) or conceptual entities (like mathematical operations, collections of data, or dates).

---------Creating JavaScript Objects
Using Object Literals
let car = {
brand: "Toyota",
model: "Camry",
year: 2023,
start: function() {
console.log("Car started");
}
};
Using the new Object() Constructor
let person = new Object();
person.name = "John";
person.age = 25;

---------Built-in JavaScript Objects

JavaScript provides many built-in objects that come with pre-defined properties and methods for performing common tasks.

Object Description
Array Creates and manipulates lists of values.
Boolean Represents logical values true/false.
Date Works with dates and times.
Error Handles run-time error information.
Function Creates new function objects dynamically.
Math Provides mathematical constants and methods.
Number Represents and manipulates numeric values.
String Represents and manipulates text strings.
Examples of Built-in Objects

// Array Object
let fruits = ["Apple", "Banana", "Mango"];
console.log(fruits.length); // Output: 3

// Date Object
let today = new Date();
console.log(today.toDateString()); // Output: e.g., "Wed Aug 13 2025"

// Math Object
console.log(Math.sqrt(16)); // Output: 4

// String Object
let text = "JavaScript";
console.log(text.toUpperCase()); // Output: JAVASCRIPT

// Boolean Object
let isValid = new Boolean(true);
console.log(isValid.valueOf()); // Output: true

// Error Object
The Error object provides information about runtime errors.
try {
throw new Error("Something went wrong!");
} catch (err) {
console.log(err.name); // Output: Error
console.log(err.message); // Output: Something went wrong!
}

// Function Object
In JavaScript, functions are also objects. You can create them using the Function constructor.
let add = new Function("a", "b", "return a + b;");
console.log(add(5, 3)); // Output: 8

// Number Object
The Number object contains methods and properties for numeric values.
let num = new Number(123.456);
console.log(num.toFixed(2)); // Output: 123.46
console.log(Number.MAX_VALUE); // Largest possible number in JS

Advantages of Using Objects in JavaScript
Reusability – Methods and properties can be reused in multiple parts of the program.
Organization – Groups related data and methods in one structure.
Modularity – Helps in writing modular and maintainable code.
Flexibility – Can hold various data types, including other objects.
