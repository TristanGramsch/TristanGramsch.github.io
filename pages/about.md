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
Welcome,
</font>
</span>
</p>

<p style="text-align: justify; text-indent: 30px;">
<font size="+1">
I am a data scientist.
meaning that I do both machine learning and data architecture development,
This is what I know most about.
I am also into health economics.
I know plenty about the overdose epidemic that currently affects the US.
And I have written plenty about social ties among drug users.
Feel free to explore the content of this webpage.
It shows part of my baggage.
</font>
</p>

<p style="text-align: justify; text-indent: 30px;">
<font size="+1">
These are some of the skills I have. If a measure bar is at 100% it means that it is what I know most about compared to myself. Nobody knows everything about these topics. They constantly evolve, change. As they change, I keep exploring them.  
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
