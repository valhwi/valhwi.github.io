---
permalink: /
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<div style="text-align:center; margin-top:50px;">
  <span id="greeting-display" style="display:inline-block; font-size:36px; font-weight:bold; transition: transform 1s;">
    Loading...
  </span>
</div>

<script>
  document.addEventListener("DOMContentLoaded", function() {
    // Load greetings from Jekyll _data folder
    const greetings = {{ site.data.hello | jsonify }};
    
    // Function to pick a random greeting
    function randomGreeting() {
      const g = greetings[Math.floor(Math.random() * greetings.length)];
      return g.hello;
    }

    const greetingDisplay = document.getElementById("greeting-display");

    // Function to update greeting and apply rotation/movement
    function updateGreeting() {
      const text = randomGreeting();
      greetingDisplay.textContent = text;

      // Random rotation between -30deg and 30deg
      const rotation = Math.random() * 60 - 30;
      // Random horizontal movement between -50px and 50px
      const translateX = Math.random() * 100 - 50;
      // Random vertical movement between -20px and 20px
      const translateY = Math.random() * 40 - 20;

      greetingDisplay.style.transform = `translate(${translateX}px, ${translateY}px) rotate(${rotation}deg)`;
    }

    // Update greeting every 2 seconds
    updateGreeting(); // Initial call
    setInterval(updateGreeting, 2000);
  });
</script>


<!-- YouTube Video -->
<div style="display: flex; justify-content: center;">
  <iframe width="560" height="315" 
          src="https://www.youtube.com/embed/wccRif2DaGs?si=3A9m4vGoqTt7PypL" 
          title="YouTube video player" 
          frameborder="0" 
          allowfullscreen>
  </iframe>
</div>

<br>

<!-- Clocks -->
<div style="display: flex; justify-content: center; gap: 10px;">
  <iframe src="https://free.timeanddate.com/clock/i9stvqo9/n16/fcfff/tc000/ftb/pa8/tt0/th1/ta1/tb4" 
          frameborder="0" 
          width="231" 
          height="50">
  </iframe>
</div>
