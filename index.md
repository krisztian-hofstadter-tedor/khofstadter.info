---
title: tEdör aka Krisztián Hofstädter
layout: default
---
Hello! My name is Krisztián Hofstädter, aka tEdör. I am a creative technologist working as a researcher, lecturer, freelancer and artist. This website informs you about my work. My cv is [here](https://khofstadter.info/assets/doc/KHofstader-CV.pdf).

<div class="tab">
  organised
  
  <button class="tablinks" onclick="openCity(event, 'categories')" id="defaultOpen" >by main theme</button>
  or 
  <button class="tablinks" onclick="openCity(event, 'time')">chronologically</button> or 
  <button class="tablinks" onclick="openCity(event, 'tags')">by tags</button>
  
</div>

<div id="time" class="tabcontent">
  <h3>ongoing</h3>
  {% include index-cron-ongoing.html %}
  <h3>past</h3>
  {% include index-cron.html %}
</div>

<div id="categories" class="tabcontent">
  {% include index-cat.html %}
</div>

<div id="tags" class="tabcontent">
  {% include index-tags.html %}
</div>

<br>

For feedback and questions please use the discussion sections at the end of the posts or email me at kris[at]khofstadter[dot]info.

<br>

<script>
function openCity(evt, cityName) {
    var i, tabcontent, tablinks;
    tabcontent = document.getElementsByClassName("tabcontent");
    for (i = 0; i < tabcontent.length; i++) {
        tabcontent[i].style.display = "none";
    }
    tablinks = document.getElementsByClassName("tablinks");
    for (i = 0; i < tablinks.length; i++) {
        tablinks[i].className = tablinks[i].className.replace(" active", "");
    }
    document.getElementById(cityName).style.display = "block";
    evt.currentTarget.className += " active";
}

// Get the element with id="defaultOpen" and click on it
document.getElementById("defaultOpen").click();
</script>
