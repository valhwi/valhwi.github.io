---
permalink: /
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<p style="text-align:center; font-size:40px; font-weight:bold;">
  <span id="greeting-display">Hello!</span>
</p>

<script>
document.addEventListener("DOMContentLoaded", function() {
  const display = document.getElementById("greeting-display");

  const greetings = [
    {% for item in site.data.hello %}
      "{{ item.hello }}"{% unless forloop.last %},{% endunless %}
    {% endfor %}
  ];

  let index = 0;

  setInterval(() => {
    display.textContent = greetings[index];
    index = (index + 1) % greetings.length;
  }, 500);
});
</script>

<div style="display: flex; justify-content: center;">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/wccRif2DaGs?si=3A9m4vGoqTt7PypL" title="YouTube video player" frameborder="0" allowfullscreen></iframe>
</div>

<br>
<div style="display: flex; justify-content: center; gap: 10px;">
<iframe src="https://free.timeanddate.com/clock/ia6i0sag/n259/fn2/fs16/ftb/bas2/bat0/bacfff/pa8/tt0/tw0/th1/ta1" frameborder="0" width="335" height="38"></iframe>
</div>
