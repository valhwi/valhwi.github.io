permalink: /
title: "Valerie"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<div style="text-align:center;">
  <div id="greeting-display" style="text-align:center; font-size:24px; margin-top:20px;">
    Welcome!
  </div>
</div>

<script>
  document.addEventListener("DOMContentLoaded", function() {
    const greetings = [
      {% for item in site.data.hello %}
        { language: "{{ item.language }}", country: "{{ item.country }}", hello: "{{ item.hello }}" }{% if forloop.last == false %},{% endif %}
      {% endfor %}
    ];

    let current = 0;
    const display = document.getElementById("greeting-display");

    function showNextGreeting() {
      const item = greetings[current];
      display.innerHTML = `${item.hello} (${item.language}, ${item.country})`;
      current = (current + 1) % greetings.length;
    }

    showNextGreeting();
    setInterval(showNextGreeting, 3000);
  });
</script>

<br>
<div style="display: flex; justify-content: center;">
  <iframe width="560" height="315" 
          src="https://www.youtube.com/embed/wccRif2DaGs?si=3A9m4vGoqTt7PypL" 
          title="YouTube video player" 
          frameborder="0" 
          allowfullscreen></iframe>
</div>
<br>
<div style="display: flex; justify-content: center; gap: 10px;">
  <iframe src="https://free.timeanddate.com/clock/i9stvqo9/n16/fcfff/tc000/ftb/pa8/tt0/th1/ta1/tb4" 
          frameborder="0" 
          width="231" 
          height="50"></iframe>
  <iframe src="https://free.timeanddate.com/clock/i9stvqo9/n145/fcfff/tc000/ftb/pa8/tt0/th1/ta1/tb4" 
          frameborder="0" 
          width="231" 
          height="50"></iframe>
</div>
