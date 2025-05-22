# JSON-Intro

### **Introduction to JSON**

- **JSON (JavaScript Object Notation)** is a lightweight data interchange format used for storing and transporting data.
- It's often used when data is sent from a server to a web page.

### **JSON Sytnax**
- JSON data consists of name/value pairs, similar to JavaScrit object properties.
- A name/value pair includes a field name (in double quotes), followed by a colon and the corresponding value.
- Unlike JavaScript, JSON names **requires double quotes**.

### **JSON Objects**
- JSON objects are enclosed in curly braces {}.
- Objects can contain multiple name/value pairs.

> data.json
```js
{
  "firstName": "John",
  "lastName": "Doe"
}
```

### **JSON Arrays**
- JSON arrays are enclosed in square brackets [].
- An array can contain objects.

> employeeData.json
```js
"employess": [
 {
   "firstName": "John",
   "lastName": "Doe"
 },
 {
   "firstName": "Anna",
   "lastName": "Smith"
 },
 {
   "firstName": "Peter",
   "lastName": "Jones"
 }
]
```

### **Converting JSON to Js Objects & Js Objects to JSON**
##### To convert a JSON string to JavaScript object, use JSON.parse().
> parse.js
```js
let jsonString = '{"name": "Alice", "age": 25};
let jsonObject = <span style="color:blue">JSON.parse</span>(jsonString);
