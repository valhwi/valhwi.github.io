---
permalink: /
title: "Valerie"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
## <br>
<div style="text-align:center;">
  <div id="greeting-display" style="text-align:center; font-size:24px; margin-top:20px;">
  Welcome!
  <ul style="list-style:none; padding:0;">
    {% for item in site.data.hello %}
      <li>
        <strong>{{ item.language }} ({{ item.country }}):</strong> {{ item.hello }}
      </li>
    {% endfor %}
  </ul>
</div>
</div>

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
