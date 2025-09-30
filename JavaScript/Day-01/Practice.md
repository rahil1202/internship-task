---

# 🧑‍💻 Day 1 – JavaScript Fundamentals Exercises

## 🧩 Part 1: Basic Setup

**Task 1:**

* Create a new folder `day1-js-basics`.
* Inside it, create:

  * `index.html`
  * `script.js`

**Task 2:**

* Link `script.js` to your HTML file using the `<script>` tag.
* Test by printing `"JS Connected Successfully!"` in the console.

---

## 📝 Part 2: Variables & Data Types (30 min)

1. **Variable Practice:**

   * Declare 3 variables: `name`, `age`, `city`
   * Assign them your own values.
   * Print them using:

     * `console.log()`
     * A sentence using **string concatenation**
     * A sentence using **template literals**

   ✅ Example Output:

   ```
   Name: Alice
   Age: 22
   City: London
   Hello, my name is Alice. I am 22 years old and live in London.
   ```

2. **Data Type Check:**

   * Declare variables with each data type: `string`, `number`, `boolean`, `null`, and `undefined`.
   * Use `typeof` to print the type of each variable.

   ✅ Example:

   ```
   string
   number
   boolean
   object
   undefined
   ```

---

## 🔢 Part 3: Type Conversion (20 min)

1. Convert a string `"42"` to a number using `Number()` and `parseInt()`.
2. Convert a number `100` to a string using `String()` and `.toString()`.
3. Convert `0`, `""`, `"hello"`, and `null` to boolean using `Boolean()`. Print results.

✅ Example Output:

```
"42" → 42
100 → "100"
0 → false
"" → false
"hello" → true
null → false
```

---

## ➕ Part 4: Operators Practice (20 min)

1. Create two variables: `num1 = 15`, `num2 = 4`.
2. Use all arithmetic operators and print results:

* Addition
* Subtraction
* Multiplication
* Division
* Modulus
* Exponentiation

✅ Example Output:

```
15 + 4 = 19
15 - 4 = 11
15 * 4 = 60
15 / 4 = 3.75
15 % 4 = 3
15 ** 4 = 50625
```

---

## 🧠 Part 5: Mini Project – "Personal Info Card" (40 min)

**Goal:** Combine HTML, CSS, and JS skills.

### 🛠️ Instructions:

1. In `index.html`:

   * Create three input fields: Name, Age, City
   * Add a button: **"Show Info"**
   * Add a `<p>` tag with `id="output"` to display the result

2. In `style.css`:

   * Style inputs and button (padding, margin, border, etc.)

3. In `script.js`:

   * On button click:

     * Read values from inputs
     * Use **template literals** to display a sentence:

       ```
       Hello [Name]! You are [Age] years old and live in [City].
       ```

✅ Example Output:

```
Hello Alice! You are 22 years old and live in London.
```

---

## 🎯 Bonus Challenge (Optional)

* Add a feature to calculate and display the **birth year** based on age.
* Add validation: if any field is empty, show `"Please fill out all fields."`

---

## 📁 Submission

* Folder structure:

  ```
  day1-js-basics/
   ├─ index.html
   ├─ style.css
   └─ script.js
  ```



Would you like me to generate this exercise sheet as a downloadable **`.md`** or **`.docx`** file to share with interns? (I can prepare it for you 📄)
