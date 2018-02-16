---
title: "Scarcity"
permalink: /concepts/scarcity.html
header:
  teaser: http://placehold.it/600x400
---

## What is Scarcity?
Scarcity is the principle that limited amounts of goods and services are available to meet unlimited wants.

## Video

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/mRSBjFkbH0I?rel=0&showinfo=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Question

### Question Test

<form class="form">
  <div><div class="radio-container"><input class="radio" type="radio" name="choice" value="0"></div> Test 1</div>
  <div><div class="radio-container"><input class="radio" type="radio" name="choice" value="1"></div> Test 2</div>
  <div><div class="radio-container"><input class="radio" type="radio" name="choice" value="2"></div> Test 3</div>
  <div><div class="radio-container"><input class="radio" type="radio" name="choice" value="3"></div> Test 4</div>
</form>

<button class="btn btn--info" id="btn" type="button" onclick="submitAnswer()">Submit</button>
<p id="message"></p>

<script>
function submitAnswer() {
  var radios = document.getElementsByName("choice");
  var len = radios.length;
  var checked = false;
  var userAnswer;
  var msg = document.getElementById("message");
  var btn = document.getElementById("btn");
  
  for(i = 0; i < len; i++) {
     if(radios[i].checked) {
       checked = true;
       userAnswer = radios[i].value;
     }
  } 
  if(!checked) {
    msg.className = "notice--info";
    btn.createAttribute("disabled");
    msg.innerHTML = "Please select an answer.";
  }
  else if(userAnswer === "1") {
    msg.className = "notice--success";
    btn.createAttribute("disabled");
    msg.innerHTML = "Correct!";
  }
  else {
    msg.className = "notice--danger";
    btn.createAttribute("disabled");
    msg.innerHTML = "Incorrect.";
  }
  setTimeout(function() {
    msg.innerHTML = "";
    msg.className = "";
    btn.removeAttribute("disabled");
  }, 3000 );
}
</script>
