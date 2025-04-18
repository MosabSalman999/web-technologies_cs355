Here’s the **summary of “CS355 Lecture 11 – PHP 4”** with **clear code explanations**, and **sectional grouping** to make it easier to review.

---

### **1. PHP Loops**

#### **While Loop**

```php
$number = 1;
while ($number <= 10) {
  echo "The number is: $number <br>";
  $number += 2;
}
// Outputs odd numbers 1, 3, ..., 9
```

#### **Do...While Loop**

```php
$x = 11;
do {
  echo "The number is: $x <br>";
  $x++;
} while ($x <= 10);
// Executes at least once, even though condition is false
```

#### **For Loop**

```php
for ($x = 10; $x >= 0; $x--) {
  echo "The number is: $x <br>";
}
```

#### **Foreach Loop**

```php
$languages = array("C++", "Java", "Python", "C#");
foreach ($languages as $value) {
  echo "$value <br>";
}
```

#### **Foreach with Associative Array**

```php
$grade = array("Omar" => "95", "Ahmad" => "77", "Zaid" => "83");
foreach ($grade as $key => $value) {
  echo "$key: $value <br>";
}
```

---

### **2. Break & Continue**

```php
for ($counter = 0; $counter < 10; $counter++) {
  if ($counter == 5) break;     // Stops the loop at 5
  echo "Counter: $counter<br>";
}

for ($counter = 0; $counter < 10; $counter++) {
  if ($counter == 5) continue;  // Skips 5
  echo "Counter: $counter<br>";
}
```

---

### **3. PHP Functions**

#### **Without Arguments**

```php
function welcome() {
  echo "Hello Students!";
}
welcome();
```

#### **With Arguments**

```php
function studentGPA($fname, $GPA) {
  echo "$fname. GPA: $GPA <br>";
}
studentGPA("Laith", "2.81");
```

#### **With Type Hinting and `declare(strict_types=1)`**

```php
declare(strict_types=1);
function totalGrade(int $grade, int $bonus) {
  return $grade + $bonus;
}
echo totalGrade(85, "5 points"); // Error: string is not int
```

#### **Without Strict Mode**

```php
function totalGrade(int $grade, int $bonus) {
  return $grade + $bonus;
}
echo totalGrade(85, "5 points"); // Output: 90 (auto-converts)
```

#### **Return Type Declaration**

```php
function sum(float $a, float $b) : int {
  return $a + $b;
}
echo sum(10.5, 20.2); // Output: 30 (as int)
```

#### **Pass by Reference**

```php
function add(&$value) {
  $value += 2;
}
$x = 2;
add($x);
echo $x; // Output: 4
```

---

### **4. PHP Date and Time**

```php
echo date("d/m/Y");      // 06/04/2025
echo date("l");          // Sunday
echo date("h:i:sa");     // 11:40:33am

// Custom time using mktime
$md = mktime(11, 40, 33, 04, 06, 2025);
echo date("d-m-Y h:i:sa", $md);

// String to timestamp using strtotime
$md = strtotime("next Sunday");
echo date("d-m-Y h:i:sa", $md);
```

---

### **5. File Handling in PHP**

#### **Read File Content**

```php
echo readfile("CScourses.txt");
```

#### **fopen + fread**

```php
$myfile = fopen("CScourses.txt", "r") or die("Unable to open file!");
echo fread($myfile, filesize("CScourses.txt"));
fclose($myfile);
```

#### **fgets – Read One Line**

```php
$myfile = fopen("CScourses.txt", "r") or die("Unable to open file!");
echo fgets($myfile);
fclose($myfile);
```

#### **fwrite – Write to File**

```php
$myfile = fopen("newfile.txt", "w") or die("Unable to open file!");
fwrite($myfile, "Hello Students\n");
fwrite($myfile, "Have a nice day!\n");
fclose($myfile);
```

---

### **6. File Upload in PHP**

#### **Step 1: Enable uploads in `php.ini`**

```ini
file_uploads = On
```

#### **Step 2: HTML Upload Form**

```html
<form action="upload.php" method="post" enctype="multipart/form-data">
  <input type="file" name="fileToUpload" id="fileToUpload">
  <input type="submit" value="Upload file" name="submit">
</form>
```

#### **Step 3: Server-Side Handling**

```php
$target_dir = "uploads/";
$target_file = $target_dir . basename($_FILES["fileToUpload"]["name"]);
$FileType = strtolower(pathinfo($target_file, PATHINFO_EXTENSION));
```

- `$_FILES["fileToUpload"]["name"]` = original file name
    
- `pathinfo()` gets the file extension
    
- `$uploadOk` can be used to check rules later