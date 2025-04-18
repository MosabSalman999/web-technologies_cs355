Here’s the **summary of “CS355 Lecture 8 – PHP 1”** with **code explained line-by-line**, and **example pages for reference** at the end.

---

### **1. Introduction to PHP**

```php
<?php
// PHP is a server-side scripting language embedded in HTML
// It supports databases, sessions, cookies, encryption, etc.
?>
```

- PHP stands for **Hypertext Preprocessor**
    
- Code is processed on the **server**, not the client
    

---

### **2. PHP Tag Types**

```php
<?php ... ?>                  // Canonical (standard)
<? ... ?>                     // Short-open (not recommended)
<script language="php"> ... </script>  // Script tags (rare)
```

---

### **3. PHP Variables**

```php
$st_number = 18;                      // Integer
$course_name = "Web Technologies";   // String
```

- Variables **start with `$`**
    
- No need to declare type (dynamic typing)
    

---

### **4. PHP Variable Scope**

#### a. **Global Scope**

```php
$var = 10;
function Test() {
  echo $var; // Error: $var is not accessible here
}
```

#### b. **Local Scope**

```php
function Test() {
  $var = 10;
  echo $var; // OK
}
echo $var; // Error: $var not accessible here
```

#### c. **Access Global Inside Function**

```php
$x = 10; $y = 20;
function Test() {
  global $x, $y;
  $x = $x + $y;
}
```

#### d. **Static Variables**

```php
function Test() {
  static $x = 0;
  $x += 3;
  echo $x;
}
Test(); // 3
Test(); // 6
Test(); // 9
```

---

### **5. PHP Data Types**

- **Simple**: Integer, Float/Double, Boolean, String
    
- **Compound**: Array, Object
    
- **Special**: NULL, Resource
    

---

### **6. PHP Integer Formats**

```php
$var1 = 31;     // Decimal
$var2 = 0o31;   // Octal (equals 25)
$var3 = 0x31;   // Hex (equals 49)

echo "$var1\n$var2\n$var3";  // Output: 31 25 49
```

---

### **7. PHP Integer Overflow**

```php
$var = PHP_INT_MAX;
echo var_dump($var);  // int(2147483647)
$var++;
echo var_dump($var);  // float(2147483648)
```

- PHP automatically converts large integers to float
    

---

### **8. PHP Float/Double Example**

```php
$w = 3.245;
$x = 3.2e3;       // 3200 in scientific notation
$y = 3E-10;       // 0.0000000003
$z = 1264275425335735;  // Too large, becomes float

var_dump($w);
var_dump($x);
var_dump($y);
var_dump($z);
```

**Output:**

```scss
float(3.245)
float(3200)
float(3.0E-10)
float(1264275425340000)
```

---

### **Pages with Examples for Reference**

- **Variable Declaration & Scope**: Pages **6–11**
    
- **Integer & Float Handling**: Pages **13–19**