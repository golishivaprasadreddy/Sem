**Unit 2**

---

## 1. JavaScript to Change HTML Style for Sample User Data

### Program
```html
<!DOCTYPE html>
<html>
<head>
  <title>Change Style Example</title>
</head>
<body>
  <h2 id="username">John Doe</h2>
  <button onclick="changeStyle()">Change Style</button>
  <script>
    function changeStyle() {
      var user = document.getElementById('username');
      user.style.color = "red";
      user.style.fontSize = "30px";
      user.style.backgroundColor = "yellow";
    }
  </script>
</body>
</html>
```

### Explanation
- An `<h2>` displays user data.  
- `changeStyle()` is called when the button is clicked.  
- The function uses JavaScript to change color, font size, and background color of the user data.

### Practical Use
- Used to highlight or customize user data dynamically, e.g., highlighting a logged-in user's name.

### Output
- Clicking the button changes **"John Doe"** to a large, red font on a yellow background.

### Real-World Use
- Used in dashboards to highlight user status or notifications (e.g., admin panel user highlights).

---

## 2. JavaScript to Change HTML Attributes for Sample User Data

### Program
```html
<!DOCTYPE html>
<html>
<head>
  <title>Change Attribute Example</title>
</head>
<body>
  <img id="userimg" src="user1.jpg" width="100" height="100" alt="User">
  <button onclick="changeAttribute()">Change Image</button>
  <script>
    function changeAttribute() {
      var img = document.getElementById('userimg');
      img.src = "user2.jpg";
      img.alt = "New User Image";
      img.width = 150;
      img.height = 150;
    }
  </script>
</body>
</html>
```

### Explanation
- Displays a user image.
- `changeAttribute()` changes the image, alt text, and dimensions.

### Practical Use
- Used for updating profile pictures after user uploads a new one.

### Output
- Image changes to another picture, gets bigger, and alt text updates.

### Real-World Use
- Social media profile editors, e-commerce product image views.

---

## 3. External JavaScript File to Read User Information and Alert

### Program

**index.html**
```html
<!DOCTYPE html>
<html>
<head>
  <title>External JS Example</title>
  <script src="user.js"></script>
</head>
<body>
  <input type="text" id="uname" placeholder="Enter your name">
  <button onclick="showAlert()">Show Alert</button>
</body>
</html>
```
**user.js**
```javascript
function showAlert() {
  var name = document.getElementById('uname').value;
  alert("Hello, " + name + "!");
}
```

### Explanation
- HTML includes an external JS file.
- User enters their name, clicks button, sees alert.

### Practical Use
- Separates HTML and JS, easier for large projects and maintenance.

### Output
- Enter "Alice", click button → Alert: **"Hello, Alice!"**

### Real-World Use
- Login forms, newsletter signups, form field validation.

---

## 4. Various Ways of Creating JavaScript Objects

### Program
```html
<!DOCTYPE html>
<html>
<head><title>JavaScript Objects</title></head>
<body>
  <script>
    // 1. Object literal
    var user1 = { name: "Alice", age: 22 };

    // 2. new Object()
    var user2 = new Object();
    user2.name = "Bob";
    user2.age = 25;

    // 3. Function constructor
    function User(name, age) {
      this.name = name;
      this.age = age;
    }
    var user3 = new User("Charlie", 30);

    // 4. Class (ES6)
    class UserClass {
      constructor(name, age) {
        this.name = name;
        this.age = age;
      }
    }
    var user4 = new UserClass("David", 28);

    document.write(user1.name + ", " + user2.name + ", " + user3.name + ", " + user4.name);
  </script>
</body>
</html>
```

### Explanation
- Shows four ways to create objects: literal, `new Object`, function, class.

### Practical Use
- Organizes user and data models in web apps.

### Output
- **Alice, Bob, Charlie, David**

### Real-World Use
- User profiles, product catalogs, and data models in applications.

---

## 5. HTML Program Using Class Concept

### Program
```html
<!DOCTYPE html>
<html>
<head>
  <title>Class Concept Example</title>
</head>
<body>
  <script>
    class Student {
      constructor(name, roll) {
        this.name = name;
        this.roll = roll;
      }
      display() {
        document.write("Name: " + this.name + "<br>Roll: " + this.roll);
      }
    }
    var s1 = new Student("Anil", 101);
    s1.display();
  </script>
</body>
</html>
```

### Explanation
- Uses ES6 class for student info with a display method.

### Practical Use
- OOP code structure for managing complex data.

### Output
- **Name: Anil**  
  **Roll: 101**

### Real-World Use
- Managing student records, employee lists, inventory.

---

## 6. What is jQuery? Set CSS Property Using jQuery

### Answer
**jQuery** is a JavaScript library that simplifies HTML document traversal, event handling, and animation.

### Program
```html
<!DOCTYPE html>
<html>
<head>
  <title>jQuery CSS Example</title>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
</head>
<body>
  <div id="user">Sample User</div>
  <button id="btn">Change CSS</button>
  <script>
    $("#btn").click(function() {
      $("#user").css({
        "color": "white",
        "background-color": "blue",
        "font-size": "25px"
      });
    });
  </script>
</body>
</html>
```

### Explanation
- jQuery changes styles with a single function call.

### Practical Use
- Easily style elements based on user actions.

### Output
- Click button, "Sample User" turns white text, blue background, large font.

### Real-World Use
- Theme switchers, notification highlights, UI customization.

---

## 7. What are jQuery Events? Use jQuery Click Event

### Answer
**jQuery events** handle user actions like clicks, focus, etc.

### Program
```html
<!DOCTYPE html>
<html>
<head>
  <title>jQuery Click Event</title>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
</head>
<body>
  <p id="demo">Click the button to change this text.</p>
  <button id="btn">Click Me</button>
  <script>
    $("#btn").click(function() {
      $("#demo").text("Text changed using jQuery click event!");
    });
  </script>
</body>
</html>
```

### Explanation
- Button click changes paragraph text using jQuery.

### Practical Use
- Respond to user interactions (e.g., form submit, menu toggle).

### Output
- Click button, paragraph text updates.

### Real-World Use
- Interactive buttons, toggles, notifications.

---

## 8. Use jQuery Focus Event

### Program
```html
<!DOCTYPE html>
<html>
<head>
  <title>jQuery Focus Event</title>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
</head>
<body>
  <input type="text" id="name" placeholder="Enter Name">
  <script>
    $("#name").focus(function() {
      $(this).css("background-color", "yellow");
    });
    $("#name").blur(function() {
      $(this).css("background-color", "white");
    });
  </script>
</body>
</html>
```

### Explanation
- When the input is focused, its background turns yellow. On blur, it returns to white.

### Practical Use
- Visual feedback for active form fields.

### Output
- Click in the input, background turns yellow; click out, it turns white.

### Real-World Use
- Highlighting active fields in forms for better UX.

---

If you want any specific question in more detail or with screenshot-like output, just let me know!
