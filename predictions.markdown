---
layout: default
title: Predictions
permalink: /predictions/
---

<div class="tabs">
  <button id="Prediction1Btn" class="buttonlinks" onclick="openTable(event, 'Prediction1')">Stocks Expected to Gain</button>
  <button id="Prediction2Btn" class="buttonlinks" onclick="openTable(event, 'Prediction2')">Stocks Expected to Pull Back</button>
</div>

<div id="Prediction1" class="tabcontent">
  <iframe title="Stocks Expected to Gain +4.0% or More" aria-label="Table" src="https://datawrapper.dwcdn.net/Hx7ah" scrolling="yes" frameborder="0" style="width: 100%; border: none;" height="750"></iframe>
</div>

<div id="Prediction2" class="tabcontent" style="display:none;">
  <iframe title="Stocks Expected to Pull Back -1.5% or More" aria-label="Table" src="https://datawrapper.dwcdn.net/mXOqs" scrolling="yes" frameborder="0" style="width: 100%; border: none;" height="750"></iframe>
</div>

<script>
document.addEventListener("DOMContentLoaded", function() {
  // Check if a previously selected tab is stored
  var selectedTab = localStorage.getItem('selectedTab');
  
  // If there's a stored selection, open that tab, otherwise default to the first tab
  if (selectedTab) {
    openTable(null, selectedTab);
    document.getElementById(selectedTab + "Btn").classList.add("active");
  } else {
    // Default to the first tab
    openTable(null, 'Prediction1');
    document.getElementById("Prediction1Btn").classList.add("active");
  }
});

function openTable(evt, predictionName) {
  var i, tabcontent, buttonlinks;
  tabcontent = document.getElementsByClassName("tabcontent");
  for (i = 0; i < tabcontent.length; i++) {
    tabcontent[i].style.display = "none";
  }
  buttonlinks = document.getElementsByClassName("buttonlinks");
  for (i = 0; i < buttonlinks.length; i++) {
    buttonlinks[i].className = buttonlinks[i].className.replace(" active", "");
  }
  document.getElementById(predictionName).style.display = "block";
  
  if (evt) {
    evt.currentTarget.className += " active";
    // Store the selected tab
    localStorage.setItem('selectedTab', predictionName);
  } else {
    // This handles the default active state without an event
    document.getElementById(predictionName + "Btn").className += " active";
  }
}
</script>
