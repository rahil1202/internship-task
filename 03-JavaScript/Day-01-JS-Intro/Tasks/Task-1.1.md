
# ✅ **DAY 1 — TASK SET (10 Tasks)**

### *(Each task includes description + real-life idea + working code)*

---

# 🟦 **Task 1 — Greet the User Using `prompt()`**

### 🎯 Goal

Learn how to accept user input and display output.

### 📝 Description

Ask the user for their name and greet them with a friendly message.

### 💻 Code

```js
let name = prompt("Enter your name:");
console.log("Hello " + name + "! Nice to meet you.");
```

---

# 🟩 **Task 2 — Add Two Numbers Entered by the User**

### 🎯 Goal

Practice converting input (string) → number and performing arithmetic.

### ✨ Real-life analogy

Online billing calculators or total price calculators.

### 💻 Code

```js
let a = Number(prompt("Enter first number:"));
let b = Number(prompt("Enter second number:"));
let sum = a + b;

console.log("The sum is:", sum);
```

---

# 🟧 **Task 3 — Check if a Number Is Even or Odd**

### 🎯 Goal

Understanding conditionals + modulus operator.

### 💻 Code

```js
let num = Number(prompt("Enter a number:"));

if (num % 2 === 0) {
  console.log(num + " is Even");
} else {
  console.log(num + " is Odd");
}
```

---

# 🟪 **Task 4 — Swap Two Variables (Without Third Variable)**

### 🎯 Goal

Learn variable reassignment and arithmetic tricks.

### 💻 Code

```js
let x = 10;
let y = 20;

console.log("Before:", x, y);

// Swap logic:
x = x + y;  
y = x - y;
x = x - y;

console.log("After:", x, y);
```

---

# 🟥 **Task 5 — Create a Student Object**

### 🎯 Goal

Introduce basic object and array use.

### ✨ Real-life use

Profiles in apps like LinkedIn, student portals, dashboards.

### 💻 Code

```js
let student = {
  name: "Rahil",
  age: 20,
  subjects: ["HTML", "CSS", "JS"]
};

console.log(student);
```

---

# 🟨 **Task 6 — Simple Login Check (Boolean + if)**

### 🎯 Goal

Use boolean variables + conditional logic.

### ✨ Real-life use

Login/logout systems, access control.

### 💻 Code

```js
let isLoggedIn = false;

if (isLoggedIn) {
  console.log("Welcome back!");
} else {
  console.log("Please login to continue.");
}
```

---

# 🟫 **Task 7 — Check Eligibility to Vote**

### 🎯 Goal

Use input/output + comparison operators.

### 💻 Code

```js
let age = Number(prompt("Enter your age:"));

if (age >= 18) {
  console.log("You are eligible to vote.");
} else {
  console.log("You are not eligible to vote.");
}
```

---

# 🟦 **Task 8 — Calculate Total Bill with Discount**

### 🎯 Goal

Practice arithmetic + logic.

### ✨ Real-life use

Billing systems, carts, online shopping.

### 💻 Code

```js
let amount = Number(prompt("Enter total amount:"));
let discount = 0;

if (amount > 1000) {
  discount = amount * 0.10; // 10% discount
}

let finalPrice = amount - discount;
console.log("Final bill:", finalPrice);
```

---

# 🟫 **Task 9 — Temperature Converter (°C → °F)**

### 🎯 Goal

Practice formulas and operator usage.

### Formula

°F = (°C × 9/5) + 32

### 💻 Code

```js
let celsius = Number(prompt("Enter temperature in Celsius:"));
let fahrenheit = (celsius * 9/5) + 32;

console.log("Temperature in Fahrenheit:", fahrenheit);
```

---

# 🟣 **Task 10 — Make a "Small Product Data" Program**

### 🎯 Goal

Combine everything:

* variables
* object
* operator
* console output

### ✨ Real-life use

E-commerce product management.

### 💻 Code

```js
let product = {
  name: "Laptop",
  price: 50000,
  quantity: 2
};

let total = product.price * product.quantity;

console.log("Product:", product.name);
console.log("Quantity:", product.quantity);
console.log("Total Price:", total);
```

---

# 🌟 **Bonus Task (Optional)**

## Ask user for two numbers & show:

* sum
* subtraction
* multiplication
* division
* remainder

```js
let a = Number(prompt("Enter first number:"));
let b = Number(prompt("Enter second number:"));

console.log("Sum:", a + b);
console.log("Difference:", a - b);
console.log("Multiply:", a * b);
console.log("Divide:", a / b);
console.log("Remainder:", a % b);
```

---