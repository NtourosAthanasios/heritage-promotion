---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
top_img: assets/images/Corfu1.png
second_img: assets/images/corfu2.png
third_img: assets/images/corfu3.png
---
<div>
    <img src="{{ page.top_img }}" alt="Corfu 1" style="width: 100%; height: 100px; object-fit: cover;">
</div>


<div class="slider-container">
  <div class="slider">
    <div class="slide">
      <img src="{{ page.top_img }}" alt="Corfu 1">
    </div>
    <div class="slide">
      <img src="{{ page.second_img }}" alt="Corfu 2">
    </div>
    <div class="slide">
      <img src="{{ page.third_img }}" alt="Corfu 3">
    </div>
  </div>
  <button class="prev" onclick="moveSlide(-1)">&#10094;</button>
  <button class="next" onclick="moveSlide(1)">&#10095;</button>
</div>


<script>
  let currentIndex = 0;

  function showSlide(index) {
    const slides = document.querySelectorAll('.slide');
    const totalSlides = slides.length;

    // Wrap around the index
    if (index >= totalSlides) {
      currentIndex = 0;
    } else if (index < 0) {
      currentIndex = totalSlides - 1;
    } else {
      currentIndex = index;
    }

    // Calculate the offset
    const offset = -currentIndex * 100; // -100% for each slide
    document.querySelector('.slider').style.transform = `translateX(${offset}%)`;
  }

  function moveSlide(step) {
    showSlide(currentIndex + step);
  }

  // Show the first slide initially
  showSlide(currentIndex);
</script>


<style>
  .slider-container {
    position: relative;
    max-width: 100%; /* Adjust this for your design */
    overflow: hidden;
  }

  .slider {
    display: flex;
    transition: transform 0.5s ease-in-out;
  }

  .slide {
    min-width: 100%; /* Each slide takes up the full container */
    box-sizing: border-box;
  }

  .slide img {
    width: 100%;
    height: auto; /* Ensures images scale correctly */
  }

  .prev, .next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background-color: rgba(255, 255, 255, 0.5);
    border: none;
    cursor: pointer;
    padding: 10px;
    font-size: 18px;
    z-index: 10; /* Make sure buttons are on top */
  }

  .prev {
    left: 10px;
  }

  .next {
    right: 10px;
  }
</style>
