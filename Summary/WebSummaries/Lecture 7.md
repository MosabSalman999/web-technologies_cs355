Here’s the **summary of “CS355 Lecture 7 – JavaScript 2”** with **code explained line-by-line**, along with **pages that include examples** for future reference.

---

### **1. JavaScript Function to Validate User Input**

```js
function disp() {
  var name = document.student.sname.value; 
  // OR: var name = document.getElementById("stid").value;

  if (name == "" || !isNaN(name)) {
    window.alert("sname you entered is invalid");
  } else {
    document.write("The name you just entered is: " + name);
  }
}
```

- `isNaN()` checks if the value is **not a number**.
    
- Triggers an alert if the input is empty or numeric.
    

**Form Structure:**

```js
<form name="student">
  <input type="text" name="sname" id="stid" onclick="disp()" />
</form>
```

---

### **2. JavaScript Popup Dialog Boxes**

#### a. **Alert Box**

```js
window.alert("Warning message");
```

- Shows a simple message with “OK” button.
#### b. **Confirm Box**

```js
var response = window.confirm("Do you want to proceed?");
if (response) {
  document.write("Confirmed");
} else {
  document.write("Cancelled");
}
```

- Shows “OK” and “Cancel”; returns `true` or `false`.
#### c. **Prompt Box**

```js
var value = window.prompt("Enter a number:", "default");
```

- Allows user to enter a value during runtime.
    
- Returns the input or `null` if canceled.
    

---

### **3. Factorial Example Using Prompt**

```js
function factorial() {
  var value = window.prompt("Enter +ve integer:", "enter here");
  var fact = parseInt(value);
  var x = 1;
  for (let i = fact; i >= 1; i--) {
    x *= i;
  }
  window.alert("Factorial value: " + x);
}
```

---

### **4. JavaScript Loops**

#### a. **While Loop**

```js
var i = 0;
while (i < 10) {
  document.write("Step: " + i + "<br />");
  i++;
}
```

#### b. **For Loop with Break**

```js
for (var i = 1; i <= 10; i++) {
  if (i == 3) break;
  document.writeln("Step: " + i + "<br />");
}
```

#### c. **For Loop with Continue**

```js
for (var i = 1; i <= 10; i++) {
  if (i == 3) continue;
  document.writeln("Step: " + i + "<br />");
}
```

---

### **5. JavaScript Exception Handling**

```js
var value = window.prompt("Enter a value between 0 and 100", "");
try {
  if (value < 0) {
    throw "Error1";
  } else if (value > 100) {
    throw "Error2";
  }
} catch (er) {
  if (er == "Error1") window.alert("Error! Value can't be negative");
  if (er == "Error2") window.alert("Error! Value more than 100 is not allowed");
}
```

---

### **Pages with Examples for Reference**

- **Alert Box Example**: Pages **17–18**
    
- **Prompt Box Example**: Pages **19–20**
    
- **Variables & Arithmetic**: Pages **21–23**
    
- **Loop Example**: Pages **24–28**
    
- **Full HTML+CSS+JavaScript Example**: Pages **29–32**