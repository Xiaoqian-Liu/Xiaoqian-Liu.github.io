---
permalink: /Group/
title: "Group Members"
hide_title: true
---

## PhD Students

<ul class="talk-list">
  <li>
    <strong><a href="/files/CV_Xinhao.pdf">Xinhao Qu</a></strong>
    <span>PhD student in Statistics at UC Riverside · 02/2026–present</span>
  </li>
    <li>
    <strong>Hieu Hoang</strong>
    <span>PhD student in Statistics at UC Riverside · 07/2026–present</span>
  </li>
  <li>
    <strong>Jordyn Niemiec</strong>
    <span>PhD student in GGB at UC Riverside · 01/2026–present · Co-advised with Prof. Ernest Martinez</span>
  </li>
</ul>

---

## Group Photos

<div class="slideshow-container">
  <div class="slide active">
    <img src="/images/2026.9.25.JPG" />
    <div class="slide-title">First group get-together and celebration of the 2026 Moon Festival!</div>
    <div class="slide-caption">September 25, 2026</div>
  </div>
  <!-- Add more slides here as you take more group photos:
  <div class="slide">
    <img src="/images/your-next-photo.jpg" alt="Group photo – [date]" />
    <div class="slide-caption">[date]</div>
  </div>
  -->
</div>

<div class="slideshow-controls">
  <button class="prev-btn" onclick="changeSlide(-1)">&#10094;</button>
  <div class="dots-container" id="dots"></div>
  <button class="next-btn" onclick="changeSlide(1)">&#10095;</button>
</div>

<style>
.slideshow-container {
  max-width: 720px;
  margin: 2em auto 0.5em auto;
  position: relative;
  overflow: hidden;
  border-radius: 8px;
  
}

.slide {
  display: none;
  text-align: center;
}

.slide.active {
  display: block;
}

.slide img {
  width: 100%;
  max-height: 480px;
  object-fit: contain;
  border-radius: 8px;
}

.slide-title {
  padding: 0.6em 1em 0.1em;
  font-size: 1em;
  font-weight: 600;
  color: #333;
  text-align: center;
}

.slide-caption {
  padding: 0.5em 1em 0.8em;
  font-size: 0.9em;
  color: #555;
  font-style: italic;
}

.slideshow-controls {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1em;
  margin-bottom: 2em;
}

.prev-btn, .next-btn {
  background: none;
  border: 1px solid #ccc;
  border-radius: 50%;
  width: 36px;
  height: 36px;
  font-size: 1rem;
  cursor: pointer;
  color: #555;
  transition: background 0.2s, color 0.2s;
}

.prev-btn:hover, .next-btn:hover {
  background: #0092ca;
  color: white;
  border-color: #0092ca;
}

.dots-container {
  display: flex;
  gap: 6px;
}

.dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: #ccc;
  cursor: pointer;
  transition: background 0.2s;
}

.dot.active {
  background: #0092ca;
}
</style>

<script>
(function() {
  var slides = document.querySelectorAll('.slide');
  var dotsContainer = document.getElementById('dots');
  var current = 0;

  // Build dots
  slides.forEach(function(_, i) {
    var dot = document.createElement('span');
    dot.className = 'dot' + (i === 0 ? ' active' : '');
    dot.addEventListener('click', function() { goTo(i); });
    dotsContainer.appendChild(dot);
  });

  function goTo(n) {
    slides[current].classList.remove('active');
    document.querySelectorAll('.dot')[current].classList.remove('active');
    current = (n + slides.length) % slides.length;
    slides[current].classList.add('active');
    document.querySelectorAll('.dot')[current].classList.add('active');
  }

  window.changeSlide = function(dir) { goTo(current + dir); };

  // Auto-advance every 5 seconds when multiple slides exist
  if (slides.length > 1) {
    setInterval(function() { goTo(current + 1); }, 5000);
  }
})();
</script>
