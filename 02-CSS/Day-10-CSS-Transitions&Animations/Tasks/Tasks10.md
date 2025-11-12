
## 🌈 Task 1 — **Smooth Fade-in & Slide-up on Load**

```html
<div class="fade-up">Welcome Aboard 🚀</div>

<style>
.fade-up {
  opacity: 0;
  transform: translateY(30px);
  animation: fadeUp 1s ease-out forwards;
}

@keyframes fadeUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
```

### Output

https://github.com/user-attachments/assets/0a88a720-d859-4abf-ba96-7199c49a36fc


✅ **What it shows:** Smooth entry animation for text or images when a page loads.
💡 Commonly used in hero headers, modals, or section reveals.

---

## 🌀 Task 2 — **Spinning Icon (Loader)**

```html
<div class="spinner"></div>

<style>
.spinner {
  width: 60px;
  height: 60px;
  border: 6px solid #ccc;
  border-top: 6px solid #3498db;
  border-radius: 50%;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  to {
    transform: rotate(360deg);
  }
}
</style>
```
### OUTPUT

https://github.com/user-attachments/assets/fded3ff1-960b-476c-9b7d-bb6f5f474c60

✅ **What it shows:** Infinite rotation with a linear timing — perfect for loaders or indicators.

---

## 💫 Task 3 — **Bouncing Ball**

```html
<div class="ball"></div>

<style>
.ball {
  width: 70px;
  height: 70px;
  background: #e74c3c;
  border-radius: 50%;
  position: relative;
  animation: bounce 0.8s ease-in-out infinite alternate;
}

@keyframes bounce {
  from { transform: translateY(0); }
  to { transform: translateY(150px); }
}
</style>
```
### OUTPUT


https://github.com/user-attachments/assets/19d56513-9bc2-4b77-a23a-a20b86e697e7



✅ **What it shows:** Using `alternate` to make it bounce up and down endlessly.
💡 Great for attention animations (like chat heads or “scroll down” hints).

---

## 🌟 Task 4 — **Typing Text Effect**

```html
<h2 class="typing">Frontend Developer</h2>

<style>
.typing {
  width: 17ch;
  overflow: hidden;
  border-right: 2px solid black;
  white-space: nowrap;
  animation: typing 3s steps(17), blink 0.6s step-end infinite alternate;
}

@keyframes typing {
  from { width: 0; }
  to { width: 17ch; }
}
@keyframes blink {
  from { border-color: transparent; }
  to { border-color: black; }
}
</style>
```
### OUTPUT


https://github.com/user-attachments/assets/21bb815d-bbfb-4a09-b580-cd3003a4f73a



✅ **What it shows:** Steps-based animation — creates the illusion of typing one letter at a time.
💡 Commonly used in portfolio hero text or command-line style UIs.

---

## 🧠 Task 5 — **Hover Button with Color & Scale Transition**

```html
<button class="grow-btn">Hover Me</button>

<style>
.grow-btn {
  background: #27ae60;
  color: white;
  border: none;
  padding: 15px 30px;
  border-radius: 6px;
  font-size: 16px;
  cursor: pointer;
  transition: background 0.4s ease, transform 0.2s ease;
}
.grow-btn:hover {
  background: #2ecc71;
  transform: scale(1.1);
}
.grow-btn:active {
  transform: scale(0.95);
}
</style>
```
### Output



https://github.com/user-attachments/assets/ae3aced3-046f-4957-83c0-b3cab6549db7


✅ **What it shows:** Combining transitions for multiple states — smooth hover and press feedback.

---

## 🔥 Task 6 — **Card Lift on Hover (with Shadow Transition)**

```html
<div class="card">Hover to Lift</div>

<style>
.card {
  width: 200px;
  height: 120px;
  background: #8e44ad;
  color: white;
  text-align: center;
  line-height: 120px;
  border-radius: 10px;
  transition: transform 0.4s ease, box-shadow 0.4s ease;
}
.card:hover {
  transform: translateY(-15px);
  box-shadow: 0 10px 20px rgba(0,0,0,0.3);
}
</style>
```
### Output


