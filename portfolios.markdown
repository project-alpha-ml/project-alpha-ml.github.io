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
  <div class="iframe-spacer"></div>
  <iframe title="PAE Portfolio Transactions" aria-label="Table" id="datawrapper-chart-7M70j" src="https://datawrapper.dwcdn.net/7M70j" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="600" data-external="1">
  </iframe>
</div>

<div id="Portfolio2" class="tabcontent" style="display:none;">
  <iframe title="PAE.CORE Portfolio Holdings" aria-label="Table" id="datawrapper-chart-zN5VG" src="https://datawrapper.dwcdn.net/zN5VG" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="300" data-external="1">
  </iframe>
  <div class="iframe-spacer"></div>
  <iframe title="PAE.CORE Portfolio Transactions" aria-label="Table" id="datawrapper-chart-1PrqF" src="https://datawrapper.dwcdn.net/1PrqF" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="600" data-external="1">
  </iframe>
</div>

<div id="Portfolio3" class="tabcontent" style="display:none;">
  <iframe title="PAE.ROTA Portfolio Holdings" aria-label="Table" id="datawrapper-chart-lysIw" src="https://datawrapper.dwcdn.net/lysIw" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="300" data-external="1">
  </iframe>
  <div class="iframe-spacer"></div>
  <iframe title="PAE.ROTA Portfolio Transactions" aria-label="Table" id="datawrapper-chart-b3tbw" src="https://datawrapper.dwcdn.net/b3tbw" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="600" data-external="1">
  </iframe>
</div>

<script type="text/javascript">
!function() {
    "use strict";
    window.addEventListener("message", function(a) {
        if (void 0 !== a.data["datawrapper-height"]) {
            var e = document.querySelectorAll("iframe");
            for (var t in a.data["datawrapper-height"]) {
                for (var r = 0; r < e.length; r++) {
                    if (e[r].contentWindow === a.source) {
                        var i = a.data["datawrapper-height"][t] + "px";
                        e[r].style.height = i;
                    }
                }
            }
        }
    });
}();

// DOMContentLoaded event to handle tab functionality after the document is fully loaded
document.addEventListener("DOMContentLoaded", function() {
    // Retrieve the stored selected tab if it exists
    var selectedTab = localStorage.getItem('selectedPortfolio');

    // Open the stored tab or default to the first tab
    if (selectedTab) {
        openTable(null, selectedTab);
    } else {
        openTable(null, 'Portfolio1');
    }

    // Set the active button based on selected or default tab
    var activeBtnId = selectedTab ? selectedTab + "Btn" : "Portfolio1Btn";
    document.getElementById(activeBtnId).classList.add("active");
});

// Function to manage opening of tabs and setting active class on buttons
function openTable(evt, portfolioName) {
    var buttonlinks = document.getElementsByClassName("buttonlinks");
    var tabcontent = document.getElementsByClassName("tabcontent");

    // Hide all tab contents initially
    for (var i = 0; i < tabcontent.length; i++) {
        tabcontent[i].style.display = "none";
    }

    // Remove 'active' class from all button links
    for (var i = 0; i < buttonlinks.length; i++) {
        buttonlinks[i].className = buttonlinks[i].className.replace(" active", "");
    }
    
    // Display the selected tab content and add 'active' class to the corresponding button
    document.getElementById(portfolioName).style.display = "block";
    if (evt) {
        evt.currentTarget.className += " active";
        // Store the selected tab
        localStorage.setItem('selectedPortfolio', portfolioName);
    } else {
        // Handle default active state without an event
        document.getElementById(portfolioName + 'Btn').className += " active";
    }
}
</script>
