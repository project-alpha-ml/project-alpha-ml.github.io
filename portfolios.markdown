---
layout: default
title: Portfolios
permalink: /portfolios/
---

<div class="tabs">
  <button id="Portfolio1Btn" class="buttonlinks" onclick="openTable(event, 'Portfolio1')">PAE Portfolio</button>
  <button id="Portfolio2Btn" class="buttonlinks" onclick="openTable(event, 'Portfolio2')">PAE.CORE Portfolio</button>
  <button id="Portfolio3Btn" class="buttonlinks" onclick="openTable(event, 'Portfolio3')">PAE.ROTA Portfolio</button>
</div>

<div id="Portfolio1" class="tabcontent">
  <iframe title="PAE Portfolio Holdings" aria-label="Table" id="datawrapper-chart-bFCvw" src="https://datawrapper.dwcdn.net/bFCvw" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="300" data-external="1">
  </iframe>
  <script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"]){var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}}}))}();
  </script>
</div>

<div id="Portfolio2" class="tabcontent" style="display:none;">
  <iframe title="PAE.CORE Portfolio Holdings" aria-label="Table" id="datawrapper-chart-zN5VG" src="https://datawrapper.dwcdn.net/zN5VG" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="300" data-external="1">
  </iframe>
  <script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"]){var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}}}))}();
  </script>
</div>

<div id="Portfolio3" class="tabcontent" style="display:none;">
  <iframe title="PAE.ROTA Portfolio Holdings" aria-label="Table" id="datawrapper-chart-lysIw" src="https://datawrapper.dwcdn.net/lysIw" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="300" data-external="1">
  </iframe>
  <script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"]){var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}}}))}();
  </script>
</div>

<script>
document.addEventListener("DOMContentLoaded", function() {
  // Check if a previously selected tab is stored
  var selectedTab = localStorage.getItem('selectedPortfolio');
  
  // If there's a stored selection, open that tab
  if (selectedTab) {
    openTable(null, selectedTab);
  } else {
    // Default to the first tab
    openTable(null, 'Portfolio1');
  }
  
  var activeBtnId = selectedTab ? selectedTab + "Btn" : "Portfolio1Btn";
  document.getElementById(activeBtnId).classList.add("active");
});

function openTable(evt, portfolioName) {
  var i, tabcontent, buttonlinks;
  tabcontent = document.getElementsByClassName("tabcontent");
  for (i = 0; i < tabcontent.length; i++) {
    tabcontent[i].style.display = "none";
  }
  buttonlinks = document.getElementsByClassName("buttonlinks");
  for (i = 0; i < buttonlinks.length; i++) {
    buttonlinks[i].className = buttonlinks[i].className.replace(" active", "");
  }
  document.getElementById(portfolioName).style.display = "block";
  
  if (evt) {
    evt.currentTarget.className += " active";
    // Store the selected tab
    localStorage.setItem('selectedPortfolio', portfolioName);
  } else {
    // This handles the default active state without an event
    document.getElementById(portfolioName + 'Btn').className += " active";
  }
}
</script>
