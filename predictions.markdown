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
</div>

<div id="Prediction2" class="tabcontent" style="display:none;">
  <iframe title="Stocks Expected to Pull Back -1.5% or More" aria-label="Table" id="datawrapper-chart-mXOqs" src="https://datawrapper.dwcdn.net/mXOqs" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="300" data-external="1">
  </iframe>
</div>

<script type="text/javascript">
// Function to handle iframe resizing based on postMessage events
!function() {
    "use strict";
    window.addEventListener("message", function(a) {
        if (void 0 !== a.data["datawrapper-height"]) {
            var iframes = document.querySelectorAll("iframe");
            for (var key in a.data["datawrapper-height"]) {
                for (var i = 0; i < iframes.length; i++) {
                    if (iframes[i].contentWindow === a.source) {
                        var newHeight = a.data["datawrapper-height"][key] + "px";
                        iframes[i].style.height = newHeight;
                    }
                }
            }
        }
    });
}();

// DOMContentLoaded event to handle tab functionality after the document is fully loaded
document.addEventListener("DOMContentLoaded", function() {
    // Retrieve the stored selected tab if it exists
    var selectedTab = localStorage.getItem('selectedTab');
    
    // Open the stored tab or default to the first tab
    if (selectedTab) {
        openTable(null, selectedTab);
    } else {
        openTable(null, 'Prediction1');
    }

    // Set the active button based on selected or default tab
    var activeBtnId = selectedTab ? selectedTab + "Btn" : "Prediction1Btn";
    document.getElementById(activeBtnId).classList.add("active");
});

// Function to manage opening of tabs and setting active class on buttons
function openTable(evt, predictionName) {
    var tabcontent = document.getElementsByClassName("tabcontent");
    var buttonlinks = document.getElementsByClassName("buttonlinks");
    
    // Hide all tab contents initially
    for (var i = 0; i < tabcontent.length; i++) {
        tabcontent[i].style.display = "none";
    }

    // Remove 'active' class from all button links
    for (var i = 0; i < buttonlinks.length; i++) {
        buttonlinks[i].className = buttonlinks[i].className.replace(" active", "");
    }

    // Display the selected tab content and add 'active' class to the corresponding button
    document.getElementById(predictionName).style.display = "block";
    if (evt) {
        evt.currentTarget.className += " active";
        // Store the selected tab
        localStorage.setItem('selectedTab', predictionName);
    } else {
        // Handle default active state without an event
        document.getElementById(predictionName + "Btn").className += " active";
    }
}
</script>
