---
title: Home
---

# James "Jimmy" Fumo
I am a researcher studying xyz.

<div class="slider-container">
  <button class="slider-btn prev" onclick="changeSlide(-1)">❮</button>

  <div class="slides">
    <img class="slide active" src="/assets/images/banner1.jpg">
    <img class="slide" src="/assets/images/banner2.jpg">
    <img class="slide" src="/assets/images/banner3.jpg">
  </div>

  <button class="slider-btn next" onclick="changeSlide(1)">❯</button>
</div>

<style>
.slider-container {
  position: relative;
  max-width: 100%;
  height: 400px;
  overflow: hidden;
  border-radius: 10px;
}

.slides {
  position: relative;
  width: 100%;
  height: 100%;
}

.slide {
  position: absolute;
  width: 100%;
  height: 100%;
  object-fit: cover;
  opacity: 0;
  transition: opacity 0.8s ease-in-out;
}

.slide.active {
  opacity: 1;
}

.slider-btn {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(0,0,0,0.4);
  color: white;
  border: none;
  padding: 10px 15px;
  font-size: 20px;
  cursor: pointer;
  border-radius: 5px;
}

.prev { left: 10px; }
.next { right: 10px; }

.slider-btn:hover {
  background: rgba(0,0,0,0.7);
}
</style>

<script>
let currentSlide = 0;
const slides = document.querySelectorAll('.slide');

function showSlide(index) {
  slides.forEach((slide, i) => {
    slide.classList.remove('active');
    if (i === index) slide.classList.add('active');
  });
}

function changeSlide(direction) {
  currentSlide += direction;
  if (currentSlide < 0) currentSlide = slides.length - 1;
  if (currentSlide >= slides.length) currentSlide = 0;
  showSlide(currentSlide);
}

// Auto-slide every 5 seconds
setInterval(() => {
  changeSlide(1);
}, 5000);
</script>
---
Email: jfumo@hawaii.edu
