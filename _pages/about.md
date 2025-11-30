---
permalink: /
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<div id="greeting-display" style="text-align:center; font-size:24px; font-weight:bold;">Welcome!</div>

<script>
fetch('/hello.json') // make sure hello.json is in your website root
  .then(response => response.json())
  .then(greetings => {
    let current = 0;
    const display = document.getElementById('greeting-display');
    function showNextGreeting() {
      const item = greetings[current];
      display.textContent = `${item.hello} (${item.language}, ${item.country})`;
      current = (current + 1) % greetings.length;
    }
    showNextGreeting();
    setInterval(showNextGreeting, 1000);
  })
  .catch(console.error);
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
