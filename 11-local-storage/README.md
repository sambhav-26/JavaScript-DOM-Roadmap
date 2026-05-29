# Local Storage in JavaScript

## Objective

This project demonstrates how to use Local Storage in JavaScript to save, retrieve, update, and delete data directly inside the browser.

Local Storage is one of the most commonly used browser storage mechanisms because data remains available even after refreshing the page or restarting the browser.

---

# What is Local Storage?

Local Storage is a built-in browser feature that allows websites to store data in the user's browser as key-value pairs.

Example:

```javascript
localStorage.setItem("name", "Sambhav");
```

Here:

```text
Key   = name
Value = Sambhav
```

Stored Data:

```text
name : Sambhav
```

---

# Why Do We Need Local Storage?

Normally, variables disappear when the page refreshes.

Example:

```javascript
let username = "Sambhav";
```

If the user refreshes the page:

```text
username is lost ❌
```

Local Storage solves this problem.

Example:

```javascript
localStorage.setItem("username","Sambhav");
```

Now even if:

- The page refreshes
- The tab closes
- The browser closes

The data remains stored.

---

# Where Is The Data Stored?

One of the most common interview and exam questions.

The data is stored inside the browser.

Examples:

- Chrome stores it inside Chrome's storage database
- Firefox stores it inside Firefox's storage database
- Edge stores it inside Edge's storage database

The data is NOT stored:

❌ In your JavaScript file

❌ In your HTML file

❌ On a server

It is stored locally on the user's device inside the browser.

---

# How Can I See Local Storage Data?

Open Developer Tools.

### Chrome

1. Press F12
2. Click Application
3. Click Local Storage

You will see:

```text
Local Storage

name    Sambhav
theme   dark
```

---

# Features of Local Storage

- Stores data permanently
- Survives page refresh
- Survives browser restart
- Stores key-value pairs
- Stores only strings
- Easy to use
- Available on all modern browsers

---

# Syntax Overview

## Save Data

```javascript
localStorage.setItem(key, value);
```

## Read Data

```javascript
localStorage.getItem(key);
```

## Delete One Item

```javascript
localStorage.removeItem(key);
```

## Delete Everything

```javascript
localStorage.clear();
```

## Count Items

```javascript
localStorage.length;
```

## Get Key Name

```javascript
localStorage.key(index);
```

---

# setItem()

## Purpose

Used to save data.

## Syntax

```javascript
localStorage.setItem("name","Sambhav");
```

## Example

```javascript
localStorage.setItem(
    "course",
    "B.Tech"
);
```

Stored Data:

```text
course : B.Tech
```

---

# getItem()

## Purpose

Used to retrieve stored data.

## Syntax

```javascript
localStorage.getItem("name");
```

## Example

```javascript
let name =
localStorage.getItem("name");

console.log(name);
```

Output:

```text
Sambhav
```

---

# removeItem()

## Purpose

Deletes a specific key-value pair.

## Syntax

```javascript
localStorage.removeItem("name");
```

Before:

```text
name : Sambhav
course : B.Tech
```

After:

```text
course : B.Tech
```

---

# clear()

## Purpose

Deletes all Local Storage data.

## Syntax

```javascript
localStorage.clear();
```

Before:

```text
name : Sambhav
course : B.Tech
theme : dark
```

After:

```text
(empty)
```

---

# length

## Purpose

Returns total number of stored items.

## Syntax

```javascript
localStorage.length;
```

Example:

```javascript
console.log(localStorage.length);
```

Output:

```text
3
```

---

# key()

## Purpose

Returns a key name using its index.

## Syntax

```javascript
localStorage.key(index);
```

Example:

```javascript
localStorage.key(0);
```

Output:

```text
name
```

---

# Can Local Storage Store Objects?

Directly?

❌ No

Local Storage stores strings only.

Example:

```javascript
let student = {
    name:"Sambhav",
    course:"B.Tech"
};
```

This cannot be stored directly.

---

# Storing Objects

Use JSON.stringify()

```javascript
let student = {
    name:"Sambhav",
    course:"B.Tech"
};

localStorage.setItem(
    "student",
    JSON.stringify(student)
);
```

Stored Value:

```text
{"name":"Sambhav","course":"B.Tech"}
```

---

# Reading Objects

Use JSON.parse()

```javascript
let student =
JSON.parse(
    localStorage.getItem("student")
);

console.log(student.name);
```

Output:

```text
Sambhav
```

---

# Real World Applications

Local Storage is commonly used for:

- Dark Mode Settings
- User Preferences
- Language Selection
- Shopping Cart Data
- Remember Me Features
- Game Progress
- Notes Applications
- Form Draft Saving

---

# Local Storage vs Session Storage

| Feature | Local Storage | Session Storage |
|----------|----------|----------|
| Survives Refresh | Yes | Yes |
| Survives Browser Close | Yes | No |
| Capacity | Larger | Smaller |
| Lifetime | Permanent | Current Tab Session |

---

# Frequently Asked Questions (FAQs)

## Q1. Does Local Storage data disappear after refresh?

No.

```javascript
localStorage.setItem("name","Sambhav");
```

The data remains after refreshing.

---

## Q2. Does Local Storage data disappear after closing the browser?

No.

The data remains stored until it is manually removed.

---

## Q3. Can different websites access each other's Local Storage?

No.

Example:

```text
google.com
```

cannot access

```text
amazon.com
```

Local Storage.

Each website has its own storage area.

---

## Q4. Is Local Storage secure?

No.

Users can open Developer Tools and view or modify Local Storage data.

Never store:

- Passwords
- Credit Card Information
- Secret API Keys

inside Local Storage.

---

## Q5. What data type does Local Storage store?

Only strings.

Examples:

```javascript
localStorage.setItem("age","20");
```

Stored as:

```text
"20"
```

String, not Number.

---

## Q6. How much data can Local Storage store?

Typically:

```text
5 MB to 10 MB
```

depending on the browser.

---

## Q7. How do I check if a key exists?

```javascript
if(localStorage.getItem("name")){
    console.log("Exists");
}
```

---

## Q8. What happens if I store a key that already exists?

The value is updated.

Example:

```javascript
localStorage.setItem("name","Sambhav");

localStorage.setItem("name","Rahul");
```

Result:

```text
name : Rahul
```

The old value is replaced.

---

# Local Storage Methods Summary

| Method | Purpose |
|----------|----------|
| setItem() | Save data |
| getItem() | Read data |
| removeItem() | Delete one item |
| clear() | Delete all data |
| key() | Get key name |
| length | Count stored items |

---

# Learning Outcome

After completing this project, you will understand:

- What Local Storage is
- Why Local Storage is used
- Where Local Storage data is stored
- How to save data using setItem()
- How to read data using getItem()
- How to delete data using removeItem()
- How to clear all data using clear()
- How to count stored items
- How to retrieve keys
- How to store JavaScript objects using JSON
- Important interview questions related to Local Storage
- Real-world use cases of Local Storage

Local Storage is one of the most important browser APIs because it enables websites to remember information even after the page has been refreshed or the browser has been restarted.