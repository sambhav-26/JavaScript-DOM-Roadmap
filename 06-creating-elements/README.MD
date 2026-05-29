# Creating Elements in JavaScript 🚀

 The methods used in the code for creating and managing elements dynamically using JavaScript.

---

# Methods Used in the Code

| Method | Purpose |
|---|---|
| `document.createElement()` | Creates a new HTML element |
| `textContent` | Adds text inside element |
| `appendChild()` | Adds element at the end |
| `innerHTML` | Adds HTML inside element |
| `prepend()` | Adds element at the beginning |
| `remove()` | Removes element |

---

# 1. document.createElement()

Used to create a new HTML element.

## Syntax

```javascript
document.createElement("tagName")
```

## Example From Code

```javascript
const newElement = document.createElement('p');
```

### What Happens?

Creates:

```html
<p></p>
```

The element is created but not shown on webpage yet.

---

# 2. textContent

Used to add plain text inside an element.

## Syntax

```javascript
element.textContent = "Text"
```

## Example From Code

```javascript
newElement.textContent =
'This is a new paragraph created using JavaScript.';
```

### Output

```html
<p>
This is a new paragraph created using JavaScript.
</p>
```

---

# 3. appendChild()

Used to add an element at the END of another element.

## Syntax

```javascript
parent.appendChild(child)
```

## Example From Code

```javascript
document.body.appendChild(newElement);
```

### What Happens?

The paragraph gets added at the bottom of body.

---

# 4. innerHTML

Used to add HTML code inside an element.

## Syntax

```javascript
element.innerHTML = "HTML CODE"
```

## Example From Code

```javascript
anotherElement.innerHTML =
'<h2>This is a heading inside a div.</h2>';
```

### Output

```html
<div>
   <h2>This is a heading inside a div.</h2>
</div>
```

---

# 5. prepend()

Used to add an element at the START of another element.

## Syntax

```javascript
parent.prepend(child)
```

## Example From Code

```javascript
document.body.prepend(anotherElement);
```

### What Happens?

The div gets added before existing content inside body.

---

# Difference Between appendChild() and prepend()

| appendChild() | prepend() |
|---|---|
| Adds at END | Adds at START |

---

# 6. remove()

Used to remove an element from webpage.

## Syntax

```javascript
element.remove()
```

## Example From Code

```javascript
newElement.remove();
```

### What Happens?

The paragraph element gets deleted from webpage.

---

# Full Code Used

```javascript
// Create a new element
const newElement = document.createElement('p');


// Set text inside paragraph
newElement.textContent =
'This is a new paragraph created using JavaScript.';


// Add paragraph at end of body
document.body.appendChild(newElement);



// Create another element
const anotherElement =
document.createElement('div');


// Add HTML inside div
anotherElement.innerHTML =
'<h2>This is a heading inside a div.</h2>';


// Add div at start of body
document.body.prepend(anotherElement);



// Remove paragraph
newElement.remove();
```

---

# Final Output Flow 🌌

## Step 1

Paragraph is created.

```html
<p>This is a new paragraph...</p>
```

---

## Step 2

Div with heading is created.

```html
<div>
   <h2>This is a heading inside a div.</h2>
</div>
```

---

## Step 3

`prepend()` adds div at top.

---

## Step 4

`remove()` deletes paragraph.

---

# Conclusion 🎯

These methods help create dynamic webpages where elements can be:

- Created
- Inserted
- Updated
- Removed

They are heavily used in:

- Todo Apps
- Chat Applications
- Notifications
- Dynamic UI
- Modern Web Apps 🚀