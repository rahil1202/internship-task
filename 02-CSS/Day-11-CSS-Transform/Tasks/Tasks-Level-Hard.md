# HIGHLY OPTIONAL

## 🔥 **Task 1: Rotating 3D Navigation Wheel**

**Concept:** A circular nav that spins in 3D — each menu item rotates around a center point.
**You’ll practice:** `rotateY`, `translateZ`, and synchronized keyframes.

---

### 💡 How to do it:

1. Wrap menu items inside a rotating `.wheel`.
2. Place each item around a circular 3D path using `rotateY` and `translateZ`.
3. Spin the `.wheel` continuously.

```html
<div class="scene">
  <div class="wheel">
    <div>🏠</div>
    <div>📦</div>
    <div>📞</div>
    <div>🛍️</div>
    <div>⚙️</div>
  </div>
</div>

<style>
.scene {
  perspective: 1000px;
  width: 200px;
  height: 200px;
  margin: 80px auto;
}
.wheel {
  width: 100%; height: 100%;
  position: relative;
  transform-style: preserve-3d;
  animation: spinWheel 10s linear infinite;
}
.wheel div {
  position: absolute;
  width: 60px; height: 60px;
  background: #3498db;
  color: white; font-size: 28px;
  border-radius: 50%;
  display: flex; justify-content: center; align-items: center;
  transform-origin: center;
}
.wheel div:nth-child(1) { transform: rotateY(0deg) translateZ(120px); }
.wheel div:nth-child(2) { transform: rotateY(72deg) translateZ(120px); }
.wheel div:nth-child(3) { transform: rotateY(144deg) translateZ(120px); }
.wheel div:nth-child(4) { transform: rotateY(216deg) translateZ(120px); }
.wheel div:nth-child(5) { transform: rotateY(288deg) translateZ(120px); }

@keyframes spinWheel {
  to { transform: rotateY(360deg); }
}
</style>
```

✅ **Use Case:** Creative navigation, feature carousel, or icon showcase.
🧠 Teaches: evenly distributing elements around 3D space.

### OUTPUT


https://github.com/user-attachments/assets/c3621705-6c4f-468b-b73d-e1582fc62a10



---

## 🧊 **Task 2: Interactive 3D Product Cube**

**Concept:** A cube that pauses and highlights the face you hover over.
**You’ll practice:** combining animation, `rotateX/Y`, and hover interactivity.

---

### 💡 How to do it:

1. Create a cube using 6 faces.
2. Make it auto-rotate.
3. Pause rotation on hover and slightly scale up.

```html
<div class="cube-scene">
  <div class="cube">
    <div class="face front">Front</div>
    <div class="face back">Back</div>
    <div class="face left">Left</div>
    <div class="face right">Right</div>
    <div class="face top">Top</div>
    <div class="face bottom">Bottom</div>
  </div>
</div>

<style>
.cube-scene {
  perspective: 1000px;
  width: 180px; height: 180px;
  margin: 80px auto;
}
.cube {
  position: relative;
  width: 100%; height: 100%;
  transform-style: preserve-3d;
  animation: spin 8s linear infinite;
  transition: transform 0.3s ease;
}
.face {
  position: absolute;
  width: 180px; height: 180px;
  display: flex; justify-content: center; align-items: center;
  background: #8e44ad;
  color: white; font-weight: bold;
  border: 2px solid #fff;
  border-radius: 8px;
}
.front  { transform: translateZ(90px); }
.back   { transform: rotateY(180deg) translateZ(90px); }
.left   { transform: rotateY(-90deg) translateZ(90px); }
.right  { transform: rotateY(90deg) translateZ(90px); }
.top    { transform: rotateX(90deg) translateZ(90px); }
.bottom { transform: rotateX(-90deg) translateZ(90px); }

@keyframes spin {
  to { transform: rotateX(360deg) rotateY(360deg); }
}
.cube:hover {
  animation-play-state: paused;
  transform: scale(1.1);
}
</style>
```

✅ **Use Case:** Product previews, 3D logo displays, dashboard animation.
🧠 Teaches: mixing animation state + hover control.

### OOUTPUT

https://github.com/user-attachments/assets/b09980c9-da1d-4e90-a3be-29a87a4bfe62


---

## 💫 **Task 3: 3D Tilt Gallery (Mouse Parallax Effect)**

**Concept:** Move mouse to tilt a gallery wall in 3D perspective.
**You’ll practice:** `rotateX/Y` with JS control + perspective.

---

### 💡 How to do it:

1. Create a `.wall` of images.
2. Use JavaScript to rotate it as you move the mouse.

