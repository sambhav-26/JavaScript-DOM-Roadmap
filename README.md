# DOM Playground 🚀

A complete beginner-to-intermediate JavaScript DOM learning repository.
This project is designed to help students understand the Document Object Model (DOM) through hands-on examples, detailed explanations, commented code, and topic-specific README files.
Instead of only learning theory, every DOM concept is demonstrated with working examples that can be run directly in the browser.


## Before Learning DOM Methods

Many beginners jump straight into methods like `getElementById()` and `querySelector()` without understanding what they're selecting.
### What is a DOM Element?
A DOM element is simply an HTML element that exists on the page.

Example:

```html
<h1>Hello</h1>
<button>Click Me</button>
```

Both the `<h1>` and `<button>` are DOM elements that JavaScript can interact with.

### How to Inspect Elements

Before working with DOM methods, it's useful to learn how to inspect elements in your browser.

1. Open any webpage
2. Right-click an element
3. Click **Inspect**

This opens the browser DevTools and allows you to see:

- The HTML structure
- Element IDs
- Classes
- Parent and child elements

Understanding how elements appear in DevTools makes learning DOM manipulation much easier.
---

# What is DOM?

DOM stands for **Document Object Model**.

When a browser loads an HTML page, it converts the HTML into a tree-like structure called the DOM.

JavaScript uses the DOM to:

- Access elements
- Modify content
- Change styles
- Handle user interactions
- Create new elements
- Store data
- Validate forms
- Update the webpage dynamically

Visual Representation:

```text
HTML Page
     ↓
Browser
     ↓
DOM Tree
     ↓
JavaScript Manipulates Elements
```

DOM is the foundation of modern frontend development.

---

# Project Goal

The purpose of this repository is to provide a practical guide for learning JavaScript DOM manipulation.

Every topic includes:

✅ Working Example

✅ Detailed Comments

✅ Beginner-Friendly Explanation

✅ Dedicated README

✅ Real World Use Cases

✅ Common Beginner Questions

---

# Repository Structure

```text
DOM_PLAYGROUND/
│
├── 01-selecting-elements/
├── 02-changing-content/
├── 03-input-values/
├── 04-styling-elements/
├── 05-classes/
├── 06-creating-elements/
├── 07-events/
├── 08-attributes/
├── 09-dom-traversing/
├── 10-timing-functions/
├── 11-local-storage/
├── 12-forms/
├── 13-window-object/
│
├── assets/
├── .gitignore
└── README.md
```

---

# Topics Covered

## 01. Selecting Elements

Learn how to find elements inside a webpage.

Methods Covered:

- getElementById()
- querySelector()
- querySelectorAll()
- getElementsByClassName()
- getElementsByTagName()

Used For:

- Buttons
- Forms
- Headings
- Cards
- Lists

---

## 02. Changing Content

Learn how JavaScript updates webpage content.

Methods Covered:

- innerHTML
- innerText
- textContent

Used For:

- Dynamic Content
- Labels
- Task Managers
- Dashboards

---

## 03. Input Values

Learn how to read user input.

Property Covered:

- value

Used For:

- Login Forms
- Search Bars
- Registration Pages

---

## 04. Styling Elements

Learn how JavaScript changes CSS dynamically.

Property Covered:

- style

Used For:

- Dark Mode
- Animations
- Dynamic UI Updates

---

## 05. Classes

Learn how to add, remove, and toggle CSS classes.

Methods Covered:

- classList.add()
- classList.remove()
- classList.toggle()
- classList.contains()

Used For:

- Navigation Menus
- Dark Mode
- Task Completion

---

## 06. Creating Elements

Learn how webpages create content dynamically.

Methods Covered:

- createElement()
- appendChild()
- prepend()
- remove()

Used For:

- Todo Apps
- Chat Applications
- Dynamic Lists

---

## 07. Events

Learn how webpages respond to user actions.

Method Covered:

- addEventListener()

Events Covered:

- click
- keydown
- input
- change
- mouseover

