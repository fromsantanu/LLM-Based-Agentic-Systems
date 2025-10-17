
# 🧩 **JavaScript for n8n – Practical Learning Path**

---

## 🧠 1. [**Core Concepts You Actually Need**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/JSForN8N/p01.md)

These are the minimum foundations to understand and write clean logic inside **Function / Code** nodes.

* What is JavaScript and how it runs in Node.js (n8n environment)
* Variables (`let`, `const`, `var`) — when to use which
* Data types — string, number, boolean, array, object
* Operators — arithmetic, comparison, logical (`&&`, `||`, `!`)
* Conditional statements — `if`, `else if`, `switch`
* Loops — `for`, `while`, `for...of`, `for...in`
* Functions — `function`, arrow functions `() => {}`
* Scope (local vs global variables)
* Template literals (backticks `` `Hello ${name}` ``)

---

## 🧱 2. [**Working with JSON (Most Important for n8n)**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/JSForN8N/p02.md)

Because **all n8n data is JSON**, this is your daily bread 🍞

* Accessing JSON properties (`item.json.name`)
* Nested objects (`item.json.user.address.city`)
* Adding / updating properties
* Deleting properties (`delete item.json.key`)
* Checking if a property exists (`if ("age" in item.json)`)
* Merging objects (`{...obj1, ...obj2}`)
* Cloning objects safely

💡 Example:

```js
const name = $json.name;
const updated = { ...$json, status: "processed" };
return [{ json: updated }];
```

---

## 🔁 3. [**Arrays and Data Transformation**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/JSForN8N/p03.md)

Most workflows process **lists of items**, so mastering arrays is essential.

* Creating and accessing arrays
* Useful array methods:

  * `map()`, `filter()`, `reduce()`, `forEach()`, `find()`, `some()`, `every()`
* Sorting (`sort()`), slicing (`slice()`), concatenating (`concat()`)
* Looping through arrays of JSON items

💡 Example:

```js
return items.filter(item => item.json.priority === "high");
```

---

## 🧰 4. [**n8n Special Variables and Helpers**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/JSForN8N/p04.md)

n8n gives you some preloaded variables inside the Function node.

* `$json` – current item data
* `$node["Node Name"].json` – get data from another node
* `$items()` – access all input items
* `$env()` – get environment variables
* `$now` – current timestamp
* `$execution` – workflow info (rarely needed)

💡 Example:

```js
const patient = $json;
const doctorNote = $node["Doctor Form"].json.note;
```

---

## 🌐 5. [**APIs and HTTP Requests (Optional but Powerful)**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/JSForN8N/p05.md)

You’ll often send or receive data from other systems.

* Basics of REST API (GET, POST, PUT, DELETE)
* Using `fetch()` inside Function nodes (if supported)
* Building headers and query parameters
* Handling JSON responses
* Error handling with `try...catch`

💡 Example:

```js
const res = await fetch("https://api.example.com/patients", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify($json)
});
return [{ json: await res.json() }];
```

---

## 🧮 6. [**Date and Time Handling**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/JSForN8N/p06.md)

Common in workflows — timestamping logs, delays, comparisons.

* Getting current time: `new Date()`
* Formatting dates
* Adding/subtracting days
* Comparing two dates

💡 Example:

```js
const now = new Date();
$json.processedAt = now.toISOString();
return [{ json: $json }];
```

---

## 🧩 7. [**Error Handling and Validation**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/JSForN8N/p07.md)

Keep your workflow safe.

* `try...catch` blocks
* Checking for missing or invalid fields
* Throwing custom errors (`throw new Error("Missing patient ID")`)
* Logging for debugging (`console.log()`)

---

## ⚙️ 8. [**Reusable Logic and Mini-Functions**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/JSForN8N/p08.md)

When your logic grows, split it nicely.

* Declaring helper functions inside Function nodes
* Keeping them clean and modular
* Returning transformed items properly

💡 Example:

```js
function addFlag(item) {
  item.json.flag = item.json.age > 60 ? "Senior" : "Adult";
  return item;
}
return items.map(addFlag);
```

---

## 🔄 9. [**Asynchronous Operations (Advanced)**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/JSForN8N/p09.md)

Useful when you need to **wait** for APIs or delays.

* Understanding `async` and `await`
* Using Promises (`.then()` and `.catch()`)
* Sleep or wait logic (`await new Promise(r => setTimeout(r, 1000))`)

---

## 🧩 10. [**Putting It All Together**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/JSForN8N/p10.md)

Mini projects for practice:

1. **Form Filter** – filter emergency cases from a doctor’s form
2. **Email Formatter** – prepare structured email message
3. **API Bridge** – send collected data to an external service
4. **Data Merger** – combine lab report data with patient form
5. **Auto-Logger** – append timestamps and logs into each record

---
