# DOM Attributes: getAttribute() and setAttribute()

## Objective

This project demonstrates how to work with HTML attributes using JavaScript DOM methods.

The project shows how to:

- Read an attribute value using `getAttribute()`
- Update an attribute value using `setAttribute()`

---

## What are Attributes?

Attributes provide additional information about HTML elements.

Example:

```html
<img src="photo.jpg" alt="Profile Photo" width="200">
```

In the example above:

- `src` is an attribute
- `alt` is an attribute
- `width` is an attribute

Attributes are written as:

```html
attribute="value"
```

---

## getAttribute()

### Purpose

Used to retrieve the value of an existing attribute.

### Syntax

```javascript
element.getAttribute("attributeName");
```

### Example

```javascript
image.getAttribute("src");
```

### Output

```text
https://via.placeholder.com/200
```

### When to Use

- Reading image URLs
- Checking link destinations
- Accessing custom data attributes
- Verifying element properties

---

## setAttribute()

### Purpose

Used to add a new attribute or modify an existing attribute.

### Syntax

```javascript
element.setAttribute("attributeName", "value");
```

### Example

```javascript
image.setAttribute(
    "src",
    "https://via.placeholder.com/300"
);
```

### Result

The image source changes to the new URL.

### When to Use

- Updating images dynamically
- Changing links
- Modifying classes
- Adding accessibility attributes
- Updating element properties without editing HTML

---

## Project Workflow

### Get Attribute Button

1. User clicks **"Get src Attribute"**.
2. `getAttribute("src")` is executed.
3. The current image source is displayed on the page.

### Change Image Button

1. User clicks **"Change Image"**.
2. `setAttribute("src", value)` updates the image URL.
3. `setAttribute("alt", value)` updates the alt text.
4. The image changes immediately.

---

## Difference Between getAttribute() and setAttribute()

| Method | Purpose |
|----------|----------|
| `getAttribute()` | Reads an attribute value |
| `setAttribute()` | Creates or updates an attribute value |

### Example

```javascript
image.getAttribute("src");
```

Reads the value.

```javascript
image.setAttribute("src", "new-image.jpg");
```

Updates the value.

---

## Learning Outcome

After completing this project, you will understand:

- What HTML attributes are
- How attributes store information about elements
- How to read attribute values using `getAttribute()`
- How to update attribute values using `setAttribute()`
- How JavaScript can dynamically modify webpage elements using attributes