Used For:

- Interactive Websites
- Forms
- Buttons
- Games

---

## 08. Attributes

Learn how to manage element attributes.

Methods Covered:

- setAttribute()
- getAttribute()

Used For:

- Images
- Links
- Accessibility
- Dynamic Updates

---

## 09. DOM Traversing

Learn how to move around the DOM tree.

Methods Covered:

- parentElement
- children
- firstElementChild
- lastElementChild

Used For:

- Component Navigation
- Dynamic Interfaces
- Complex Layouts

---

## 10. Timing Functions

Learn how JavaScript executes code after delays.

Methods Covered:

- setTimeout()
- setInterval()
- clearTimeout()
- clearInterval()

Used For:

- Timers
- Clocks
- Games
- Notifications

---

## 11. Local Storage

Learn how browsers store data permanently.

Methods Covered:

- setItem()
- getItem()
- removeItem()
- clear()
- key()
- length

Used For:

- User Preferences
- Dark Mode
- Shopping Carts
- Remember Me Features

---

## 12. Forms

Learn how forms work and why pages refresh.

Methods Covered:

- preventDefault()

Concepts Covered:

- Form Submission
- Validation
- Event Object
- Default Browser Behavior

Used For:

- Login Systems
- Registration Forms
- Search Pages

---

## 13. Window Object

Learn the root object of browser JavaScript.

Methods Covered:

- alert()
- prompt()
- confirm()

Events Covered:

- click
- keydown
- input
- change
- submit
- mouseover

Used For:

- Browser Interaction
- User Prompts
- Confirmation Dialogs

---

# The Most Important DOM Pattern

Throughout this repository, you'll repeatedly see this workflow:

```text
Select Element
        ↓
Listen To Event
        ↓
Create / Modify Element
        ↓
Update The Page
```

Example:

```javascript
let btn = document.querySelector("button");

btn.addEventListener("click", function () {

    let li = document.createElement("li");

    li.innerText = "New Task";

    document
        .querySelector("ul")
        .appendChild(li);

});
```
---

# How To Run This Project

## Clone Repository

```bash
git clone https://github.com/sambhav-26/DOM_Playgound.git
```

# Recommended Learning Order

For beginners:

```text
01-selecting-elements
        ↓
02-changing-content
        ↓
03-input-values
        ↓
04-styling-elements
        ↓
05-classes
        ↓
06-creating-elements
        ↓
07-events
        ↓
08-attributes
        ↓
09-dom-traversing
        ↓
10-timing-functions
        ↓
11-local-storage
        ↓
12-forms
        ↓
13-window-object
```

Follow this order to build concepts progressively.

---

# Who Is This For?

This repository is ideal for:

- Beginners Learning JavaScript
- College Students
- Frontend Development Beginners
- Self-Learners
- Hackathon Participants
- Anyone Preparing for JavaScript Interviews

---

# Common Beginner Questions

### Do I need React before learning DOM?

No.

Understanding DOM first makes React much easier to learn.

---

### Why is DOM important?

Because every frontend framework ultimately interacts with the DOM.

---

### Do real websites use these concepts?

Yes.

Every website uses:

- Events
- Forms
- Local Storage
- DOM Manipulation

daily.

---

### Is this enough before learning React?

Yes.

A solid understanding of these topics provides a strong foundation for:

- React
- Next.js
- Vue
- Angular

---

# Contributing

Contributions are welcome.

Possible improvements:

- New examples
- Better UI demonstrations
- Additional DOM methods
- Mini projects

---

# Contact

If you have questions, suggestions, or find an issue:

📧 **krsambhavjain@gmail.com**

---

# License

This project is intended for educational and learning purposes.

Feel free to use, modify, and learn from the examples.

---

## Final Note

The DOM is where JavaScript becomes interactive.

Once you understand how to:

- Select Elements
- Listen to Events
- Modify Content
- Create Elements
- Store Data
- Handle Forms

you have learned the core skills behind modern frontend development.

Happy Coding! 🚀
