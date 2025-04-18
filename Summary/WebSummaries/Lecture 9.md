Here’s the **summary of “CS355 Lecture 9 – PHP 2”** with each code segment **explained line-by-line**, followed by the **example reference pages** at the end.

---

### **1. Float/Double Data Type**

```php
$w = 3.245;         // Standard decimal float
$x = 3.2e3;         // Scientific notation (3200)
$y = 3E-10;         // Very small number (0.0000000003)
$z = 1264275425335735; // Large number auto-converted to float

var_dump($w); var_dump($x); var_dump($y); var_dump($z);
```

---

### **2. Boolean Data Type**

```php
$x = rand(0, 1);               // Generates 0 or 1 randomly
$BL_val = $x ? True : False;   // Ternary operator: short if-else
if ($BL_val) {
  echo "Pass\n";
} else {
  echo "Fail\n";
}
```

---

### **3. String Operations**

```php
$course = "CS355";
$title = 'Web Technologies';
echo $course . $title;    // Concatenation using dot operator (.)
```

#### **Searching in Strings**

```php
echo strpos("CS355 Web Technologies", "Web"); // Outputs: 6
```

#### **Replacing in Strings**

```php
echo str_replace("Java", "Python", "Java Language"); // Outputs: Python Language
```

#### **String Length**

```php
echo strlen("Hello World!"); // Outputs: 12
```

---

### **4. Arrays in PHP**

#### **Indexed Array**

```php
$cars = array("Volvo", "BMW", "Toyota");
for ($x = 0; $x < count($cars); $x++) {
  echo $cars[$x] . "<br>";
}
```

#### **Associative Array**

```php
$num = array("Web" => "355", "Java" => "214", "C++" => "116");
echo "Java number is " . $num['Java']; // Outputs: Java number is 214
```

#### **Loop through Associative Array**

```php
$grade = array("Zaid" => "85", "Khaled" => "97", "Laith" => "73");
foreach ($grade as $name => $value) {
  echo "Key=$name, Value=$value<br>";
}
```

#### **Multidimensional Array**

```php
$cars = array(
  array("Ford", 70, 88),
  array("Toyota", 100, 95),
  array("Kia", 40, 50)
);
```

#### **Loop through Multidimensional Array**

```php
for ($row = 0; $row < 3; $row++) {
  echo "<p><b>Row $row</b></p><ul>";
  for ($col = 0; $col < 3; $col++) {
    echo "<li>" . $cars[$row][$col] . "</li>";
  }
  echo "</ul>";
}
```

---

### **5. PHP HTML Form Validation Example**

#### **Input Handling**

```php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
  if (empty($_POST["name"])) {
    $nameErr = "Name is required";
  } else {
    $name = test_input($_POST["name"]);
    if (!preg_match("/^[a-zA-Z-' ]*$/", $name)) {
      $nameErr = "Only letters and white space allowed";
    }
  }
}
```

#### **Function to Sanitize Input**

```php
function test_input($data) {
  $data = trim($data);
  $data = stripslashes($data);
  $data = htmlspecialchars($data);
  return $data;
}
```

#### **Form with Retained Input**

```php
<form method="post" action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]);?>">
  Name: <input type="text" name="name" value="<?php echo $name; ?>">
  <span class="error">* <?php echo $nameErr; ?></span>
  <!-- More fields follow same pattern -->
</form>
```

#### **Output User Input**

```php
echo "<h2>Your Input:</h2>";
echo $name; echo "<br>";
echo $email; echo "<br>";
...
```

---

### **Pages with Examples for Reference**

- **Float, Boolean, String Functions**: Pages **1–9**
    
- **Indexed/Associative/Multidimensional Arrays**: Pages **10–16**
    
- **HTML + PHP Form Validation Example**: Pages **17–24**