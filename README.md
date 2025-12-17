## Q1. What is Node.js?

Node.js is an open-source, cross-platform **JavaScript runtime environment** that allows you to run JavaScript code **outside the browser**, mainly on the server side.

---

## Q2. How is Node a runtime environment? What is V8?

Node.js provides everything required to execute JavaScript on the server (JS engine, APIs, event loop).
**V8** is Google’s JavaScript engine (written in C++) that converts JavaScript into machine code for fast execution.

---

## Q3. Runtime Environment vs Framework

| Runtime Environment | Framework                |
| ------------------- | ------------------------ |
| Executes code       | Provides structure/tools |
| Example: Node.js    | Example: Express.js      |
| Low-level           | High-level               |

---

## Q4. Node.js vs Express.js

| Node.js             | Express.js                 |
| ------------------- | -------------------------- |
| Runtime environment | Web framework              |
| Low-level APIs      | Built on Node              |
| More code needed    | Simplifies server creation |

---

## Q5. Client-Side vs Server-Side

| Browser          | Node.js            |
| ---------------- | ------------------ |
| DOM access       | No DOM             |
| Runs in browser  | Runs on server     |
| User interaction | Business logic, DB |

---

## 7 Main Features of Node.js

1. Asynchronous & Non-blocking
2. Single-threaded
3. Event-driven
4. Fast (V8 engine)
5. Scalable
6. Cross-platform
7. Large NPM ecosystem

---

## Single Threaded Programming

Uses **one main thread** to handle requests.

## Multi Threaded Programming

Uses **multiple threads** to execute tasks concurrently.

---

## Synchronous Programming

Tasks execute **one after another**, blocking the next task.

## Asynchronous Programming

Tasks execute **without blocking**, using callbacks/promises.

---

## Synchronous vs Asynchronous

| Synchronous | Asynchronous |
| ----------- | ------------ |
| Blocking    | Non-blocking |
| Slower      | Faster       |
| Simple      | Efficient    |

---

## Events & Event System

* **Event**: An action (click, request)
* **Event Emitter**: Emits events
* **Event Queue**: Stores events
* **Event Loop**: Executes events
* **Event Driven**: App reacts to events

---

## Advantages of Node.js

* High performance
* Scalable
* Same language frontend/backend
* Huge ecosystem

---

## Disadvantages of Node.js

* Not good for CPU-intensive tasks
* Callback complexity
* Single-thread limitations

---

## How to Setup Node Project

```bash
npm init -y
```

Create `index.js` → run `node index.js`

---

## What is NPM?

Node Package Manager – manages dependencies.

### node_modules folder

Stores installed packages.

---

## package.json

Contains project metadata, scripts & dependencies.

---

## What are Modules in Node?

Reusable pieces of code.

### Ways to Export

1. `module.exports`
2. `exports`

### If not exported?

Cannot be accessed outside the file.

---

## Importing Modules

```js
const func = require('./file')
const { a, b } = require('./file')
```

---

## Module Wrapper Function

Each module is wrapped in a function internally:

```js
(function(exports, require, module, __filename, __dirname){})
```

---

## Types of Modules

1. Core Modules
2. Local Modules
3. Third-party Modules

---

## Top 5 Built-in Modules

1. fs
2. path
3. os
4. events
5. http

---

## fs Module

Handles file operations.
Functions: `readFile`, `writeFile`, `appendFile`, `unlink`

---

## path Module

Handles file paths.
Functions: `join`, `resolve`, `basename`, `extname`

---

## os Module

Provides OS info.
Functions: `platform`, `totalmem`, `freemem`, `hostname`

---

## events Module

Used for event handling.

```js
const EventEmitter = require('events');
```

### Event Arguments

Data passed while emitting events.

---

## Function vs Event

| Function        | Event          |
| --------------- | -------------- |
| Called directly | Triggered      |
| One-time        | Listener-based |

---

## http Module

Creates web servers and handles requests/responses.

### createServer()

Creates an HTTP server.

```js
http.createServer((req, res) => {})
```
