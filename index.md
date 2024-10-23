---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
top_img: assets/images/Corfu1.png
second_img: assets/images/corfu2.png
third_img: assets/images/corfu3.png
---

<div class="slider-container">
  <div class="slider">
    <div class="slide">
      <img src="{{ site.baseurl }}/{{ page.top_img }}" alt="Corfu 1">
    </div>
    <div class="slide">
      <img src="{{ site.baseurl }}/{{ page.second_img }}" alt="Corfu 2">
    </div>
    <div class="slide">
      <img src="{{ site.baseurl }}/{{ page.third_img }}" alt="Corfu 3">
    </div>
  </div>
</div>

<style>
  .slider-container {
    width: 100%;
    overflow: hidden;
  }

  .slider {
    display: flex;
    transition: transform 0.5s ease-in-out;
  }

  .slide {
    min-width: 100%;
    box-sizing: border-box;
  }

  .slide img {
    width: 100%;
    height: auto;
  }
</style>

