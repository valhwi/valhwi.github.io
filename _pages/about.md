---
permalink: /
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<div id="greeting-display" style="text-align:center; font-size:24px; margin-top:20px; font-weight:bold;">
  Welcome!
</div>

<script>
  document.addEventListener("DOMContentLoaded", function() {
    // Safely convert JSON data to JS array
    var greetings = {{ site.data.hello | map: "hello" | jsonify }};

    console.log("Greetings array:", greetings); // check in browser console

    if (!greetings || greetings.length === 0) return;

    var current = 0;
    var display = document.getElementById("greeting-display");

    function rotateGreeting() {
      display.innerText = greetings[current];
      current = (current + 1) % greetings.length;
    }

    rotateGreeting(); // show first greeting immediately
    setInterval(rotateGreeting, 1000); // rotate every 2 seconds
  });
</script>


<br>

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
