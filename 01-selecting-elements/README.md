# DOM Playground 🚀

>  learning **DOM Element Selection** using JavaScript.

JavaScript becomes truly powerful when it starts talking to the webpage 🧠⚡  
This folder focuses on learning how to **select HTML elements** from the DOM before manipulating them.

---

# 📚 Topics Covered

| Topic | Purpose |
|---|---|
| `getElementById()` | Select element using id |
| `querySelector()` | Select first matching element |
| `querySelectorAll()` | Select all matching elements |
| `getElementsByClassName()` | Select elements using class |
| `getElementsByTagName()` | Select elements using tag |

---

# 🧩 DOM Selection Methods

---

## 1️⃣ getElementById()

Selects an element using its **unique id**.

### 🛠 Syntax
```javascript
document.getElementById("idName")
```

### ✅ Example
```javascript
let title = document.getElementById("title");
```

### 🎯 Mostly Used For
- headings
- buttons
- unique sections
- forms

---

## 2️⃣ querySelector()

Selects the **FIRST matching element**.

### 🛠 Syntax
```javascript
document.querySelector("selector")
```

### ✅ Example
```javascript
document.querySelector(".box")
document.querySelector("#title")
document.querySelector("p")
```

### 🎯 Mostly Used For
- classes
- ids
- tags
- modern JavaScript projects

### 🌟 Special Feature
Works with CSS selectors.

---

## 3️⃣ querySelectorAll()

Selects **ALL matching elements**.

### 🛠 Syntax
```javascript
document.querySelectorAll("selector")
```

### ✅ Example
```javascript
let boxes = document.querySelectorAll(".box1");
```

### 🎯 Mostly Used For
- multiple cards
- buttons
- lists
- loops

### 📦 Returns
A `NodeList`

Example:
```javascript
[box1, box2, box3]
```

---

## 4️⃣ getElementsByClassName()

Selects elements using **class name**.

### 🛠 Syntax
```javascript
document.getElementsByClassName("className")
```

### ✅ Example
```javascript
document.getElementsByClassName("sub")
```

### 🎯 Mostly Used For
- grouped elements
- same styled elements
- repeated sections

---

## 5️⃣ getElementsByTagName()

Selects elements using **HTML tag name**.

### 🛠 Syntax
```javascript
document.getElementsByTagName("tagName")
```

### ✅ Example
```javascript
document.getElementsByTagName("button")
document.getElementsByTagName("div")
```

### 🎯 Mostly Used For
- loops
- selecting same tags
- bulk operations

---

# ⚡ Additional Concepts Used

These concepts are also used in this project for small manipulations and visualization.

They will be explained in detail in upcoming folders.

| Concept | Purpose |
|---|---|
| `innerHTML` | Change HTML content |
| `style` | Change CSS using JS |
| `for loop` | Repeat tasks on multiple elements |

---

# 🧠 Beginner Flow of DOM Selection

```text
Select Element
      ↓
Store in Variable
      ↓
Change Content / Style
      ↓
Update Webpage
```

### Example
```javascript
let title = document.getElementById("title");

title.innerHTML = "Updated Title";
```

---

# 🎨 Small Before vs After Example

| Before | After |
|---|---|
| Blue Box 🟦 | Green Box 🟩 |
| Old Title | Updated Title |
| Normal Text | Styled Text |

---

# 🎯 Learning Goal

This project helps beginners understand:

✅ how JavaScript finds HTML elements  
✅ different DOM selection techniques  
✅ how webpages become interactive  
✅ the foundation of frontend development

---

# 🌌 Final Note

Every frontend interaction starts with selecting the correct element.

DOM selection is the doorway between:
```text
Static HTML 🌑
        →
Interactive Web Apps 🚀
```