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
    var greetings = [
      {% for item in site.data.hello %}
        "{{ item.hello }}" {% unless forloop.last %},{% endunless %}
      {% endfor %}
    ];

    if (greetings.length === 0) return; // safety check

    var current = 0;
    var display = document.getElementById("greeting-display");

    function rotateGreeting() {
      display.innerText = greetings[current];
      current = (current + 1) % greetings.length;
    }

    rotateGreeting(); // first greeting
    setInterval(rotateGreeting, 1000);
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
