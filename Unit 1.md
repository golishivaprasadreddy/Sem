**Unit-1**

## 1. HTML Definition & Heading Tags

**Definition:**  
HTML (HyperText Markup Language) is the standard language used to create web pages. It structures web content through elements called tags.

**Key Tags/Properties:**  
- `<h1>`, `<h2>`, ..., `<h6>` are heading tags. `<h1>` is the highest/most important heading, and `<h6>` the least.
- Headings make content easy to read and help search engines understand the page’s structure.

**Complete Code:**
```html name=heading-tags-sample.html
<!DOCTYPE html>
<html>
<head>
    <title>Heading Tags Example</title>
</head>
<body>
    <!-- Main user name as the most important heading -->
    <h1>John Doe</h1>
    <!-- Job title as a second-level heading -->
    <h2>Software Engineer</h2>
    <!-- Email as a third-level heading -->
    <h3>Email: john@example.com</h3>
    <!-- Location as a fourth-level heading -->
    <h4>Location: New York</h4>
</body>
</html>
```

**Describe Output:**  
This code displays the user's data using various heading styles, with each line decreasing in font size.

**Real Use:**  
Heading tags are crucial for organizing content; they improve readability and SEO (search engine optimization) for real websites.

---

## 2. Anchor Tag (Hyperlink) & Image Tag

**Definition:**  
- The `<a>` tag creates hyperlinks, allowing users to navigate to other pages or websites.
- The `<img>` tag displays images on a webpage.

**Key Tags/Properties:**  
- `<a href="URL">` specifies the link’s destination.
- `<img src="image_url" alt="description">` sets the image source and alt-text for accessibility.

**Complete Code:**
```html name=anchor-image-sample.html
<!DOCTYPE html>
<html>
<head>
    <title>Anchor & Image Example</title>
</head>
<body>
    <!-- Hyperlink to another website -->
    <a href="https://www.example.com" target="_blank">Visit Example.com</a>
    <br>
    <!-- Displaying a sample image -->
    <img src="https://via.placeholder.com/150" alt="Sample Image">
</body>
</html>
```

**Describe Output:**  
A clickable hyperlink appears, and below it, an image is displayed.

**Real Use:**  
Links and images are fundamental for web navigation and presentation, making sites interactive and visually appealing.

---

## 3. HTML Table (4 Rows x 3 Columns)

**Definition:**  
The `<table>` tag creates a table to display data in rows and columns.

**Key Tags/Properties:**  
- `<table>`: Table container.
- `<tr>`: Table row.
- `<td>`: Table data/cell.
- `<th>`: Table header cell.

**Complete Code:**
```html name=table-sample.html
<!DOCTYPE html>
<html>
<head>
    <title>User Table</title>
</head>
<body>
    <!-- Table displaying user data -->
    <table border="1">
        <tr>
            <th>Name</th>
            <th>Email</th>
            <th>Location</th>
        </tr>
        <tr>
            <td>John Doe</td>
            <td>john@example.com</td>
            <td>New York</td>
        </tr>
        <tr>
            <td>Jane Smith</td>
            <td>jane@example.com</td>
            <td>London</td>
        </tr>
        <tr>
            <td>Mike Brown</td>
            <td>mike@example.com</td>
            <td>Sydney</td>
        </tr>
    </table>
</body>
</html>
```

**Describe Output:**  
A table appears with headers and sample user data in each cell.

**Real Use:**  
Tables are ideal for displaying structured data like user lists, product inventories, or schedules.

---

## 4. HTML Lists

**Definition:**  
Lists organize related items. HTML supports unordered (`<ul>`) and ordered (`<ol>`) lists.

**Key Tags/Properties:**  
- `<ul>`: Unordered (bulleted) list.
- `<ol>`: Ordered (numbered) list.
- `<li>`: List item.

**Complete Code:**
```html name=list-sample.html
<!DOCTYPE html>
<html>
<head>
    <title>User List Example</title>
</head>
<body>
    <!-- Unordered list of users -->
    <ul>
        <li>John Doe</li>
        <li>Jane Smith</li>
        <li>Mike Brown</li>
    </ul>
    <!-- Ordered list of skills -->
    <ol>
        <li>HTML</li>
        <li>CSS</li>
        <li>JavaScript</li>
    </ol>
</body>
</html>
```

**Describe Output:**  
Displays a bulleted list of names and a numbered list of skills.