https://github.com/user-attachments/assets/ee6edf3e-e625-4da8-9c30-598e4b4a3f2a



✅ **What it shows:** Subtle depth illusion using translate and shadow.
💡 Great for cards, tiles, or any interactive element.

---

## 🎡 Task 7 — **Pulsing Heartbeat**

```html
<div class="heart">❤️</div>

<style>
.heart {
  font-size: 60px;
  animation: beat 0.9s ease-in-out infinite;
}

@keyframes beat {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.3); }
}
</style>
```
### Output


https://github.com/user-attachments/assets/efc9b22c-f984-4f0b-9a2d-5c2098f926a4

✅ **What it shows:** Looping `scale()` for a pulsing “heartbeat.”
💡 Used for “Like” icons, notifications, or playful elements.

---

## 🌈 Task 8 — **Color Wave Background Animation**

```html
<div class="gradient-bg"></div>

<style>
.gradient-bg {
  height: 200px;
  background: linear-gradient(270deg, #ff6b6b, #feca57, #1dd1a1, #54a0ff);
  background-size: 600% 600%;
  animation: wave 10s ease infinite;
}

@keyframes wave {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}
</style>
```

### Output


https://github.com/user-attachments/assets/d428612f-d138-4870-acf3-61a01ab3156b


✅ **What it shows:** Using gradient + background-position to make color waves move.
💡 Fantastic for headers, banners, or animated backgrounds.

---

## ⚡ Task 9 — **Fade & Slide-in Cards (Staggered Delay)**

```html
<div class="cards">
  <div class="card" style="--d:0s">Card 1</div>
  <div class="card" style="--d:0.2s">Card 2</div>
  <div class="card" style="--d:0.4s">Card 3</div>
</div>

<style>
.cards {
  display: flex;
  gap: 20px;
}

.card {
  background: #3498db;
  color: white;
  width: 100px;
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transform: translateY(20px);
  animation: fadeUp 1s ease forwards;
  animation-delay: var(--d);
}

@keyframes fadeUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
```

### Output

https://github.com/user-attachments/assets/9c80b9ac-7a4d-4c31-8294-9b202a6396e1


✅ **What it shows:** Delayed start for each element — sequential “fade up” animation.
💡 Great for grid or card reveal effects.

---

## 🧩 Task 10 — **Sliding Notification Toast**

```html
<div class="toast">✅ Saved Successfully!</div>

<style>
.toast {
  position: fixed;
  bottom: 20px;
  right: -300px;
  background: #2ecc71;
  color: white;
  padding: 15px 25px;
  border-radius: 6px;
  animation: slideIn 0.6s ease forwards, fadeOut 0.6s ease 3s forwards;
}

@keyframes slideIn {
  from { right: -300px; opacity: 0; }
  to { right: 20px; opacity: 1; }
}
@keyframes fadeOut {
  to { opacity: 0; transform: translateY(30px); }
}
</style>
```

### Output

https://github.com/user-attachments/assets/ecda77a4-77b5-4ad8-8f6e-877c66111a1c

✅ **What it shows:**

* Enters smoothly, stays visible for a few seconds, then fades away.
  💡 Perfect for notifications, alerts, or success messages.

---

# 🧠 What You Just Learned Through Practice

| Concept                      | Shown In    | Real-World Use                   |
| ---------------------------- | ----------- | -------------------------------- |
| Fade/slide transitions       | Ex. 1, 9    | Entrances, reveals               |
| Infinite looping             | Ex. 2, 3, 7 | Loaders, breathing icons         |
| Steps animation              | Ex. 4       | Typing or progress steps         |
| Easing & alternate           | Ex. 3, 7    | Natural motion                   |
| Shadow & scale transitions   | Ex. 5, 6    | UI feedback                      |
| Gradient & background motion | Ex. 8       | Animated visuals                 |
| Timing delays & chaining     | Ex. 9, 10   | Staggered effects                |
| Fill-mode & forwards         | Ex. 1, 10   | Keep final state after animation |

---

💡 **Pro tip:** Always pair animation with *purpose* — motion should guide attention, not distract it.


