
# ✅ **TASK 1 — Double the Numbers (map)**

### Description

Given an array of numbers, create a new array with each number doubled.

### Code

```js
let nums = [2, 4, 6, 8];

let doubled = nums.map(n => n * 2);

console.log(doubled);  // [4, 8, 12, 16]
```

---

# ✅ **TASK 2 — Convert Names to Uppercase (map)**

### Description

Convert each name in an array to uppercase.

### Code

```js
let names = ["rahil", "ayan", "sana"];

let upper = names.map(n => n.toUpperCase());

console.log(upper);
```

---

# ✅ **TASK 3 — Filter Even Numbers (filter)**

### Description

Return only even numbers from the array.

### Code

```js
let arr = [1, 2, 3, 4, 5, 6];

let even = arr.filter(n => n % 2 === 0);

console.log(even); // [2,4,6]
```

---

# ✅ **TASK 4 — Find a Student Older Than 20 (find)**

### Description

Find first student whose age is more than 20.

### Code

```js
let students = [
  { name: "Rahil", age: 21 },
  { name: "Ayan", age: 19 },
  { name: "Sana", age: 22 }
];

let result = students.find(s => s.age > 20);

console.log(result);
```

---

# ✅ **TASK 5 — Find Last Item Using at()**

### Description

Get the last element using `.at(-1)`.

### Code

```js
let items = ["pen", "book", "tablet"];

console.log(items.at(-1)); // tablet
```

---

# 🌟 **5 MEDIUM / HARD TASKS**

---

# 🔥 **TASK 6 — Total Bill Using reduce()**

### Description

Given a cart, calculate the total price.

### Code

```js
let cart = [
  { item: "Shoes", price: 2000, qty: 2 },
  { item: "Watch", price: 1500, qty: 1 },
  { item: "Bag", price: 1000, qty: 3 }
];

let total = cart.reduce((sum, item) => {
  return sum + item.price * item.qty;
}, 0);

console.log("Total Bill:", total);
```

---

# 🔥 **TASK 7 — Filter Expensive Products (filter)**

### Description

Return products priced above ₹20,000.

### Code

```js
let products = [
  { name: "Laptop", price: 60000 },
  { name: "Phone", price: 18000 },
  { name: "Camera", price: 30000 }
];

let expensive = products.filter(p => p.price > 20000);

console.log(expensive);
```

---

# 🔥 **TASK 8 — Sort Students by Marks (sort)**

### Description

Sort students in descending order of marks.

### Code

```js
let students = [
  { name: "Rahil", marks: 88 },
  { name: "Ayan", marks: 75 },
  { name: "Sana", marks: 92 }
];

students.sort((a, b) => b.marks - a.marks);

console.log(students);
```

---

# 🔥 **TASK 9 — Get All Usernames (map + array of objects)**

### Description

Extract all usernames from an array.

### Code

```js
let users = [
  { username: "rahil_dev", age: 21 },
  { username: "ayan_xyz", age: 20 },
  { username: "sana_k", age: 22 }
];

let usernames = users.map(u => u.username);

console.log(usernames);
```

---

# 🔥 **TASK 10 — Check If All Students Passed (every)**

### Description

Marks >= 40 = pass.
Check if **every** student passed.

### Code

```js
let marks = [45, 80, 90, 60];

let allPassed = marks.every(m => m >= 40);

console.log(allPassed); // true
```