**Real Use:**  
Lists are vital for presenting options, steps, or collections, such as features, instructions, or menus.

---

## 5. HTML Form for User Information

**Definition:**  
The `<form>` tag collects user input on web pages.

**Key Tags/Properties:**  
- `<form>`: Form container.
- `<input>`: User input field (text, radio, etc.).
- `<textarea>`: Multi-line text input.
- `<label>`: Describes each input field.

**Complete Code:**
```html name=form-sample.html
<!DOCTYPE html>
<html>
<head>
    <title>User Form Example</title>
</head>
<body>
    <!-- Form to accept user information -->
    <form>
        <label>Name:</label>
        <input type="text" name="name"><br><br>
        <label>Gender:</label>
        <input type="radio" name="gender" value="Male"> Male
        <input type="radio" name="gender" value="Female"> Female<br><br>
        <label>Address:</label>
        <textarea name="address"></textarea><br><br>
        <input type="submit" value="Submit">
    </form>
</body>
</html>
```

**Describe Output:**  
Displays a form with fields for name, gender (radio buttons), address, and a submit button.

**Real Use:**  
Forms are essential for user interaction, such as registrations, surveys, and contact forms.

---

## 6. External Style Sheet (`style.css`) & HTML Link

**Definition:**  
External CSS files (like `style.css`) separate design from content and are linked to HTML via the `<link>` tag.

**Key Tags/Properties:**  
- `<link rel="stylesheet" href="style.css">`: Links external CSS.
- CSS:
  - `background-color`: Sets background color.
  - `color`: Sets text color.
  - `text-decoration`: Adds underline.
  - `text-align`: Aligns text.
  - `text-indent`: Indents first line.

**Complete Code:**

```css name=style.css
body {
    background-color: aqua; /* Sets background color */
    color: navy;            /* Sets text color */
}
h1 {
    text-decoration: underline; /* Underlines heading */
    text-align: center;         /* Centers heading */
}
p {
    text-indent: 60px;          /* Indents first line */
    font-weight: normal;        /* Normal font weight */
}
```

```html name=external-css-sample.html
<!DOCTYPE html>
<html>
<head>
    <title>External CSS Example</title>
    <!-- Link to the external CSS file -->
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Sample User Data</h1>
    <p>
        John Doe is a software developer from New York, skilled in HTML, CSS, and JavaScript.
    </p>
</body>
</html>
```

**Describe Output:**  
Webpage has an aqua background, navy text, a centered/underlined heading, and an indented paragraph.

**Real Use:**  
External CSS promotes code reusability and maintainability, making it easier to apply consistent styles site-wide.

---

## 7. Inline CSS Example

**Definition:**  
Inline CSS styles are applied directly to an element using the `style` attribute.

**Key Tags/Properties:**  
- `style="property:value;"` within HTML tags sets styles directly.

**Complete Code:**
```html name=inline-css-sample.html
<!DOCTYPE html>
<html>
<head>
    <title>Inline CSS Example</title>
</head>
<body>
    <h1 style="color: green; text-align: center;">Sample User Data</h1>
    <p style="font-size: 18px; text-indent: 40px;">
        John Doe is a software developer skilled in HTML, CSS, and JavaScript.
    </p>
</body>
</html>
```

**Describe Output:**  
The heading is green and centered; the paragraph is larger and indented.

**Real Use:**  
Inline CSS allows quick, specific style adjustments but is not recommended for large projects due to maintainability.

---

## 8. Internal CSS Example

**Definition:**  
Internal CSS is written inside a `<style>` tag in the `<head>` section, affecting elements within that HTML document.

**Key Tags/Properties:**  
- `<style>`: Contains CSS rules in the HTML `<head>`.

**Complete Code:**
```html name=internal-css-sample.html
<!DOCTYPE html>
<html>
<head>
    <title>Internal CSS Example</title>
    <style>
        body {
            background-color: #f0f8ff;
            color: #333;
        }
        h1 {
            color: navy;
            text-align: center;
        }
        p {
            text-indent: 50px;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <h1>Sample User Data</h1>
    <p>
        John Doe is a passionate web developer. He enjoys coding and learning new technologies.
    </p>
</body>
</html>
```

**Describe Output:**  
Webpage has a light blue background, dark text, centered navy heading, indented paragraph.

**Real Use:**  
Internal CSS is useful for single-page sites or prototypes, allowing quick style changes without external files.

---

If you want all these answers combined in a single study file (e.g., Markdown), let me know
