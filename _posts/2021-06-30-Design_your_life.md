---
title: Design your life
tags: [Philosophy, Project design]
style: fill
color: primary
description: Notes on the book 'Designing your life' by Bill Burnet and Dave Evans.  
---
## A few words on the world one can build

<p style="text-align: justify; text-indent: 30px;">
Here I want to share my thoughts and notes about a book called "Designing Your Life: How to Build a Well-Lived, Joyful Life". As time progresses, I will also add other reflections about how to have an exciting life. A worth living life if you will. I am by no means an expert. Not a designer. Not a monk. But I do think that I have a pretty awesome life. And I want to share what I know with others. Hopefully help them get more awesome lives.
</p>

<p style="text-align: justify; text-indent: 30px;">
Here we start the journey of designing your life. It is possible. Actually, is not even that hard. And it might give you a boost. Wherever you are going.
</p>

<!-- Include notes of all chapters  -->
<details>
  <summary> Chapter 1. Start where you are </summary>
<div w3-include-html = "\assets\documents\design_your_life_notes\Chapter 1. Start where you are.html"></div>
</details>

<details>
  <summary> Chapter 2. Building a compass </summary>
<div w3-include-html = "\assets\documents\design_your_life_notes\Chapter 2. Building a compass.html"></div>
</details>

<details>
  <summary> Chapter 3. Wayfinding </summary>
<div w3-include-html = "\assets\documents\design_your_life_notes\Chapter 3. Wayfinding.html"></div>
</details>

<details>
  <summary> Chapter 4. Getting unstuck </summary>
<div w3-include-html = "\assets\documents\design_your_life_notes\Chapter 4. Getting unstuck.html"></div>
</details>

<details>
  <summary> Chapter 5. Design your lives </summary>
<div w3-include-html = "\assets\documents\design_your_life_notes\Chapter 5. Design your lives.html"></div>
</details>

<details>
  <summary> Chapter 6. Prototyping </summary>
<div w3-include-html = "\assets\documents\design_your_life_notes\Chapter 6. Prototyping.html"></div>
</details>

<details>
  <summary> Chapter 7. How not to get a job </summary>
<div w3-include-html = "\assets\documents\design_your_life_notes\Chapter 7. How to not get a job.html"></div>
</details>

<details>
  <summary> Chapter 8. Designing your dream job </summary>
<div w3-include-html = "\assets\documents\design_your_life_notes\Chapter 8. Designing your dream job.html"></div>
</details>

<details>
  <summary> Chapter 9. Choosing happiness </summary>
<div w3-include-html = "\assets\documents\design_your_life_notes\Chapter 9. Choosing happiness.html"></div>
</details>

<details>
  <summary> Chapter 10. Failure immunity </summary>
<div w3-include-html = "\assets\documents\design_your_life_notes\Chapter 10. Failure immunity.html"></div>
</details>

<details>
  <summary> Chapter 11. Building a team </summary>
<div w3-include-html = "\assets\documents\design_your_life_notes\Chapter 11. Building a team.html"></div>
</details>

<details>
  <summary> Conclusion: a well-designed life </summary>
<div w3-include-html = "\assets\documents\design_your_life_notes\Conclusion a well designed life.html"></div>
</details>

<!---
Define w3-include- html function.
Include function in the script.
This code is needed to render .html files in the script.
--->
<script>
function includeHTML() {
  var z, i, elmnt, file, xhttp;
  /* Loop through a collection of all HTML elements: */
  z = document.getElementsByTagName("*");
  for (i = 0; i < z.length; i++) {
    elmnt = z[i];
    /*search for elements with a certain atrribute:*/
    file = elmnt.getAttribute("w3-include-html");
    if (file) {
      /* Make an HTTP request using the attribute value as the file name: */
      xhttp = new XMLHttpRequest();
      xhttp.onreadystatechange = function() {
        if (this.readyState == 4) {
          if (this.status == 200) {elmnt.innerHTML = this.responseText;}
          if (this.status == 404) {elmnt.innerHTML = "Page not found.";}
          /* Remove the attribute, and call this function once more: */
          elmnt.removeAttribute("w3-include-html");
          includeHTML();
        }
      }
      xhttp.open("GET", file, true);
      xhttp.send();
      /* Exit the function: */
      return;
    }
  }
}
</script>

<script>
includeHTML();
</script>
