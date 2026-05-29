# DOM Traversing Methods

## Objective

This project demonstrates DOM Traversing methods in JavaScript.

DOM Traversing allows JavaScript to navigate through the relationships between HTML elements in the DOM tree.

---

# What is DOM Traversing?

DOM Traversing is the process of moving between related elements in the DOM structure.

Instead of searching the entire document repeatedly, JavaScript can directly access related elements such as:

- Parent elements
- Child elements
- First child
- Last child

---

# Why Use DOM Traversing?

DOM Traversing helps developers:

- Access related elements quickly
- Write cleaner code
- Improve readability
- Avoid unnecessary DOM searches

---

# DOM Structure Example

```html
<div id="container">
    <h1>Heading</h1>
    <p>Paragraph</p>
    <button>Click Me</button>
</div>
```

Tree Representation:

```text
div
├── h1
├── p
└── button
```

---

# parentElement

## Purpose

Returns the parent element of a selected element.

## Syntax

```javascript
element.parentElement
```

## Example

```javascript
let heading = document.querySelector("h1");

console.log(heading.parentElement);
```

## Output

```html
<div id="container">
```

---

# children

## Purpose

Returns all child elements of a parent.

## Syntax

```javascript
element.children
```

## Example

```javascript
console.log(container.children);
```

## Output

```text
[h1, p, button]
```

---

# firstElementChild

## Purpose

Returns the first child element inside a parent.

## Syntax

```javascript
element.firstElementChild
```

## Example

```javascript
console.log(container.firstElementChild);
```

## Output

```html
<h1>Heading</h1>
```

---

# lastElementChild

## Purpose

Returns the last child element inside a parent.

## Syntax

```javascript
element.lastElementChild
```

## Example

```javascript
console.log(container.lastElementChild);
```

## Output

```html
<button>Click Me</button>
```

---

# Traversing Methods Summary

| Method | Purpose |
|----------|----------|
| parentElement | Gets the parent element |
| children | Gets all child elements |
| firstElementChild | Gets the first child element |
| lastElementChild | Gets the last child element |

---

# Learning Outcome

After completing this project, you will understand:

- What DOM Traversing is
- Why DOM Traversing is used
- How to access parent elements
- How to access child elements
- How to access the first child element
- How to access the last child element
- How JavaScript navigates through the DOM tree