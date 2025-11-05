
## 🧩 **Task 1: Floating Product Card (2D Translate + Scale)**

**Concept:** Learn smooth 2D movement on hover with a realistic “lift” and “shadow.”
**You’ll practice:** `translateY()`, `scale()`, transitions.

### 💡 How to do it:

1. Create a simple product card.
2. On hover, make it lift slightly upward (`translateY`) and grow (`scale`).

```html
<div class="card">
  <img src="https://picsum.photos/200" alt="">
  <h3>Product Name</h3>
  <p>$49.99</p>
</div>

<style>
.card {
  width: 220px;
  text-align: center;
  border-radius: 10px;
  padding: 15px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.card:hover {
  transform: translateY(-10px) scale(1.05);
  box-shadow: 0 10px 20px rgba(0,0,0,0.2);
}
.card img { width: 100%; border-radius: 10px; }
</style>
```

✅ Use Case: Store cards, gallery tiles, blog previews.
🧠 Teaches: stacking multiple transform functions together.

### OUTPUT


https://github.com/user-attachments/assets/2f70db10-9722-493a-aef1-bec1d5387ff6

---

## 🌀 **Task 2: Rotating Arrow Button (2D Rotate)**

**Concept:** Use rotation to create clear visual feedback.
**You’ll practice:** `rotate()`, `transform-origin`.

### 💡 How to do it:

1. Make a button with an arrow (`▼`).
2. On hover, rotate the arrow 180° to point upward.

```html
<button class="dropdown">Menu ▼</button>

<style>
.dropdown {
  background: #3498db;
  color: white;
  font-size: 18px;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  transition: transform 0.3s ease;
  transform-origin: center;
}
.dropdown:hover {
  transform: rotate(180deg);
}
</style>
```

✅ Use Case: Dropdowns, accordions, toggle indicators.
🧠 Teaches: `transform-origin` and rotational feedback.

### OUTPUT


https://github.com/user-attachments/assets/53753bc4-247d-45b8-8617-5f67a89f5537



---

## 🧱 **Task 3: Slanted “SALE” Banner (2D Skew)**

**Concept:** Apply `skew()` to make stylized text effects.
**You’ll practice:** `skew()`, transitions.

### 💡 How to do it:

1. Create a “SALE” banner.
2. Tilt it diagonally using `skew()` on hover.

```html
<div class="banner">SALE 50% OFF</div>

<style>
.banner {
  background: #e74c3c;
  color: white;
  font-weight: bold;
  text-align: center;
  width: 250px;
  padding: 12px;
  font-size: 18px;
  transition: transform 0.4s ease;
}
.banner:hover {
  transform: skew(-15deg);
}
</style>
```

✅ Use Case: Discount banners, hero ribbons, promo strips.
🧠 Teaches: `skew()` to add dynamic tension to shapes.
### OUTPUT

https://github.com/user-attachments/assets/3f5a2afe-4fff-42c2-9999-8003a0c55df4

---

## 🧠 **Task 4: Spinning Loader (2D Rotate + Animation)**

**Concept:** Create infinite smooth rotation.
**You’ll practice:** `rotate()`, keyframes, infinite loop.

### 💡 How to do it:

1. Build a circular loader.
2. Continuously rotate using keyframes.

```html
<div class="loader"></div>

<style>
.loader {
  width: 70px;
  height: 70px;
  border: 6px solid #ccc;
  border-top: 6px solid #2ecc71;
  border-radius: 50%;
  animation: spin 1s linear infinite;
}
@keyframes spin {
  to { transform: rotate(360deg); }
}
</style>
```

✅ Use Case: Preloaders, waiting indicators.
🧠 Teaches: Using transforms in `@keyframes`.
### OUTPUT


https://github.com/user-attachments/assets/812f534a-325d-46b4-ba78-7a13416184c0



---

## 🌈 **Task 5: 3D Flip Card (rotateY + perspective)**

**Concept:** Learn 3D flipping between front and back faces.
**You’ll practice:** `rotateY`, `perspective`, `backface-visibility`.

### 💡 How to do it:

1. Create a `.scene` container with perspective.
2. Add a `.card` with `.front` and `.back` faces.
3. On hover, rotate the card.

```html
<div class="scene">
  <div class="card3d">
    <div class="front">FRONT</div>
    <div class="back">BACK</div>
  </div>
</div>

<style>
.scene {
  perspective: 800px;
  width: 200px;
  height: 120px;
}
.card3d {
  width: 100%; height: 100%;
  transform-style: preserve-3d;
  transition: transform 0.8s;
  position: relative;
}
.card3d:hover {
  transform: rotateY(180deg);
}
.front, .back {
  position: absolute;
  width: 100%; height: 100%;
  display: flex; justify-content: center; align-items: center;
  backface-visibility: hidden;
  border-radius: 10px; color: white; font-weight: bold;
}
.front { background: #2980b9; }
.back  { background: #27ae60; transform: rotateY(180deg); }
</style>
```

