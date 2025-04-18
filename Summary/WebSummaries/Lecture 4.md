Here’s the **summary of “CS355 Lecture 4 - HTML 2”** with **code explained line by line** in simple terms, and **pages with examples listed at the end** for your future reference.

---

### **1. Unordered vs. Ordered Lists**

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul> 
<!-- Unordered list: displays items as bullet points -->

<ol>
  <li>Item 1</li>
  <li>Item 2</li>
</ol>
<!-- Ordered list: displays items as numbers -->

```

---

### **2. Definition Lists**

```html
<dl>               <!-- Starts the definition list -->
  <dt>Term</dt>    <!-- Term being defined -->
  <dd>Definition</dd>  <!-- Description of the term -->
</dl>              <!-- Ends the definition list -->

```

---

### **3. Tables**

```html
<table>                       <!-- Start table -->
  <tr>                         <!-- Start row -->
    <td>Cell 1</td>            <!-- First cell -->
    <td>Cell 2</td>            <!-- Second cell -->
  </tr>
</table>                      <!-- End table -->

```

- No headers in this version. Can add `<th>` for headers if needed.
    

---

### **4. Images**

```html
<img src="image.png" alt="Description" />
<!-- Displays image; src = file path, alt = image description -->
```

---

### **5. Forms Overview**

```html
<form>                         <!-- Start form -->
  <!-- Input elements go here -->
</form>                        <!-- End form -->

```

- Used to gather user input that can be sent to a server.
    

---

### **6. Text Input Controls**

```html
<input type="text" />          <!-- Single-line text box -->
<input type="password" />      <!-- Password input, masks characters -->
<textarea></textarea>          <!-- Multi-line text box -->
```

---

### **7. Checkboxes & Radio Buttons**

```html
<input type="checkbox" />      <!-- Allows multiple selections -->
<input type="radio" name="group1" />  <!-- Only one option can be selected per group -->
```

---

### **8. Drop-down List**

```html
<select name="dropdown">
  <option value="1">Option 1</option>
  <option value="2">Option 2</option>
</select>
<!-- Displays a drop-down menu -->
```

---

### **9. Hidden Inputs**

```html
<input type="hidden" name="pagename" value="10" />
<!-- Stores data without showing it in the browser -->
```

---

### **10. Submit and Reset Buttons**

```html
<input type="submit" value="Submit" />
<input type="reset" value="Reset" />
<!-- Submit sends data; Reset clears form inputs -->
```

---

### **11. HTML Frames and Inline Frames**

```html
<iframe src="sample1.html" height="400" width="400" frameborder="1">
  <!-- fallback content if iframe not supported -->
</iframe>
<!-- Displays another HTML page within the current one -->
```

---

### **Pages with Examples for Reference**

- **Tables Example #1**: Pages **21–24**
    
- **Forms Example #2**: Pages **25–30**