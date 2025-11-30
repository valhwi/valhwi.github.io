---
permalink: /
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<p style="text-align:center; font-size:24px; font-weight:bold;">
  <span id="greeting-display">Welcome!</span>
</p>

<script>
document.addEventListener("DOMContentLoaded", function() {
  var display = document.getElementById("greeting-display");
  if (!display) {
    console.error("No element found with id 'greeting-display'");
    return;
  }

  // Fetch greetings from assets/hello.json
  fetch('/assets/hello.json')
    .then(response => response.json())
    .then(data => {
      // Extract 'hello' field from each JSON object
      var greetings = data.map(entry => entry.hello);
      var currentIndex = 0;

      function rotateGreeting() {
        display.innerText = greetings[currentIndex];
        currentIndex = (currentIndex + 1) % greetings.length;
      }

      rotateGreeting(); // show first greeting immediately
      setInterval(rotateGreeting, 1000); // rotate every second
    })
    .catch(err => console.error("Error loading JSON:", err));
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