✅ Use Case: Profile cards, flip games, product back info.
🧠 Teaches: Perspective depth and hidden backfaces.

### OUTPUT


https://github.com/user-attachments/assets/098ef096-62cc-49ac-abc3-b9c8cb284c68


---

## 🎡 **Task 6: 3D Rotating Cube (rotateX + rotateY)**

**Concept:** Combine multiple 3D rotations to simulate a real cube.
**You’ll practice:** `preserve-3d`, `translateZ`, continuous keyframe rotation.

### 💡 How to do it:

1. Build a cube with 6 sides (`.face`).
2. Use keyframes to spin it endlessly.

```html
<div class="cube-scene">
  <div class="cube">
    <div class="face front">1</div>
    <div class="face back">2</div>
    <div class="face left">3</div>
    <div class="face right">4</div>
    <div class="face top">5</div>
    <div class="face bottom">6</div>
  </div>
</div>

<style>
.cube-scene {
  perspective: 900px;
  width: 150px; height: 150px;
  margin: 80px auto;
}
.cube {
  width: 100%; height: 100%;
  transform-style: preserve-3d;
  animation: spinCube 8s linear infinite;
  position: relative;
}
.face {
  position: absolute; width: 150px; height: 150px;
  display: flex; align-items: center; justify-content: center;
  font-size: 2em; color: white; font-weight: bold;
  background: rgba(52,152,219,0.9); border: 2px solid #fff;
}
.front  { transform: translateZ(75px); }
.back   { transform: rotateY(180deg) translateZ(75px); }
.left   { transform: rotateY(-90deg) translateZ(75px); }
.right  { transform: rotateY(90deg) translateZ(75px); }
.top    { transform: rotateX(90deg) translateZ(75px); }
.bottom { transform: rotateX(-90deg) translateZ(75px); }

@keyframes spinCube {
  0%   { transform: rotateX(0deg) rotateY(0deg); }
  100% { transform: rotateX(360deg) rotateY(360deg); }
}
</style>
```

✅ Use Case: 3D logos, data visualization cubes, portfolio highlights.
🧠 Teaches: advanced perspective & spatial arrangement.
### OUTPUT


https://github.com/user-attachments/assets/5b993a95-76cc-47f1-92ab-21411ac5e7a2



---

## 🪞 **Task 7: Interactive 3D Tilt Card (rotateX + rotateY)**

**Concept:** Create parallax-like tilt effect following mouse movement.
**You’ll practice:** subtle 3D rotation and responsiveness.

### 💡 How to do it:

1. Add a card in a perspective container.
2. Update `rotateX` and `rotateY` dynamically on mouse move.

```html
<div class="tilt-scene">
  <div class="tilt-card">MOVE MOUSE</div>
</div>

<style>
.tilt-scene {
  perspective: 1000px;
  width: 300px; height: 200px;
  margin: 80px auto;
}
.tilt-card {
  width: 100%; height: 100%;
  background: linear-gradient(135deg, #8e44ad, #3498db);
  color: white;
  font-size: 24px; font-weight: bold;
  display: flex; justify-content: center; align-items: center;
  border-radius: 15px;
  transition: transform 0.1s ease;
}
</style>

<script>
const card = document.querySelector('.tilt-card');
document.querySelector('.tilt-scene').addEventListener('mousemove', e => {
  const rect = e.currentTarget.getBoundingClientRect();
  const x = e.clientX - rect.left - rect.width / 2;
  const y = e.clientY - rect.top - rect.height / 2;
  const rotateX = (y / rect.height) * -15;
  const rotateY = (x / rect.width) * 15;
  card.style.transform = `rotateX(${rotateX}deg) rotateY(${rotateY}deg)`;
});
document.querySelector('.tilt-scene').addEventListener('mouseleave', () => {
  card.style.transform = 'rotateX(0) rotateY(0)';
});
</script>
```

✅ Use Case: Modern portfolio cards, dashboards, product showcases.
🧠 Teaches: Real-time transform manipulation + user interaction.

---

# 🎯 Summary Table

| Task               | Concept                  | Skills Practiced     |
| ------------------ | ------------------------ | -------------------- |
| 1. Floating Card   | translate, scale         | Hover interaction    |
| 2. Rotating Arrow  | rotate, transform-origin | Motion feedback      |
| 3. SALE Banner     | skew                     | Text effects         |
| 4. Spinning Loader | rotate + keyframes       | Infinite animation   |
| 5. Flip Card       | rotateY, perspective     | 3D flipping          |
| 6. Rotating Cube   | rotateX/Y, translateZ    | Spatial thinking     |
| 7. Tilt Card       | rotateX/Y (JS)           | Interactive parallax |

---
