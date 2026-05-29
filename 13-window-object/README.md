# Window Object in JavaScript

## Objective

This project demonstrates the Window Object and some of the most commonly used browser methods and events.

After completing this project, you will understand:

- What the Window Object is
- Why it exists
- How alert() works
- How prompt() works
- How confirm() works
- What browser events are
- How events are triggered
- How addEventListener() works with Window-related interactions
- Common beginner doubts and misconceptions

---

# What is the Window Object?

The Window Object is the top-level object created automatically by the browser whenever a webpage loads.

Think of it as the "main container" of the browser.

Everything you use in browser JavaScript ultimately belongs to the Window Object.

Visual Representation:

```text
Window
│
├── document
├── localStorage
├── console
├── alert()
├── prompt()
├── confirm()
├── setTimeout()
├── setInterval()
└── many more...
```

---

# Why Was the Window Object Created?

JavaScript needs a way to interact with the browser.

The Window Object acts as the bridge between:

```text
JavaScript
        ↕
Browser
```

Without the Window Object:

- No popups
- No document access
- No local storage
- No timers
- No browser interaction

---

# Understanding the Window Object

Most beginners write:

```javascript
alert("Hello");
```

But internally JavaScript treats it as:

```javascript
window.alert("Hello");
```

Similarly:

```javascript
document.getElementById("box");
```

is actually:

```javascript
window.document.getElementById("box");
```

And:

```javascript
localStorage.setItem("name","Sambhav");
```

is actually:

```javascript
window.localStorage.setItem("name","Sambhav");
```

The browser automatically adds `window.` for you.

---

# alert()

## Purpose

Displays a popup message to the user.

## Syntax

```javascript
alert("Hello");
```

## Example

```javascript
alert("Welcome!");
```

Output:

```text
+----------------+
| Welcome!       |
|                |
|      OK        |
+----------------+
```

---

## How alert() Works

Flow:

```text
JavaScript Executes
        ↓
Popup Appears
        ↓
Execution Pauses
        ↓
User Clicks OK
        ↓
Execution Continues
```

---

## Beginner Doubt

### "Why does my code stop after alert()?"

Because alert() blocks execution.

Example:

```javascript
console.log("Before");

alert("Hello");

console.log("After");
```

Output:

```text
Before
[Popup Appears]
After
```

The second log waits until the popup closes.

---

# prompt()

## Purpose

Collects input from the user.

## Syntax

```javascript
prompt("Enter Name");
```

---

## Example

```javascript
let name =
prompt("Enter Your Name");
```

User enters:

```text
Sambhav
```

Result:

```javascript
name = "Sambhav";
```

---

## What Does prompt() Return?

If user clicks OK:

```javascript
"Sambhav"
```

String

If user clicks Cancel:

```javascript
null
```

---

## Beginner Doubt

### "Why is prompt returning null?"

Because the user clicked Cancel.

Example:

```javascript
let name =
prompt("Enter Name");

console.log(name);
```

Output:

```text
null
```

when Cancel is pressed.

---

## Beginner Doubt

### "Why is prompt not opening?"

Possible reasons:

- Browser blocks popups
- Running inside a restricted environment
- JavaScript error before prompt()
- Event listener not attached correctly

Always check:

```javascript
console.log("Button Clicked");
```

before prompt().

---

# confirm()

## Purpose

Asks the user for confirmation.

## Syntax

```javascript
confirm("Are you sure?");
```

---

## Example

```javascript
let result =
confirm("Delete File?");
```

---

## Return Values

If user clicks OK:

```javascript
true
```

If user clicks Cancel:

```javascript
false
```

---

## Example

```javascript
let result =
confirm("Delete File?");

if(result){

    console.log("Deleted");

}else{

    console.log("Cancelled");

}
```

---

## Beginner Doubt

### "Why is confirm returning true or false?"

Because confirm() is designed for decision making.

It tells JavaScript what the user selected.

---

# Browser Events

Events are actions performed by the user or browser.

Examples:

- Clicking
- Typing
- Moving Mouse
- Submitting Forms

---

# What is an Event?

Example:

```text
User Clicks Button
```

This action creates a:

```text
click event
```

JavaScript can listen for it.

---

# click Event

Triggered when an element is clicked.

Example:

```javascript
button.addEventListener(
    "click",
    function(){

        console.log("Clicked");

    }
);
```

