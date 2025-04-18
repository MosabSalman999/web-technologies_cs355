Here’s the **summary of “CS355 Lecture 10 – PHP 3”** with **code explained line-by-line**, plus the **important reference concepts** at the end.

---

### **1. PHP Object Data Type**

```php
class StudyPlan {
  function Course() {
    $this->level = "Third"; // $this refers to the object itself
  }
}

$web = new Course();     // Create an object
echo $web->level;        // Output: Third
```

---

### **2. PHP NULL Data Type**

```php
$var = NULL;
// OR simply declare without a value, PHP sets it to NULL automatically
```

- `isset($var)` returns `false` for null
    
- Evaluates as `false` in conditions
    

---

### **3. PHP Resource Type**

```php
$fp = fopen("index.php", 'r');  // Opens file as a resource
$conn = mysqli_connect("localhost", "root", "admin", "users"); 
// Connects to MySQL, returns a resource
```

---

### **4. PHP Constants**

```php
define("GJU", "German Jordanian University", true);
echo gju; // Output: German Jordanian University
```

- `define()` creates a constant
    
- Third parameter makes it case-insensitive
    

---

### **5. PHP Operators**

#### Arithmetic

```php
+ - * / % **   // Basic + exponentiation
```

#### Comparison

```php
== != < > <= >= === !== <=>   // <=> is "spaceship operator"
```

#### Assignment

```php
= += -= *= /= %= **=
```

#### Increment/Decrement

```php
++$x; $x++; --$x; $x--;
```

#### Logical

```php
&& || ! xor
```

#### String

```php
.      // Concatenate
.=     // Append
```

#### Array

```php
+ == != === !==
```

#### Conditional (Ternary & Null coalescing)

```php
$x = ($a == 1) ? "Yes" : "No";
$x = $a ?? "default";  // If $a is null or not set, $x = "default"
```

---

### **6. Operator Precedence (from highest to lowest)**

```text
Unary:           -- ++ !
Multiplicative:  * / %
Additive:        + -
Relational:      < <= > >=
Equality:        == !=
Logical AND:     &&
Logical OR:      ||
Conditional:     ?: ??
Assignment:      += -= *= /= %= =
```

---

### **7. Conditional Statements**

#### if…else

```php
$d = date("D");
if ($d == "Friday") {
  echo "Have a nice weekend!";
} else {
  echo "Have a nice day!";
}
```

#### switch

```php
$favcolor = "red";
switch ($favcolor) {
  case "red": echo "Your favorite color is red!"; break;
  case "blue": echo "Your favorite color is blue!"; break;
  default: echo "Your favorite color is neither red, blue, nor green!";
}
```
