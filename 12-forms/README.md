# Forms and preventDefault() in JavaScript

## Objective

This project demonstrates how to handle form submissions using JavaScript and the `preventDefault()` method.

The goal is to understand:

- What happens when a form is submitted
- Why pages refresh after form submission
- What `preventDefault()` does
- What the `event` object is
- How form validation works
- Why modern websites use `preventDefault()`

---

# What is a Form?

A form is an HTML element used to collect information from users.

Examples:

- Login Forms
- Registration Forms
- Search Bars
- Contact Forms
- Feedback Forms

Example:

```html
<form>
    <input type="text">
    <button type="submit">
        Submit
    </button>
</form>
```

The purpose of a form is to collect data and submit it.

---

# What Happens When We Click Submit?

When a user clicks a submit button, the browser automatically performs a default action.

Example:

```text
User Clicks Submit
        ↓
Form Submits
        ↓
Page Refreshes
```

This automatic behavior is called the **default behavior** or **default action**.

---

# Beginner Doubt:
# "If JavaScript can already read .value, why do we need preventDefault()?"

This is one of the most common beginner questions.

Consider:

```javascript
form.addEventListener("submit", function(){

    let username =
    document.getElementById("username").value;

    console.log(username);

});
```

You might think:

> "JavaScript already got the value. Why do we need preventDefault()?"

The answer is:

JavaScript DOES get the value.

The problem is what happens immediately after.

The browser refreshes the page.

Flow:

```text
Submit
 ↓
JavaScript Reads Value
 ↓
Validation Runs
 ↓
Browser Refreshes Page
 ↓
Form Resets
```

The validation works.

The problem is that the page refreshes right after it.

---

# Why Does Data Appear To Be Lost?

Imagine you type:

```text
Username: Sambhav
```

Then click Submit.

Without preventDefault():

```text
Submit
 ↓
Validation Runs
 ↓
Page Refreshes
 ↓
Input Becomes Empty
```

The browser recreates the page from scratch.

That is why your entered data disappears.

---

# What Does preventDefault() Actually Do?

Syntax:

```javascript
event.preventDefault();
```

This tells the browser:

> "Do not perform your normal action."

For a form, the normal action is:

```text
Submit Form
 ↓
Refresh Page
```

preventDefault() stops that refresh.

---

# What Happens With preventDefault()?

Flow:

```text
Submit
 ↓
preventDefault()
 ↓
No Refresh
 ↓
Validation Runs
 ↓
Data Remains Visible
```

Now the browser does not refresh.

The user can still see:

```text
Username: Sambhav
```

inside the textbox.

---

# What is the Event Object?

Another very common beginner question.

Consider:

```javascript
form.addEventListener(
    "submit",
    function(event){

        event.preventDefault();

    }
);
```

Where did this `event` come from?

We never created it.

JavaScript creates it automatically.

---

# What is Stored Inside event?

Whenever an event occurs:

- Click
- Submit
- Key Press
- Mouse Move

JavaScript creates an Event Object.

Example:

```javascript
{
    type: "submit",
    target: form,
    timeStamp: 12345,
    ...
}
```

This object contains information about the event.

---

# Why Do We Need event?

Without the event object:

```javascript
function(){

}
```

JavaScript knows a submit happened.

But it cannot give us information about it.

With:

```javascript
function(event){

}
```

JavaScript gives us access to:

- Event type
- Target element
- Timestamp
- preventDefault()
- Many other event properties

---

# Can event Have Another Name?

Yes.

These are all valid:

```javascript
function(event){

}
```

```javascript
function(e){

}
```

```javascript
function(myEvent){

}
```

Most developers use:

```javascript
event
```

or

```javascript
e
```

---

# How preventDefault() Uses event

The preventDefault() method belongs to the event object.

Example:

```javascript
event.preventDefault();
```

Meaning:

```text
event
 ↓
contains
 ↓
preventDefault()
```

Without the event object:

```javascript
preventDefault();
```

will not work.

---

# Complete Example

```javascript
form.addEventListener(
    "submit",
    function(event){

        event.preventDefault();

        let username =
        document.getElementById("username").value;

        if(username === ""){

            alert("Username Required");

        }else{

            alert("Login Successful");

        }

    }
);
```

---

# Step-by-Step Flow of the Example

## User Action

```text
User Clicks Submit
```

---

## Submit Event Occurs

```javascript
"submit"
```

is triggered.

---

## JavaScript Creates Event Object

```javascript
event
```

is automatically passed into the function.

---

## preventDefault() Runs

```javascript
event.preventDefault();
```

The browser refresh is cancelled.

---

## Validation Runs

```javascript
if(username === "")
```

checks the input.

---

## Result Appears

```text
Username Required
```

or

```text
Login Successful
```

---

# Real World Uses

preventDefault() is commonly used in:

## Login Systems

Check username and password before submission.

---

## Registration Forms

Validate:

- Name
- Email
- Password

before sending data.

---

## Search Bars

Prevent refresh.

Perform search using JavaScript.

---

## AJAX Requests

Send data without refreshing the page.

---

## React Applications

React forms almost always use:

```javascript
event.preventDefault();
```

---

## Vue Applications

Frequently used in form handling.

---

## Angular Applications

Used during form validation.

---

# Common Interview Questions

## Q1. What does preventDefault() do?

Stops the browser's default behavior.

---

## Q2. Does preventDefault() stop JavaScript execution?

No.

It only stops the browser's default action.

JavaScript continues running normally.

---

## Q3. Why does form data disappear without preventDefault()?

Because the page refreshes after submission.

---

## Q4. Does validation happen without preventDefault()?

Yes.

Validation still runs.

But the page refreshes immediately afterward.

---

## Q5. What is event?

An object automatically created by JavaScript whenever an event occurs.

---

## Q6. Who creates the event object?

JavaScript automatically creates and passes it to the event handler function.

---

## Q7. Can I rename event?

Yes.

```javascript
function(e)
```

works exactly the same as:

```javascript
function(event)
```

---

# Summary

| Concept | Purpose |
|----------|----------|
| Form | Collect user input |
| Submit Event | Triggered when form is submitted |
| Event Object | Contains information about the event |
| preventDefault() | Stops browser default behavior |
| Validation | Checks whether user input is valid |

---

# Beginner Memory Trick

Think of form submission like a train.

Without preventDefault():

```text
Submit
 ↓
Validation
 ↓
Train Leaves (Page Refresh)
```

With preventDefault():

```text
Submit
 ↓
Stop The Train
 ↓
Validation
 ↓
Process Data
 ↓
Send Data When Ready
```

The most important thing to remember is:

**preventDefault() does not perform validation.**

It simply prevents the browser from refreshing the page so that JavaScript has complete control over what happens next.
```**