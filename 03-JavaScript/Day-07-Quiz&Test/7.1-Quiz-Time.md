
# Guess the output 

# ✅ **Example 1 — Basic setTimeout vs normal log**

```js
console.log("A");

setTimeout(() => {
  console.log("B");
}, 0);

console.log("C");
```

### **Output sequence**

```

```

### **Why?**

* JS runs sync code first → “A” → “C”
* setTimeout goes to callback queue → runs last.

---

# ✅ **Example 2 — Promise vs setTimeout**

```js
console.log("A");

setTimeout(() => console.log("B"), 0);

Promise.resolve().then(() => console.log("C"));

console.log("D");
```

### **Output**

```


```

### **Why?**

Microtask (Promise) runs before macrotask (timeout).

---

# ✅ **Example 3 — Multiple Promises**

```js
console.log("1");

Promise.resolve().then(() => console.log("2"));
Promise.resolve().then(() => console.log("3"));

console.log("4");
```

### **Output**

```

```

Promises always run **after current code**, but **in order added**.

---

# ✅ **Example 4 — Nested setTimeout**

```js
console.log("Start");

setTimeout(() => {
  console.log("Middle");
  setTimeout(() => console.log("End"), 0);
}, 0);

console.log("Finish");
```

### **Output**

```

```

---

# ✅ **Example 5 — Async/Await + setTimeout**

```js
async function run() {
  console.log("1");

  setTimeout(() => console.log("2"), 0);

  await Promise.resolve();
  console.log("3");
}

run();
console.log("4");
```

### **Output**

```

```

### Why?

* sync: 1 → 4
* await → goes to microtask → prints 3
* timeout prints last

---

# ✅ **Example 6 — Callback inside Promise**

```js
function run(cb) {
  Promise.resolve().then(() => {
    cb();
  });
}

console.log("A");

run(() => console.log("B"));

console.log("C");
```

### **Output**

```

```

---

# ✅ **Example 7 — Promise inside setTimeout**

```js
setTimeout(() => {
  console.log("Timeout 1");

  Promise.resolve().then(() => console.log("Promise inside Timeout"));

}, 0);

console.log("Sync");
```

### **Output**

```

```

### Why?

Microtask executes **inside the timeout**, not earlier.

---

# ✅ **Example 8 — Long Blocking Task**

```js
console.log("A");

setTimeout(() => console.log("B"), 0);

let start = Date.now();
while (Date.now() - start < 2000) {}

console.log("C");
```

### **Output**

```

```

### Why?

Blocking loop prevents timeout until after sync code ends.

---

# ✅ **Example 9 — Mixed async/await + multiple awaits**

```js
async function test() {
  console.log("1");

  await null;
  console.log("2");

  await null;
  console.log("3");
}

console.log("0");
test();
console.log("4");
```

### **Output**

```

```

---

# ✅ **Example 10 — Promise chain vs await**

```js
console.log("A");

Promise.resolve()
  .then(() => console.log("B"))
  .then(() => console.log("C"));

async function run() {
  console.log("D");
  await null;
  console.log("E");
}

run();

console.log("F");
```

### **Output**

```

```

### Why?

* sync → A D F
* microtasks: Promise B → async E → next Promise C

---

# ✅ **Example 11 — setInterval vs setTimeout**

```js
console.log("Start");

setInterval(() => console.log("Interval"), 0);

setTimeout(() => console.log("Timeout"), 0);

console.log("End");
```

### **Output**

```

...
```

**Note:**

* timeout runs once
* interval repeats
* interval doesn't run before timeout

---

# ✅ **Example 12 — Callback Hell vs Promise Execution Order**

```js
console.log("1");

setTimeout(() => { console.log("2"); }, 0);

Promise.resolve().then(() => {
  console.log("3");
  setTimeout(() => console.log("4"), 0);
});

console.log("5");
```

### **Output**

```

```

### Why?

1. Sync → 1, 5
2. Microtask → 3
3. Timeout from line 2 → 2
4. Timeout inside Promise → 4

---

