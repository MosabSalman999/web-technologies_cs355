Here’s the **summary of “CS355 Lecture 5 - CSS”** with **CSS code explained line-by-line** and **example pages listed at the end** for quick reference.

---

### **1. CSS Overview**

```css
/* CSS separates content from design (formatting, styling) */
/* Three types of CSS inclusion: */
```

- **Inline**: Style added directly in an element inside `<body>`
    
- **Internal**: Style placed inside `<style>` tag in the `<head>`
    
- **External**: Style loaded from a separate `.css` file using `<link>`
    

---

### **2. Inline CSS Example**

```css
<h1 style="color:blue;">Heading</h1>  
<!-- Styles only this single h1 element -->
```

---

### **3. Internal CSS Example**

<head>
<style>
  body { background-color: powderblue; }
  h1 { color: blue; }
  p { color: red; }
</style>
</head>
```css
<head>
<style>
  body { background-color: powderblue; }
  h1 { color: blue; }
  p { color: red; }
</style>
</head>
```

- Internal CSS affects **all matching elements** within the page.

---

### **4. External CSS**

```css
<head>
<link rel="stylesheet" href="style.css" />
</head>
```

**In `style.css`:**

```css
body { background-color: powderblue; }
h1 { color: blue; }
p { color: red; }
```

- External CSS allows you to apply the same styling across **multiple pages**.

---

### **5. CSS Syntax Recap**

```css
selector { property: value; }
```

Example:

```css
h1 { color: blue; }
```

---

### **6. CSS Text Attributes**

```css
h1 {
  color: blue;                /* Text color */
  font-family: verdana;       /* Font type */
  font-size: 300%;            /* Font size (relative) */
}
p {
  color: red;
  font-family: courier;
  font-size: 160%;
}
```

Other text properties:

- `text-align`: left, right, center, justify
    
- `text-decoration`: underline, line-through, blink
    

---

### **7. Borders, Padding, and Margins**

```css
p {
  color: red;
  font-size: 160%;
  border: 2px solid powderblue; /* Line around the element */
  padding: 30px;               /* Space inside the border */
  margin: 50px;                /* Space outside the border */
}
```

---

### **8. CSS Conflict Resolution (Cascading Rules)**

When all three styles are applied:

- **Inline > Internal > External**
    
- Browser gives **highest priority to inline**, then internal, then external.
    

---

### **Pages with Examples for Reference**

- **Inline Styles Example #1**: Pages **16–17**
    
- **Embedded Style Sheets (Internal)**: Pages **18–20**
    
- **External Style Sheet Example**: Pages **21–24**
    
