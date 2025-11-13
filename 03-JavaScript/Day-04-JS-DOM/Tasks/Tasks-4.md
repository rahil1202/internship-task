
# ✅ ** TASK 1 — Change Text on Button Click**

### ✔ Description

Clicking the button should change the text of a paragraph.

### ✔ Output behavior

Before: “Old Text”
After: “New Text Updated!”

### ✔ Code

```html
<!DOCTYPE html>
<html>
<head>
<style>
button {
  padding: 10px 20px;
  background: #3498db;
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}
p {
  font-size: 20px;
}
</style>
</head>

<body>

<p id="text">Old Text</p>
<button id="btn">Change Text</button>

<script>
document.getElementById("btn").addEventListener("click", () => {
  document.getElementById("text").textContent = "New Text Updated!";
});
</script>

</body>
</html>
```

---

# ✅ ** TASK 2 — Change Background Color on Click**

### ✔ Description

Clicking the box changes its background color.

### ✔ Output behavior

Before: gray
After: green

### ✔ Code

```html
<!DOCTYPE html>
<html>
<head>
<style>
#box {
  width: 200px;
  height: 100px;
  background: lightgray;
  border-radius: 8px;
  cursor: pointer;
}
</style>
</head>

<body>

<div id="box"></div>

<script>
document.getElementById("box").addEventListener("click", () => {
  box.style.background = "green";
});
</script>

</body>
</html>
```

---

# ✅ ** TASK 3 — Hover to Enlarge Image**

### ✔ Description

Hover over image → it grows in size.

### ✔ Code

```html
<!DOCTYPE html>
<html>
<head>
<style>
img {
  width: 150px;
  transition: 0.3s;
  border-radius: 8px;
}
img:hover {
  width: 200px;
}
</style>
</head>

<body>

<img src="https://via.placeholder.com/150" alt="img">

</body>
</html>
```

---

# ✅ ** TASK 4 — Show Input Text Live (Live Preview)**

### ✔ Description

Whatever user types → display below instantly.

### ✔ Code

```html
<!DOCTYPE html>
<html>
<head>
<style>
input {
  padding: 8px;
  width: 200px;
}
#output {
  margin-top: 10px;
  font-size: 20px;
}
</style>
</head>

<body>

<input id="inp" placeholder="Type something..." />
<p id="output"></p>

<script>
inp.addEventListener("input", () => {
  output.textContent = inp.value;
});
</script>

</body>
</html>
```

---

# ✅ ** TASK 5 — Add List Item on Button Click**

### ✔ Description

Click -> adds a new item to list.

### ✔ Code

```html
<!DOCTYPE html>
<html>
<head>
<style>
li {
  margin: 5px 0;
}
button {
  padding: 8px 15px;
  background: green;
  color: white;
  border: none;
}
</style>
</head>

<body>

<ul id="list">
  <li>Item 1</li>
</ul>

<button id="add">Add Item</button>

<script>
let count = 2;

document.getElementById("add").addEventListener("click", () => {
  let li = document.createElement("li");
  li.textContent = "Item " + count++;
  list.appendChild(li);
});
</script>

</body>
</html>
```

---

# 🔥 ** TASK 6 — Dark Mode Toggle**

### ✔ Description

Clicking the button toggles between light/dark themes.

### ✔ Code

```html
<!DOCTYPE html>
<html>
<head>
<style>
body {
  transition: 0.4s;
  padding: 20px;
  font-family: sans-serif;
}
.dark {
  background: #111;
  color: white;
}
button {
  padding: 10px 20px;
  background: black;
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}
</style>
</head>

<body>

<button id="toggle">Toggle Dark Mode</button>

<script>
document.getElementById("toggle").addEventListener("click", () => {
  document.body.classList.toggle("dark");
});
</script>

</body>
</html>
```

---

# 🔥 ** TASK 7 — Simple Counter App (Increment & Decrement)**

### ✔ Output

* increases number
  – decreases number
  Reset = back to 0

### ✔ Code

```html
<!DOCTYPE html>
<html>
<head>
<style>
button {
  padding: 10px 15px;
  margin: 5px;
  background: #2980b9;
  color: white;
  border: none;
  border-radius: 5px;
}
#count {
  font-size: 30px;
  margin: 15px 0;
}
</style>
</head>

<body>

<h1 id="count">0</h1>
<button id="plus">+</button>
<button id="minus">-</button>
<button id="reset">Reset</button>

<script>
let count = 0;

plus.addEventListener("click", () => {
  count++;
  document.getElementById("count").textContent = count;
});

minus.addEventListener("click", () => {
  count--;
  document.getElementById("count").textContent = count;
});

reset.addEventListener("click", () => {
  count = 0;
  document.getElementById("count").textContent = count;
});
</script>

</body>
</html>
```

---

# 🔥 ** TASK 8 — Simple To-Do App (DOM Create & Delete)**

### ✔ Description

User adds tasks → tasks appear with a delete button.

### ✔ Code

```html
<!DOCTYPE html>
<html>
<head>
<style>
#todo-list li {
  margin: 5px 0;
  display: flex;
  justify-content: space-between;
}
button {
  background: red;
  color: white;
  border: none;
  padding: 3px 8px;
}
</style>
</head>

<body>

<input id="task" placeholder="Enter task..." />
<button id="add">Add</button>

<ul id="todo-list"></ul>

<script>
document.getElementById("add").addEventListener("click", () => {
  let taskText = task.value;

  if (taskText.trim() === "") return;

  let li = document.createElement("li");
  li.textContent = taskText;

  let del = document.createElement("button");
  del.textContent = "X";

  del.addEventListener("click", () => {
    li.remove();
  });

  li.appendChild(del);
  document.getElementById("todo-list").appendChild(li);

  task.value = "";
});
</script>

</body>
</html>
```

---

# 🔥 ** TASK 9 — Live Character Counter (Input Event)**

### ✔ Description

Shows user how many characters typed.
Turns red when limit is reached.

### ✔ Code

```html
<!DOCTYPE html>
<html>
<head>
<style>
#count {
  font-size: 18px;
}
.red {
  color: red;
}
</style>
</head>

<body>

<textarea id="msg" rows="4" cols="30"></textarea>
<p id="count">0 / 50</p>

<script>
msg.addEventListener("input", () => {
  let len = msg.value.length;
  count.textContent = `${len} / 50`;

  if (len >= 50) {
    count.classList.add("red");
  } else {
    count.classList.remove("red");
  }
});
</script>

</body>
</html>
```

---

# 🔥 **/ TASK 10 — Build a Mini Product Card with Add to Cart**

### ✔ Description

Button click updates cart count.
You simulate an ecommerce interaction.

### ✔ Code

```html
<!DOCTYPE html>
<html>
<head>
<style>
.card {
  width: 200px;
  padding: 15px;
  border: 1px solid #ddd;
  border-radius: 8px;
  font-family: sans-serif;
}
button {
  padding: 8px 15px;
  background: #2ecc71;
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}
#cart {
  margin-top: 20px;
  font-size: 22px;
}
</style>
</head>

<body>

<div class="card">
  <h3>Wireless Mouse</h3>
  <p>₹499</p>
  <button id="addCart">Add to Cart</button>
</div>

<h2 id="cart">Cart: 0 items</h2>

<script>
let count = 0;

document.getElementById("addCart").addEventListener("click", () => {
  count++;
  document.getElementById("cart").textContent = "Cart: " + count + " items";
});
</script>

</body>
</html>
```

---
