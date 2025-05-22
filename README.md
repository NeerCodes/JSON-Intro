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
let jsonString = '{"name": "Alice", "age": 25}';
let jsonObject = JSON.parse(jsonString);
console.log(jsonObject.name); //Output: "Alice"
console.log(jsonObject.age); //Output: 25
```

##### To convert a JavaScript object to JSON format, use JSON.stringify().
> stringify.js
```js
let jsonData = {"name": "John", "age": 22};
let jsonStr = JSON.stringify(jsonData);
console.log(jsonStr); //Output: "{\name\":\"John",\"age\":22}"
```


### **JSON code to handle JSON data from an API**
> fetch.js
```js
async function fetchData(url) {
  try {
    const response = await fetch(url);

    if (!response.ok) {
      throw new Error(`Error fetching data: ${response.statusText}`);
    }

    const data = await response.json();
    return data; // Return the parsed data

  } catch (error) {
    console.error("Error:", error);
    return null;
  }
}
```
