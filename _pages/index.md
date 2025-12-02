---
permalink: /
author_profile: true

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

<div style="display: flex; justify-content: center; margin-top: 10px;">
    <img src="{{ base_path }}/images/main.jpg" width="500" height="400">>
</div>
<br>
<div style="display: flex; flex-direction: column; align-items: center; gap: 5px;">
  <iframe src="https://free.timeanddate.com/clock/ia6k1lz0/n259/fn2/fs16/tct/pct/ftb/bas2/bat1/bacfff/pa8/tt0/tw0/th1/ta1" frameborder="0" width="338" height="42" allowtransparency="true"></iframe>
  <iframe src="https://free.timeanddate.com/clock/ia6k1gdm/n145/fn2/fs16/tct/pct/ftb/bas2/bat1/bacfff/pa8/tt0/tw0/th1/ta1" frameborder="0" width="351" height="42" allowtransparency="true"></iframe>
</div>


