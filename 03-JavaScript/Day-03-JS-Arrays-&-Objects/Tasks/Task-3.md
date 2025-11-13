# 🌟 **DAY 3 — TASK SET (10 Tasks)**

### *(Arrays + Objects + Real-Life Scenarios)*

---

# 🟦 **Task 1 — Create & Access an Array (Easy)**

### 🎯 Description

Create an array of 5 fruits. Print the 1st and last fruit.

### 📘 Learning

Array creation, indexing.

### 💻 Code

```js
let fruits = ["apple", "banana", "kiwi", "mango", "grapes"];

console.log("First:", fruits[0]);
console.log("Last:", fruits[fruits.length - 1]);
```

---

# 🟩 **Task 2 — Add & Remove Items from an Array (Easy)**

### 🎯 Description

Create a shopping cart array.
Add 2 items using `.push()` and remove 1 item using `.pop()`.

### 📘 Learning

push(), pop()

### 💻 Code

```js
let cart = ["Shoes", "Shirt"];

cart.push("Watch");
cart.push("Bag");

cart.pop();

console.log(cart);
```

---

# 🟧 **Task 3 — Use slice and splice (Medium)**

### 🎯 Description

Given an array of numbers:

* Use `slice()` to copy indexes 1 to 3
* Use `splice()` to remove the 2nd number

### 📘 Learning

slice(), splice()

### 💻 Code

```js
let nums = [10, 20, 30, 40, 50];

let sliced = nums.slice(1, 4);
console.log("Slice:", sliced);

nums.splice(1, 1);
console.log("After Splice:", nums);
```

---

# 🟥 **Task 4 — Loop Through Array (Easy)**

### 🎯 Description

Print all names in a student list using `for…of`.

### 📘 Learning

Looping arrays.

### 💻 Code

```js
let students = ["Rahil", "Ayan", "Sana", "Mehul"];

for (let s of students) {
  console.log(s);
}
```

---

# 🟪 **Task 5 — Create & Access an Object (Easy)**

### 🎯 Description

Create a student object (name, age, city).
Print all 3 values.

### 📘 Learning

Object creation, dot notation.

### 💻 Code

```js
let student = {
  name: "Rahil",
  age: 21,
  city: "Mumbai"
};

console.log(student.name);
console.log(student.age);
console.log(student.city);
```

---

# 🟫 **Task 6 — Update & Add Object Keys (Medium)**

### 🎯 Description

Create a `product` object.

* Update price
* Add a new key `discount`
* Delete the “brand” key

### 📘 Learning

Add, update, delete properties.

### 💻 Code

```js
let product = {
  name: "Laptop",
  price: 50000,
  brand: "Dell"
};

product.price = 48000;
product.discount = 10;
delete product.brand;

console.log(product);
```

---

# 🟦 **Task 7 — Loop Through Object (Medium)**

### 🎯 Description

Loop over a user object using `for…in` and print key → value.

### 📘 Learning

Object loops.

### 💻 Code

```js
let user = {
  username: "rahil_dev",
  followers: 220,
  verified: true
};

for (let key in user) {
  console.log(key + ":", user[key]);
}
```

---

# 🟩 **Task 8 — Array of Objects (Very Important)**

### 🎯 Description

Create an array of 3 movies.
Each movie = {title, rating, year}.
Print all movie titles.

### 📘 Learning

Array of objects (API-style data)

### 💻 Code

```js
let movies = [
  { title: "Inception", rating: 8.8, year: 2010 },
  { title: "Interstellar", rating: 8.6, year: 2014 },
  { title: "Dunkirk", rating: 7.9, year: 2017 }
];

for (let m of movies) {
  console.log(m.title);
}
```

---

# 🟥 **Task 9 — Calculate Total Cart Amount (Hard)**

### 🎯 Description

You are given this cart:

```js
let cart = [
  { name: "Shoes", price: 2000, qty: 2 },
  { name: "Watch", price: 1500, qty: 1 },
  { name: "Bag", price: 1000, qty: 3 }
];
```

Calculate total bill using a loop.

### 📘 Learning

Arrays + objects + loop + arithmetic.

### 💻 Code

```js
let cart = [
  { name: "Shoes", price: 2000, qty: 2 },
  { name: "Watch", price: 1500, qty: 1 },
  { name: "Bag", price: 1000, qty: 3 }
];

let total = 0;

for (let item of cart) {
  total += item.price * item.qty;
}

console.log("Total Bill:", total);
```

---

# 🟪 **Task 10 — Search for a Product in Array of Objects (Hard)**

### 🎯 Description

Given a product list, find the price of `"Camera"`.

```js
let list = [
  { name: "Laptop", price: 60000 },
  { name: "Phone", price: 20000 },
  { name: "Camera", price: 30000 }
];
```

### 📘 Learning

Array search logic.

### 💻 Code

```js
let list = [
  { name: "Laptop", price: 60000 },
  { name: "Phone", price: 20000 },
  { name: "Camera", price: 30000 }
];

for (let item of list) {
  if (item.name === "Camera") {
    console.log("Camera Price:", item.price);
  }
}
```

---

# 🎉 **Day 3 Tasks Complete!**

You’ve practiced:
✔ Arrays
✔ Objects
✔ Array + Object combos
✔ Loops
✔ Searching
✔ Updating
✔ Real-life problems (cart, movies, orders, products)

This is the foundation of all major JS and React projects.
