# JavaScript Timing Functions

## Objective

This project demonstrates JavaScript Timing Functions.

Timing Functions allow JavaScript to execute code after a delay or repeatedly after a specified interval.

---

# What are Timing Functions?

Timing Functions are built-in JavaScript methods used to schedule code execution.

They help perform actions:

- After a delay
- Repeatedly at fixed intervals

---

# setTimeout()

## Purpose

Executes code only once after a specified delay.

## Syntax

```javascript
setTimeout(function, milliseconds);
```

## Example

```javascript
setTimeout(function(){
    alert("Hello");
},2000);
```

### Output

After 2 seconds:

```text
Hello
```

---

# How setTimeout() Works

1. JavaScript schedules the function.
2. Timer starts.
3. After the specified time, the function executes.
4. The function runs only once.

---

# clearTimeout()

## Purpose

Cancels a scheduled timeout before it executes.

## Syntax

```javascript
clearTimeout(timeoutId);
```

## Example

```javascript
let id = setTimeout(showMessage,5000);

clearTimeout(id);
```

Result:

The function never executes.

---

# setInterval()

## Purpose

Executes code repeatedly after a specified interval.

## Syntax

```javascript
setInterval(function, milliseconds);
```

## Example

```javascript
setInterval(function(){
    console.log("Running...");
},1000);
```

### Output

```text
Running...
Running...
Running...
Running...
```

The function runs every second.

---

# How setInterval() Works

1. JavaScript schedules the function.
2. Timer starts.
3. Function executes.
4. Timer resets automatically.
5. Function executes again.
6. Continues until stopped.

---

# clearInterval()

## Purpose

Stops a running interval.

## Syntax

```javascript
clearInterval(intervalId);
```

## Example

```javascript
let id = setInterval(showMessage,1000);

clearInterval(id);
```

Result:

The interval stops executing.

---

# Variations Demonstrated

## setTimeout with Anonymous Function

```javascript
setTimeout(function(){
    console.log("Executed");
},3000);
```

---

## setTimeout with Named Function

```javascript
function showMessage(){
    console.log("Executed");
}

setTimeout(showMessage,3000);
```

---

## setTimeout with Arrow Function

```javascript
setTimeout(()=>{
    console.log("Executed");
},3000);
```

---

## setInterval with Anonymous Function

```javascript
setInterval(function(){
    console.log("Running");
},1000);
```

---

## setInterval with Arrow Function

```javascript
setInterval(()=>{
    console.log("Running");
},1000);
```

---

# Common Uses

- Digital Clocks
- Countdowns
- Games
- Animations
- Notifications
- Auto Save Features
- Data Refreshing
- Live Dashboards

---

# Difference Between setTimeout() and setInterval()

| Method | Purpose |
|----------|----------|
| setTimeout() | Runs once after a delay |
| setInterval() | Runs repeatedly after every interval |

---

# Learning Outcome

After completing this project, you will understand:

- What Timing Functions are
- How setTimeout() works
- How setInterval() works
- How clearTimeout() works
- How clearInterval() works
- Different ways to use Timing Functions
- Real-world applications of Timing Functions