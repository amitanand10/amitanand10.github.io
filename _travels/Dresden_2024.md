---
layout: page
title: Dresden 2024
description: with background image
img: assets/img/Dresden_2024/Img1.png
importance: 2
category: work
related_publications: true
---


{% assign pics = 
  [
    { img: "./assets/img/Dresden_2024/Img2.jpg", caption: "" },
    { img: "./assets/img/Dresden_2024/Img3.jpg", caption: "" },
    { img: "/assets/img/Dresden_2024/Img4.jpg", caption: "" },
    { img: "/assets/img/Dresden_2024/Img5.jpg", caption: "" },
    { img: "/assets/img/Dresden_2024/6Img.jpg", caption: "" },
    { img: "./assets/img/Dresden_2024/Img7.jpg", caption: "" },
    { img: "/assets/img/Dresden_2024/Img8.jpg", caption: "" },
    { img: "/assets/img/Dresden_2024/Img9.jpg", caption: "C" },
    { img: "/assets/img/Dresden_2024/Img10.jpg", caption: "" }
  ]
%}

{% for pic in pics %}
<div style="margin-bottom: 1.5em;">
  <img src="{{ pic.img }}" alt="Travel photo" style="width:100%; max-width:600px; display:block; margin:auto;">
  {% if pic.caption %}
    <div style="text-align:center; font-size:0.95em; color:#666; margin-top:0.5em;">{{ pic.caption }}</div>
  {% endif %}
</div>
{% endfor %}




{% endraw %}
