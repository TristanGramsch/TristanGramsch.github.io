---
layout: page
title: About me
permalink: /about/
weight: 1
---
<!--html is a vast sea of code
press ctrl + shift + z to comment
You can make HTML run CSS code using the style argument inside an html command.
For example: <p style="text-align: justify;">
 -->
<p style="text-align: justify;">
<span style="background-color: #4485b8; color: #fff; display: inline-block; padding: 2px 8px; font-weight: bold; border-radius: 5px;">
<font size="+2">
Welcome.
</font>
</span>
</p>

<p style="text-align: justify; text-indent: 30px;">
<font size="+1">

This website showcases part of my journey in life. I am a sociologist by education and data scientist by profession. I finished a sociology undergrad in Chile and continued with a Master's in Chicago. As a sociologist, I thoroughly studied drug use and networks of support. In Chicago, I learned to code and got a job as a data scientist at the Cook County Assessor's Office. I had the privilege to work with a great team and a great mentor. My data skills reached a new level. Currently I work at Benchmark Analytics. 

<p>Here are some of my skills. Throughout the way I have been one of my best teachers. </p>

</font>
</p>

<div class="row">
{% include about/skills.html title="Machine learning" source=site.data.machine-learning %}
{% include about/skills.html title="Architecture development" source=site.data.architecture-development %}
</div>

# <span style="text-decoration: underline"> My timeline </span>
<div class="row">
{% include about/timeline.html %}
</div>
