---
name: NIAS Conference on Studies of Belonging. 2021.
tools: [R, conference]
image: "https://www.drugabuse.gov/sites/default/files/images/Benzodiazepines%20and%20Opioids%202.2.jpg"
description: Major psychiatry textbooks make questionable claims about the nature of drug addiction. It might be contributing to over prescription in the US.  
---
<h2> Here, </h2>

<font size = "+1">
<p style = "text-align: justify; text-indent: 30px;">
I present the argument I made for the 2021 Waset conference on the Sociology of health and the 2021 NIAS Conference on Studies of Belonging. I got accepted with the paper "Psychiatric blindspot: how drug addiction diagnosis miss social network factors".
</p>

<p style = "text-align: justify; text-indent: 30px;">
I argue that 3 major psychiatry textbooks make questionable considerations about the nature of drug addiction. The psychiatry textbooks I am talking about are: the Diagnostic and Statistical Manual of Mental Disorders (call it DSM-5); the Oxford Handbook of Psychiatry (call it Oxford); and the American Psychiatric Association Publishing Textbook of Psychiatry (call it APA). These psychiatry textbooks suggest that a conflictive relationship with family members make up ground to diagnose addiction. But the suggestion is not thoroughly discussed. And convincing evidence is not provided. Clinicians read these psychiatry textbooks. Some medical certifications even require clinicians to study these psychiatry textbooks. Clinicians then make clinical decisions. They can diagnose drug addiction and prescribe medications to their patients. Medications like benzodiazepines.
</p>

<p style = "text-align: justify; text-indent: 30px;">
Here is the problem. Psychiatry textbooks influence clinicians. Most likely, clinicians trust and follow psychiatry procedures. And thus diagnose addiction to people who have a conflictive relationship with family members. An overestimation of what addiction is. In turn, addiction overestimation can lead to overprescription. A big problem in the US. Clinicians might prescribe addiction medication to those who do not need it. And contribute to the current overdose crisis.
</p>
</font>

<h2> The problem of benzodiazepines </h2>

<font size = "+1">
<p style = "text-align: justify; text-indent: 30px">
As indicated <a href = "https://www.drugabuse.gov/drug-topics/opioids/benzodiazepines-opioids;" style = "text-indent: 0px;"> here </a> by the National Institute on Drug Abuse, "between 1996 and 2013, the number of adults who filled a benzodiazepine prescription increased by 67%, from 8.1 million to 13.5 million".
As Benzodiazepine prescription rose, overdose death involving Benzodiazepines rose too.   
</p>
<img src = "https://www.drugabuse.gov/sites/default/files/images/Benzodiazepines%20and%20Opioids%202.2.jpg">
<p style = "text-align: justify; text-indent: 30px">
Here I present some visualizations of overdose data in some states in the US.
I made these visualizations based on code by <a href = "https://www.kaggle.com/khsamaha/fatal-drug-overdose-eda" style = "text-indent: 0px;"> Kheirallah Samaha </a>. Data comes from <a href = "https://www.data.gov/" style = "text-indent: 0px;"> data.gov </a>. Data was compiled by <a href = "https://www.kaggle.com/ruchi798/drug-overdose-deaths" style = "text-indent: 0px;"> Ruchi Bathia </a>. This is a 5000 unique values dataset of overdoses in the US. Most deaths were recorded in Connecticut.
</p>
</font>

<!-- Include NIAS-presentation.html -->
<div w3-include-html = "/assets/documents/projects_documents/NIAS-presentation.html"></div>

<h2> Thoughts </h2>
<font size = "+1">
<p style = "text-align: justify; text-indent: 30px">
Psychiatry textbooks do not show a full picture of what addiction is. Addiction tends to happen to those who are white, middle age, male, and uneducated. Poor people in despair. Broken families do not cause addiction. Broken families are common among addicts (I would prefer to call them: 'prone to overdose'). Showcasing this information might lead clinicians to prescribe better. And reduce the overprescription crisis. Let's build narratives that people can understand. Trends they can recognize. People might see themselves reflected in larger social trends. They might have better information to make decisions. Have more agency. Discern whether or not to believe what their psychiatrist says. And whether or not to take the drug they give.
</p></font>

<h2> Conclusion </h2>
<font size = "+1">
<p style = "text-align: justify; text-indent: 30px;">
Poorly supported claims about drug addiction are common. "Scripting addiction" by professor Carr narrates this phenomena. The world of mainstream American addiction treatment is highly ritualized. Psychiatry textbooks do not support their addiction claims well. They might contribute to overprescrition. And therefore overdose. We need to better regulate what psychiatrists write about. The well-being US addicts might depend on it.
</p> </font> 

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
