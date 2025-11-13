
# 🧠 **DAY 2 — TASK SET (10 TASKS)**

**Covers: Control Flow + Functions + Scope + Recursion**

---

# 🟦 **Task 1 — Age Eligibility Checker (if/else)**

### 🎯 Description

Ask the user for their age and check:

* If age ≥ 18 → Adult
* Else → Minor

### 📘 Concepts

`if`, comparison, input/output.

### 💻 Code

```js
let age = Number(prompt("Enter your age:"));

if (age >= 18) {
  console.log("You are an Adult.");
} else {
  console.log("You are a Minor.");
}
```

---

# 🟩 **Task 2 — Grading System (else if)**

### 🎯 Description

Input marks, output grade:

* ≥90 → A
* ≥75 → B
* ≥50 → C
* else → Fail

### 📘 Concepts

Chained conditions.

### 💻 Code

```js
let marks = Number(prompt("Enter your marks:"));

if (marks >= 90) {
  console.log("Grade A");
} else if (marks >= 75) {
  console.log("Grade B");
} else if (marks >= 50) {
  console.log("Grade C");
} else {
  console.log("Fail");
}
```

---

# 🟧 **Task 3 — Simple Calculator (switch)**

### 🎯 Description

Ask user:

* number1
* number2
* operator: +, -, *, /

Perform operation.

### 📘 Concepts

`switch`, operators.

### 💻 Code

```js
let a = Number(prompt("Enter number 1:"));
let b = Number(prompt("Enter number 2:"));
let op = prompt("Enter operator (+, -, *, /):");

switch (op) {
  case "+":
    console.log(a + b);
    break;
  case "-":
    console.log(a - b);
    break;
  case "*":
    console.log(a * b);
    break;
  case "/":
    console.log(a / b);
    break;
  default:
    console.log("Invalid Operator");
}
```

---

# 🟨 **Task 4 — Max of Three Numbers (Function)**

### 🎯 Description

Create a function that takes 3 numbers and returns the greatest.

### 📘 Concepts

Functions, return, parameters.

### 💻 Code

```js
function maxOfThree(a, b, c) {
  if (a >= b && a >= c) return a;
  if (b >= a && b >= c) return b;
  return c;
}

console.log(maxOfThree(10, 25, 15));
```

---

# 🟪 **Task 5 — Discount Calculator (Default Parameter)**

### 🎯 Description

Write a function:
`calculate(price, quantity, tax = 0.18)`
Return final amount.

### 📘 Concepts

Default values + return.

### 💻 Code

```js
function calculate(price, qty, tax = 0.18) {
  let subtotal = price * qty;
  return subtotal + subtotal * tax;
}

console.log(calculate(1000, 2)); // tax default = 18%
```

---

# 🟥 **Task 6 — Greeting Function (Arrow Function)**

### 🎯 Description

Use an arrow function to greet a person by name.

### 📘 Concepts

Arrow functions.

### 💻 Code

```js
const greet = (name) => {
  console.log("Hello " + name + "!");
};

greet("Rahil");
```

---

# 🟫 **Task 7 — Check if Number is Prime (Function + Logic)**

### 🎯 Description

Write a function that returns:

* `"Prime"` or `"Not Prime"`

### 📘 Concepts

Loops + return + conditions.

### 💻 Code

```js
function isPrime(n) {
  if (n <= 1) return "Not Prime";

  for (let i = 2; i < n; i++) {
    if (n % i === 0) return "Not Prime";
  }

  return "Prime";
}

console.log(isPrime(17));
```

---

# 🟦 **Task 8 — Cart Total Using Function Expression**

### 🎯 Description

Use a function expression to calculate:
`price * quantity`.

### 📘 Concepts

Function expressions, operators.

### 💻 Code

```js
const total = function(price, qty) {
  return price * qty;
};

console.log(total(500, 3));
```

---

# 🟩 **Task 9 — Recursion Basics: Countdown**

### 🎯 Description

Create a function:
`countDown(5)`
Output:

```
5
4
3
2
1
Done!
```

### 📘 Concepts

Recursion.

### 💻 Code

```js
function countDown(n) {
  if (n === 0) {
    console.log("Done!");
    return;
  }

  console.log(n);
  countDown(n - 1);
}

countDown(5);
```

---

# 🟧 **Task 10 — Sum of Numbers Using Recursion**

### 🎯 Description

Create a function:
`sum(n)`
Return sum of 1 to n.

Example:
`sum(5) = 1+2+3+4+5 = 15`

### 📘 Concepts

Recursion, return.

### 💻 Code

```js
function sum(n) {
  if (n === 1) return 1;
  return n + sum(n - 1);
}

console.log(sum(5)); // 15
```

---

