# 📘 README.md

# 🎨 DOM Styling Elements in JavaScript

This explains how to style HTML elements dynamically using JavaScript DOM styling methods.

Using DOM styling, we can change:

- Colors
- Borders
- Width and Height
- Spacing
- Text styles
- Layout

directly from JavaScript.

---

# 🎯 Selecting Elements for Styling

Before applying styles, we first select the element from the webpage.

---

# ✅ Selecting Element by ID

## 📌 Syntax

```js
document.getElementById("idName");
```

---

## ✅ Example

```js
let box = document.getElementById("box1");
```

---

## ✅ What Happens

- JavaScript finds the element with id `box1`
- Stores it inside the variable `box`
- Now we can apply styling to it

---

# 🎨 Applying Styles Using `.style`

After selecting the element, styles can be added using:

```js
element.style.property = "value";
```

---

# ✅ Example

```js
box.style.backgroundColor = "pink";
```

This changes the background color of the element.

---

# ⚡ Styling Syntax

```js
element.style.cssProperty = "value";
```

---

# 🎯 Common DOM Styling Properties

| Property | Purpose | Example |
|---|---|---|
| `backgroundColor` | Changes background color | `"red"` |
| `color` | Changes text color | `"white"` |
| `border` | Adds border | `"1px solid black"` |
| `width` | Changes width | `"200px"` |
| `height` | Changes height | `"100px"` |
| `margin` | Adds outer spacing | `"20px"` |
| `padding` | Adds inner spacing | `"10px"` |
| `fontSize` | Changes text size | `"30px"` |
| `borderRadius` | Makes corners rounded | `"10px"` |

---

# 🧠 Important Rule

## ✅ CSS Property

```css
background-color
```

---

## ✅ JavaScript DOM Property

```js
backgroundColor
```

JavaScript uses:

```txt
Camel Case
```

instead of hyphens (`-`).

---

# 🎨 Example of Multiple Styles

```js
let box = document.getElementById("box1");

box.style.backgroundColor = "lightgreen";
box.style.border = "2px solid black";
box.style.width = "200px";
box.style.height = "100px";
```

---

# ⚡ Border Styling Syntax

## ✅ Syntax

```js
element.style.border = "width style color";
```

---

## ✅ Example

```js
box.style.border = "1px solid black";
```

| Value | Meaning |
|---|---|
| `1px` | Border thickness |
| `solid` | Border style |
| `black` | Border color |

---

# 🎯 Margin and Padding

## ✅ Margin

Adds space outside the element.

```js
box.style.margin = "20px";
```

---

## ✅ Padding

Adds space inside the element.

```js
box.style.padding = "10px";
```

---

# 🚀 Real World Uses

| Use Case | Example |
|---|---|
| Dark Mode | Change colors dynamically |
| Interactive Buttons | Hover effects |
| Games | Move and style objects |
| Dashboards | Dynamic cards |
| Forms | Error highlighting |

---

# 🧩 Final Conclusion

DOM styling allows JavaScript to dynamically control webpage design.

Using:

```js
element.style.property = "value";
```

we can style elements directly from JavaScript and create interactive webpages ✨