---

## In Our Project

```javascript
document
.getElementById("alertBtn")
.addEventListener(
    "click",
    function(){

        alert("Hello");

    }
);
```

Flow:

```text
Click Button
        ↓
click Event Fires
        ↓
alert() Executes
```

---

# keydown Event

Triggered when a keyboard key is pressed.

Example:

```javascript
input.addEventListener(
    "keydown",
    function(){

        console.log("Key Pressed");

    }
);
```

---

## When Is It Used?

- Keyboard shortcuts
- Games
- Password detection
- Live typing systems

---

# input Event

Triggered whenever the value changes.

Example:

```javascript
input.addEventListener(
    "input",
    function(){

        console.log("Typing");

    }
);
```

---

## Difference Between input and keydown

keydown:

```text
Key Pressed
```

input:

```text
Actual Value Changed
```

---

# change Event

Triggered when:

1. Value changes
2. User leaves the field

Example:

```javascript
input.addEventListener(
    "change",
    function(){

        console.log("Changed");

    }
);
```

---

## Beginner Doubt

### "Why isn't change firing while I type?"

Because:

```text
change
```

waits until the input loses focus.

Example:

```text
Type Text
        ↓
Click Somewhere Else
        ↓
change Fires
```

---

# mouseover Event

Triggered when the mouse enters an element.

Example:

```javascript
element.addEventListener(
    "mouseover",
    function(){

        console.log("Mouse Entered");

    }
);
```

---

## Common Uses

- Tooltips
- Hover Effects
- Menus
- Interactive UI

---

# addEventListener()

All events in this project use:

```javascript
addEventListener()
```

Syntax:

```javascript
element.addEventListener(
    "eventName",
    callbackFunction
);
```

Example:

```javascript
button.addEventListener(
    "click",
    function(){

        alert("Hello");

    }
);
```

Meaning:

```text
Listen for click
        ↓
Run function
```

---

# Project Workflow

## Alert Button

```text
Click
 ↓
click Event
 ↓
alert()
 ↓
Popup Appears
```

---

## Prompt Button

```text
Click
 ↓
click Event
 ↓
prompt()
 ↓
User Enters Name
 ↓
Name Displayed
```

---

## Confirm Button

```text
Click
 ↓
click Event
 ↓
confirm()
 ↓
true / false
 ↓
Result Displayed
```

---

## Input Field

### keydown

```text
Press Key
 ↓
keydown Fires
```

### input

```text
Type Character
 ↓
input Fires
```

### change

```text
Change Value
 ↓
Leave Field
 ↓
change Fires
```

### mouseover

```text
Move Mouse Over Field
 ↓
mouseover Fires
```

---

# Common Beginner Questions

## Q1. Is alert() part of JavaScript?

Technically it belongs to:

```javascript
window.alert()
```

The browser provides it.

---

## Q2. Is document part of Window?

Yes.

```javascript
window.document
```

and

```javascript
document
```

are the same.

---

## Q3. Is localStorage inside Window?

Yes.

```javascript
window.localStorage
```

---

## Q4. Why don't we write window everywhere?

JavaScript automatically assumes:

```javascript
window.alert()
```

when you write:

```javascript
alert()
```

---

## Q5. Can I create my own Window Object?

No.

The browser creates it automatically.

---

## Q6. What is the difference between alert(), prompt(), and confirm()?

| Method | Purpose | Return Value |
|----------|----------|----------|
| alert() | Show message | Nothing |
| prompt() | Get input | String / null |
| confirm() | Get confirmation | true / false |

---

# Summary

| Concept | Purpose |
|----------|----------|
| Window Object | Top-level browser object |
| alert() | Display message |
| prompt() | Get user input |
| confirm() | Get confirmation |
| click | Detect clicks |
| keydown | Detect key presses |
| input | Detect typing |
| change | Detect value changes |
| mouseover | Detect mouse entering |

---

# Learning Outcome

After completing this project, you will understand:

- What the Window Object is
- Why the browser creates it
- How alert(), prompt(), and confirm() work
- What events are
- How event listeners work
- How browser APIs are connected to the Window Object
- Common beginner mistakes and doubts
- The relationship between Window, Document, Local Storage, Events, and Browser Interaction

The most important thing to remember is:

**The Window Object is the root object of browser JavaScript. Most browser features you use directly or indirectly come from the Window Object.**