```html
<div class="gallery-scene">
  <div class="wall">
    <img src="https://picsum.photos/150?1">
    <img src="https://picsum.photos/150?2">
    <img src="https://picsum.photos/150?3">
  </div>
</div>

<style>
.gallery-scene {
  perspective: 1000px;
  width: 480px; height: 180px;
  margin: 100px auto;
}
.wall {
  display: flex; gap: 15px;
  transform-style: preserve-3d;
  transition: transform 0.1s ease;
}
.wall img {
  width: 150px; height: 150px;
  border-radius: 8px;
  box-shadow: 0 10px 20px rgba(0,0,0,0.2);
}
</style>

<script>
const wall = document.querySelector('.wall');
document.querySelector('.gallery-scene').addEventListener('mousemove', e => {
  const rect = e.currentTarget.getBoundingClientRect();
  const x = e.clientX - rect.left - rect.width/2;
  const y = e.clientY - rect.top - rect.height/2;
  const rotateX = (y / rect.height) * -15;
  const rotateY = (x / rect.width) * 15;
  wall.style.transform = `rotateX(${rotateX}deg) rotateY(${rotateY}deg)`;
});
document.querySelector('.gallery-scene').addEventListener('mouseleave', () => {
  wall.style.transform = 'rotateX(0) rotateY(0)';
});
</script>
```

✅ **Use Case:** Interactive galleries, portfolio sections, or hero headers.
🧠 Teaches: dynamic transforms from mouse input.
### OUTPUT



https://github.com/user-attachments/assets/fa5e2700-c2e3-49f5-9834-99a3a7174de9


---

## 🌌 **Task 4: 3D Space Card Hover (Depth Illusion)**

**Concept:** Give depth illusion using subtle 3D transforms and shadows.
**You’ll practice:** `translateZ`, perspective, transitions.

---

### 💡 How to do it:

1. Create a 3D scene with a card.
2. On hover, move it slightly forward in depth and tilt.

```html
<div class="depth-scene">
  <div class="depth-card">
    <h2>Galaxy</h2>
    <p>Explore beyond limits 🌌</p>
  </div>
</div>

<style>
.depth-scene {
  perspective: 800px;
  width: 280px; height: 180px;
  margin: 80px auto;
}
.depth-card {
  width: 100%; height: 100%;
  background: linear-gradient(135deg, #1e3c72, #2a5298);
  color: white;
  border-radius: 10px;
  display: flex; flex-direction: column; align-items: center; justify-content: center;
  box-shadow: 0 5px 15px rgba(0,0,0,0.3);
  transition: transform 0.4s ease, box-shadow 0.4s ease;
}
.depth-card:hover {
  transform: translateZ(60px) rotateX(6deg) rotateY(-6deg);
  box-shadow: 0 15px 25px rgba(0,0,0,0.4);
}
</style>
```

✅ **Use Case:** Modern product, feature, or portfolio cards.
🧠 Teaches: realism through subtle perspective.
### OUTPUT


https://github.com/user-attachments/assets/03e549ce-9f68-4a42-893f-75792d59cc18



---

## 🪄 **Task 5: 3D Fold-out Menu (Door Animation + Depth)**

**Concept:** Create a menu that folds open like a book using 3D rotation.
**You’ll practice:** `transform-origin`, `rotateY`, perspective.

---

### 💡 How to do it:

1. Wrap two menu “pages” side-by-side.
2. Rotate one side like a door using `rotateY`.

```html
<div class="menu-scene">
  <div class="menu">
    <div class="left">MENU</div>
    <div class="right">
      <a href="#">Home</a>
      <a href="#">Shop</a>
      <a href="#">About</a>
    </div>
  </div>
</div>

<style>
.menu-scene {
  perspective: 900px;
  width: 300px; height: 200px;
  margin: 80px auto;
}
.menu {
  display: flex; width: 100%; height: 100%;
  transform-style: preserve-3d;
}
.left, .right {
  width: 50%; height: 100%;
  display: flex; flex-direction: column; align-items: center; justify-content: center;
  background: #34495e; color: white;
  font-size: 22px; font-weight: bold;
  border: 2px solid white;
  transition: transform 1s ease;
  transform-origin: left;
}
.right {
  background: #2ecc71;
  transform-origin: left;
}
.menu:hover .right {
  transform: rotateY(-120deg);
}
.right a {
  color: white; text-decoration: none;
  margin: 6px 0;
}
</style>
```

✅ **Use Case:** Side panels, login forms, onboarding screens.
🧠 Teaches: door-like 3D motion & transform-origin precision.
### OUTPUT


https://github.com/user-attachments/assets/b838af1a-2af6-4c66-9a50-f3a5f2fe9f34


---

# 🎯 Summary Table

| Task                 | Concept                  | Techniques Practiced       |
| -------------------- | ------------------------ | -------------------------- |
| 1. Rotating 3D Wheel | Circular motion          | rotateY + translateZ       |
| 2. Product Cube      | 3D cube with hover pause | rotateX/Y, preserve-3d     |
| 3. Tilt Gallery      | Mouse parallax           | rotateX/Y + JS             |
| 4. Space Card        | Depth illusion           | translateZ + subtle tilt   |
| 5. Fold-out Menu     | Door rotation            | rotateY + transform-origin |

---
