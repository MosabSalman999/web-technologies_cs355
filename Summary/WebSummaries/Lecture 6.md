Here’s the **summary of “CS355 Lecture 6 – JavaScript 1”** with **code and key points explained line-by-line**, followed by **pages with examples** for future reference.

---

### **1. What is JavaScript?**

```js
// JavaScript is a client-side scripting language.
// It runs inside the browser and doesn't need a compiler.
```

- It's **object-based** (not full OOP – no inheritance).
    
- Mainly used to **add interactivity**, **validate forms**, and **manipulate HTML**.
    

---

### **2. Adding JavaScript to HTML**

```js
<!-- In the <head> or <body> -->
<script language="JavaScript">
  document.write("Web Technologies");
</script>
```

- `language="JavaScript"`: defines the scripting language.
    
- `document.write()`: outputs content to the web page.
    

---

### **3. Using Type Attribute (Modern Syntax)**

```js
<script type="text/javascript">
  document.write("Hello Students!");
</script>
```

- `type="text/javascript"` is more standard and preferred over `language`.
    

---

### **4. Where Scripts Run**

```js
<head>
<script> ... </script>   <!-- Runs when called -->
</head>
<body>
<script> ... </script>   <!-- Runs as the page loads -->
</body>
```

- Multiple scripts can be used in one HTML page.
    

---

### **5. JavaScript Syntax Notes**

```js
// This is a single-line comment

/* This is a 
multi-line comment */

document.write("<h1>Title</h1>");   // Writes HTML to the page
```

- JavaScript is **case-sensitive**.
    
- Semicolons are **optional but recommended**.
    

---

### **6. External JavaScript Files**

```js
// Save this code in external.js (no <script> tags inside!)
document.write("External script line 1<br>");
document.write("External script line 2<br>");
```

**Use it like this:**

```js
<script src="external.js"></script>
```

- Helps reuse the same script across **multiple HTML files**.
    

---

### **7. Variable Declaration**

```js
var x;                 // traditional declaration
const grade1 = 50;     // constant value
let sum = grade1 + 20; // variable that can change
```

- Use `let` or `const` instead of `var` in modern code.
    

---

### **8. Declaring Functions**

```js
function sum(a, b) {
  return a + b;
}
```

- Functions are reusable blocks of code.
    

---

### **9. Calling Functions**

**a) Direct Call:**

```js
<script>
  var result = sum(10, 20);
  document.write("The sum is: " + result);
</script>
```

**b) Event Handler Call:**

```js
<input type="button" value="Click me" onclick="sum()">

<script>
  function sum() {
    let a = 10, b = 20;
    let c = a + b;
    document.write("The sum is: " + c);
  }
</script>
```

- Event handlers like `onclick` allow dynamic interaction.
    

---

### **Pages with Examples for Reference**

- **JavaScript Write Example**: Pages **13**
    
- **External Script Example**: Pages **14–16**
    
- **Function Call Examples (Direct + Event)**: Pages **21–22**
    
- **JS WriteLn Example**: Pages **23–24**