# 🌱 **5 EASY TASKS**

---

# ✅ **TASK 1 — Delay Message (Callback + setTimeout)**

### Description

After 2 seconds, print "Task Completed".

### Code

```js
function wait(callback) {
  setTimeout(() => {
    callback("Task Completed");
  }, 2000);
}

wait((msg) => {
  console.log(msg);
});
```

### Output:

```
Task Completed
```

---

# ✅ **TASK 2 — Add Two Numbers Using a Callback**

### Description

Create a function that takes two numbers and a callback.
Print the sum using the callback.

### Code

```js
function add(a, b, callback) {
  callback(a + b);
}

add(5, 7, (result) => {
  console.log("Sum is:", result);
});
```

---

# ✅ **TASK 3 — Convert callback code into a Promise**

### Description

Make a Promise that resolves after 1 second.

### Code

```js
let p = new Promise((resolve) => {
  setTimeout(() => resolve("Promise Resolved"), 1000);
});

p.then(msg => console.log(msg));
```

---

# ✅ **TASK 4 — Simulate API Fetch With Promise + .then()**

### Description

After 1500ms, return user data.

### Code

```js
function getUser() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve({ name: "Rahil", age: 21 });
    }, 1500);
  });
}

getUser().then(user => console.log("User:", user));
```

---

# ✅ **TASK 5 — async/await Basic: Wait for a Promise**

### Description

Use async/await to get a message after waiting 1 second.

### Code

```js
function getMessage() {
  return new Promise(res => setTimeout(() => res("Hello Async"), 1000));
}

async function show() {
  let msg = await getMessage();
  console.log(msg);
}

show();
```

---

# 🌟 **5 MEDIUM / HARD TASKS**

---

# 🔥 **TASK 6 — Fix Callback Hell by Converting to Promises**

### Description

Given deeply nested callbacks, rewrite using Promises.

### Original Code (callback hell):

```js
function step1(cb) {
  setTimeout(() => cb("Step 1 done"), 1000);
}
function step2(cb) {
  setTimeout(() => cb("Step 2 done"), 1000);
}
function step3(cb) {
  setTimeout(() => cb("Step 3 done"), 1000);
}

step1((msg1) => {
  console.log(msg1);
  step2((msg2) => {
    console.log(msg2);
    step3((msg3) => {
      console.log(msg3);
    });
  });
});
```

### Convert to Promises:

```js
function step1() {
  return new Promise(res => setTimeout(() => res("Step 1 done"), 1000));
}
function step2() {
  return new Promise(res => setTimeout(() => res("Step 2 done"), 1000));
}
function step3() {
  return new Promise(res => setTimeout(() => res("Step 3 done"), 1000));
}

step1()
  .then(console.log)
  .then(step2)
  .then(console.log)
  .then(step3)
  .then(console.log);
```

---

# 🔥 **TASK 7 — Fetch Posts Sequentially Using async/await**

### Description

Simulate loading user → posts → comments using async/await.

### Code

```js
function getUser() {
  return new Promise(res => setTimeout(() => res({ id: 1 }), 1000));
}

function getPosts(user) {
  return new Promise(res =>
    setTimeout(() => res(["post1", "post2"]), 1000)
  );
}

function getComments(posts) {
  return new Promise(res =>
    setTimeout(() => res(["comment1", "comment2"]), 1000)
  );
}

async function loadData() {
  const user = await getUser();
  console.log("User:", user);

  const posts = await getPosts(user);
  console.log("Posts:", posts);

  const comments = await getComments(posts);
  console.log("Comments:", comments);
}

loadData();
```

---

# 🔥 **TASK 8 — Parallel Execution Using Promise.all()**

### Description

Run three tasks at the same time.

### Code

```js
function task1() {
  return new Promise(res => setTimeout(() => res("Task 1"), 1000));
}
function task2() {
  return new Promise(res => setTimeout(() => res("Task 2"), 2000));
}
function task3() {
  return new Promise(res => setTimeout(() => res("Task 3"), 1500));
}

async function runParallel() {
  let results = await Promise.all([task1(), task2(), task3()]);
  console.log(results);
}

runParallel();
```

Output:

```
["Task 1", "Task 2", "Task 3"]
```

---

# 🔥 **TASK 9 — Error Handling With async/await**

### Description

Simulate login success/failure using try/catch.

### Code

```js
function login(user, pass) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (user === "rahil" && pass === "1234") resolve("Login Success");
      else reject("Invalid Credentials");
    }, 1000);
  });
}

async function doLogin() {
  try {
    let msg = await login("rahil", "0000");
    console.log(msg);
  } catch (err) {
    console.log("Error:", err);
  }
}

doLogin();
```

---

# 🔥 **TASK 10 — Build a Mini “Product Loader” System**

### Description

Simulate:

1. Fetch product list
2. For each product, fetch its price
3. Print all final results

This includes looping + async/await.

### Code

```js
function getProducts() {
  return new Promise(res =>
    setTimeout(() => res(["Mouse", "Keyboard", "Laptop"]), 1000)
  );
}

function getPrice(product) {
  return new Promise(res =>
    setTimeout(() => res(product + " price: ₹" + Math.floor(Math.random()*5000)), 1000)
  );
}

async function loadProducts() {
  const products = await getProducts();

  for (let p of products) {
    const price = await getPrice(p);
    console.log(price);
  }
}

loadProducts();
```

Example Output:

```
Mouse price: ₹1200
Keyboard price: ₹2600
Laptop price: ₹4500
```

---

# 🎉 **DAY 6 COMPLETE!**

You have now mastered:

✔ Callbacks
✔ Callback Hell
✔ Promises
✔ .then / .catch
✔ Promise chaining
✔ async/await
✔ try/catch
✔ Parallel async tasks
✔ Real async system simulations

This knowledge is EXACTLY what real developers use.

