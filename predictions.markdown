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
  <iframe title="Stocks Expected to Gain +4.0% or More" aria-label="Table" id="datawrapper-chart-Hx7ah" src="https://datawrapper.dwcdn.net/Hx7ah" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="300" data-external="1">
  </iframe>
  <script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"]){var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}}}))}();
  </script>
</div>

<div id="Prediction2" class="tabcontent" style="display:none;">
  <iframe title="Stocks Expected to Pull Back -1.5% or More" aria-label="Table" id="datawrapper-chart-mXOqs" src="https://datawrapper.dwcdn.net/mXOqs" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="300" data-external="1">
  </iframe>
  <script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"]){var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}}}))}();
  </script>
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
