# Event Handling using addEventListener()

## Objective

This project demonstrates how to handle user interactions in JavaScript using the `addEventListener()` method.

Two buttons are provided:

- Button 1 changes the background color to Light Green.
- Button 2 changes the background color to Light Blue.

The color change occurs when the user clicks a button.

---

## What is Event Handling?

Event handling is the process of responding to user actions on a webpage.

Examples of events include:

- Click
- Double Click
- Key Press
- Mouse Movement
- Form Submission

JavaScript listens for these events and executes specific code when they occur.

---

## addEventListener() Method

The `addEventListener()` method is used to attach an event handler to an HTML element.

### Syntax

```javascript
element.addEventListener(event, callbackFunction);
```

### Parameters

| Parameter | Description |
|------------|-------------|
| event | The event to listen for |
| callbackFunction | The function that executes when the event occurs |

---

## Method 1: Using an Anonymous Function

```javascript
btn.addEventListener("click", function () {
    document.body.style.backgroundColor = "lightgreen";
});
```

### Explanation

- The event being listened for is `"click"`.
- An anonymous function is passed directly to `addEventListener()`.
- When the button is clicked, the function executes immediately.
- The background color changes to Light Green.

---

## Method 2: Using a Named Function

```javascript
btn1.addEventListener("click", changecolor);

function changecolor() {
    document.body.style.backgroundColor = "lightblue";
}
```

### Explanation

- The event being listened for is `"click"`.
- A named function is passed to `addEventListener()`.
- When the button is clicked, JavaScript calls the `changecolor()` function.
- The background color changes to Light Blue.

---

## Difference Between the Two Approaches

| Anonymous Function | Named Function |
|-------------------|----------------|
| Defined directly inside `addEventListener()` | Defined separately |
| Best for small tasks | Best for reusable code |
| Cannot be reused easily | Can be reused multiple times |

---

## Event Flow

1. User clicks a button.
2. The click event is detected.
3. `addEventListener()` triggers the associated function.
4. The function executes.
5. The webpage background color changes.

---

## Learning Outcome

After completing this project, you will understand:

- What event handling is.
- How the `addEventListener()` method works.
- How to respond to click events.
- The difference between anonymous and named callback functions.
- How JavaScript reacts to user interactions.