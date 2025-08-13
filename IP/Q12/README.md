---

### **User Defined Exception in JavaScript**

In JavaScript, an **exception** is an unexpected error that occurs during program execution, which disrupts the normal flow of the program. While JavaScript provides several built-in exceptions (`ReferenceError`, `TypeError`, `SyntaxError`, etc.), developers can also **create their own exceptions**. These are called **user-defined exceptions**.

#### **Why Use User-Defined Exceptions?**

* To provide **custom error messages** specific to the application logic.
* To **validate user input** and stop execution when invalid data is found.
* To **handle special conditions** that are not covered by built-in errors.

---

### **Steps to Create a User-Defined Exception**

1. **Detect the error condition** in your code.
2. **Use the `throw` statement** to throw an error. The thrown value can be a string, number, Boolean, object, or an instance of the `Error` class.
3. **Handle the error** using `try...catch...finally` blocks.
4. **Optionally** use the `instanceof Error` check to verify if the caught object is an Error instance.

---

### **Example:**

```javascript
try {
  var num = prompt("Enter a number (1-2):", "1");

  // Throwing user-defined exceptions
  if (num == "1") throw "Custom String Error Message"; // string type error
  else if (num == "2") throw 404; // numeric error
  else throw new Error("Invalid input provided"); // Error object
} catch (err) {
  alert("Exception caught!");

  // Show the type and value of the error
  alert("Type: " + typeof err + "\nValue: " + err);

  // Check if it is an Error object
  if (err instanceof Error) {
    alert("Error Message: " + err.message);
  }
}
```

---

### **Explanation:**

- If **user enters `1`** → A **string error** is thrown.
- If **user enters `2`** → A **number error** is thrown.
- For **any other input** → An **Error object** is thrown with a custom message `"Invalid input provided"`.
- The `catch` block handles all these cases.
- The **`instanceof Error`** check is used to distinguish between primitive values and actual Error objects.

---

### **Key Points:**

- **`throw`** can throw any JavaScript value (primitive or object).
- **`try...catch`** ensures the program does not stop abruptly when an exception occurs.
- **User-defined exceptions** improve readability and debugging by giving meaningful error messages.
- Using the **Error object** is preferred for consistency (`err.name`, `err.message`).

---
