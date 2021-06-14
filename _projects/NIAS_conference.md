---
name: Argument presented at NIAS Conference on Studies of Belonging
tools: [R]
image: "https://www.drugabuse.gov/sites/default/files/images/Benzodiazepines%20and%20Opioids%202.2.jpg"
description: Major psychiatry textbooks make questionable claims about the nature of drug addiction. It might be contributing to over prescription in the US.  
---
<h2> Here, </h2>

<p style = "text-align: justify"><font size = "+1">
I present the argument I made for the 2021 NIAS Conference on Studies of Belonging. I got accepted with the paper "Psychiatric blindspot: how drug addiction diagnosis miss social network factors".

I argue that 3 major psychiatry textbooks make questionable considerations about the nature of drug addiction.
Psychiatry textbooks suggest that a conflictive relationship with family members make up ground to diagnose addiction.
And there is little evidence or discussion provided.
The psychiatry textbooks are: the Diagnostic and Statistical Manual of Mental Disorders (call it DSM-5); the Oxford Handbook of Psychiatry (call it Oxford); and the American Psychiatric Association Publishing Textbook of Psychiatry (call it APA).

Here is the problem.
Clinical suggestions lead medical professionals to make clinical decisions.
Medical professionals might tend to diagnose addiction to those who have broken families.
An overestimation of what addiction is.
In turn, this can lead to over-prescription. A big problem in the US.
</font> </p>

<h2> The problem of benzodiazepines </h2>

<p style = "text-align: justify"><font size = "+1">
Benzodiazepines are a family of sedatives prescribed by physicians to mitigate the effects of withdrawal.
Benzodiazepines are often prescribed to drug addicts.
As indicated <a href = "https://www.drugabuse.gov/drug-topics/opioids/benzodiazepines-opioids"> here </a> by the National Institute on Drug Abuse, "between 1996 and 2013, the number of adults who filled a benzodiazepine prescription increased by 67%, from 8.1 million to 13.5 million".
As Benzodiazepine prescription rose, overdose death involving Benzodiazepines rose too.   

<img src = "https://www.drugabuse.gov/sites/default/files/images/Benzodiazepines%20and%20Opioids%202.2.jpg">

Next I present some visualizations of overdose data in some states in the US.
These visualizations where made by <a href = "https://www.kaggle.com/khsamaha/fatal-drug-overdose-eda"> Kheirallah Samaha </a> using data from <a href = "https://www.data.gov/"> data.gov </a>. Compiled by <a href = "https://www.kaggle.com/ruchi798/drug-overdose-deaths"> Ruchi Bathia </a>.
This is a 5000 unique values dataset of overdoses in the US. Most deaths were recorded in Connecticut.
I tweaked the visualizations to make them more legible.

</font> </p>

<div w3-include-html = "/assets/documents/projects_documents/NIAS-presentation.html">
</div>

<h2> Conclusion </h2>
<p style = "text-align: justify"><font size = "+1">

Poorly supported claims about drug addiction are common.
The world of mainstream American addiction treatment is highly ritualized.
"Scripting addiction" by professor Carr narrates this phenomena.
We need better regulations for the practice of psychiatrists.

</font> </p>

<!---
Define w3-include- html function.
Include function in the script.
This code is needed to render NIAS-presentation.html above.
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
