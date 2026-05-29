# DOM Class Methods in JavaScript 🚀

This project explains how to use `classList` methods in JavaScript DOM manipulation.

These methods help us:

- Add classes
- Remove classes
- Toggle classes
- Check classes

They are commonly used for:

- Dark mode 🌙
- Menus 📂
- Animations ✨
- Active buttons 🔘
- Completed tasks ✅

---

# What is a Class?

A class is a reusable label given to HTML elements.

Example:

```html
<h1 class="title">Hello</h1>
```

Here:

- `class` → HTML attribute
- `title` → class name

Classes are mainly used with:

- CSS for styling
- JavaScript for dynamic changes

---

# DOM Class Methods

## 1. classList.add()

Adds a class to an element.

### Syntax

```javascript
element.classList.add("className")
```

### Example

```javascript
let x = document.getElementById("sky");

x.classList.add("blue");
```

### What Happens?

The class `"blue"` gets added to the element.

---

## 2. classList.remove()

Removes a class from an element.

### Syntax

```javascript
element.classList.remove("className")
```

### Example

```javascript
let y = document.getElementById("sa");

y.classList.remove("pink");
```

### What Happens?

The `"pink"` class is removed from the element.

---

## 3. classList.toggle()

Adds or removes class automatically.

### Syntax

```javascript
element.classList.toggle("className")
```

### Example

```javascript
document.body.classList.toggle("dark");
```

### What Happens?

- If class exists → removes it
- If class does not exist → adds it

### Common Uses

- Dark mode 🌙
- Mobile menus 📱
- Active buttons 🔘

---

## 4. classList.contains()

Checks if class exists or not.

### Syntax

```javascript
element.classList.contains("className")
```

### Example

```javascript
if(document.body.classList.contains("dark")){
    console.log("Dark mode ON");
}
```

### Returns

- `true`
- `false`

---

# Example Project

## HTML

```html
<h1 id="sky">the sky is blue</h1>

<h1 id="sa" class="pink">the sky is pink</h1>

<button id="btn">Dark Mode</button>
```

---

## CSS

```css
.s{
    color:powderblue;
    background-color:blue;
}

.pink{
    color:pink;
    background-color:purple;
}

.dark{
    background:black;
    color:white;
}
```

---

## JavaScript

```javascript
// Selecting first heading
let x = document.getElementById("sky");

// Adding class
x.classList.add("s");


// Selecting second heading
let y = document.getElementById("sa");

// Removing class
y.classList.remove("pink");


// Button click event
document.getElementById("btn").onclick = function(){

    // Toggle dark mode
    document.body.classList.toggle("dark");


    // Check if dark class exists
    if(document.body.classList.contains("dark")){

        console.log("Dark mode ON");

    }

}
```

---

# Difference Between id and class

| id | class |
|---|---|
| Unique | Reusable |
| Used for one element | Used for many elements |
| Selected using `#` | Selected using `.` |

---

# Important DOM Methods Used

| Method | Purpose |
|---|---|
| `getElementById()` | Selects element by id |
| `classList.add()` | Adds class |
| `classList.remove()` | Removes class |
| `classList.toggle()` | Adds/removes class |
| `classList.contains()` | Checks class exists |

---

# Conclusion 🎯

DOM class methods are very important in modern JavaScript.

They help create:

- Interactive websites
- Dynamic UI
- Animations
- Themes
- Responsive components

Learning these methods is the foundation of frontend development 🚀