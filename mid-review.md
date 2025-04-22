- *window.confirm*("text message"); // it returns true or false , ok or cancel 
- *window.alert*("message"); just show a message 
- *window.prompt*("enter value","0")

### Q1. What will be the output of the following Javascript code . 
```js
<script type = "text/javascript">
<!window.alert("Welcome to \n Web Technologies \n @ GJU);>
</script>
```
```output
message : Welcome to \n Web Technologies \n @ GJU
```

### Q2. Write a Javascript code for a function that confirms the user response by pressing a button (OK, Cancel)
```js
<head>
<script type = text/javascript>
function your_confirm(){
var answer = window.confirm("Press a button");
if(answer == ture){
document.write("you pressed OK");
}else{
document.write("you pressed Cancel");
}
}
</script>
</head>

<body
>
<input type="button" onclick="your_confirm()" value="Display your confirm box"/>
</body>
```

### Q3. Write a Javascript code that allows the user to enter an integer Temperatur value between 0 -100 and validate this value . 

```js
<body>
<script>
var value = parseInt(window.prompt("enter a value between 0 -100","0"));
if (value < 0){
window.alert("value should be more than 0");
}else if(value > 100){
window.alert("value should be less than 100);
}else{
window.alert("your value is " + value);
}
</script>
</body>
```

### Q4. Write a Javascript code that prints greetings according to the following times:
| Time AM/PM   | Greetings      |
| ------------ | -------------- |
| *0-12* AM    | Good Morning   |
| *12 - 18* PM | Good afternoon |
| *18-24* PM   | Good evening   |

```js
var date = new Date();
var hour = date.getHours(); // returns hour in 24-hour format (0-23)

if (hour < 12) {
  window.alert("Good morning");
} else if (hour < 18) {
  window.alert("Good afternoon");
} else {
  window.alert("Good evening");
}
```

### Q5. What will be the output of the following program:
```js
<head>
<script type="text/javascript">
function product(a,b){return a*b;}
</script>
</head>
<body>
<script>
document.write(product(4,3));
</script>
</body>
</html>
```

