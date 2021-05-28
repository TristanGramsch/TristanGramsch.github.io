---
layout: page
title: About me
permalink: /about/
weight: 1
---
<!--html is a vast sea of code
press ctrl + shift + z to comment
 -->
<p style="text-align: justify">
<span style="background-color: #4485b8; color: #fff; display: inline-block; padding: 2px 8px; font-weight: bold; border-radius: 5px;"> <font size="+2">
Welcome,
</font></span><br>
<font size="+1">
I am Tristán, a data scientist.
Meaning that I both do machine learning and data architecture development.
This is what I know most about.
<br>
I am also into health economics.
I know plenty about the overdose epidemic that currently affects the US.
And I have written plenty about social ties among drug users.
<br>
Feel free to explore the content of this webpage.
It is designed to share the things I find interesting.
To show what I find beautiful.
</font>
</p>

<div class="row">
{% include about/skills.html title="Machine learning" source=site.data.programming-skills %}
{% include about/skills.html title="Architecture development" source=site.data.management-skills %}
</div>

# <span style="text-decoration: underline"> My timeline </span>
<div class="row">
{% include about/timeline.html %}
</div>
