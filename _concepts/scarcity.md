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
  <div><div class="radio-container"><input class="radio" type="radio" name="choice" id="0" value="0"></div><label for="0">Test 1</label></div>
  <div><div class="radio-container"><input class="radio" type="radio" name="choice" id="1" value="1"></div><label for="1">Test 2</label></div>
  <div><div class="radio-container"><input class="radio" type="radio" name="choice" id="2" value="2"></div><label for="2">Test 3</label></div>
  <div><div class="radio-container"><input class="radio" type="radio" name="choice" id="3" value="3"></div><label for="3">Test 4</label></div>
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
  var disabled = document.createAttribute("disabled");
  
  for(i = 0; i < len; i++) {
     if(radios[i].checked) {
       checked = true;
       userAnswer = radios[i].value;
     }
  } 
  if(!checked) {
    msg.className = "notice--info";
    btn.setAttributeNode(disabled);
    msg.innerHTML = "Please select an answer.";
  }
  else if(userAnswer === "1") {
    msg.className = "notice--success";
    btn.setAttributeNode(disabled);
    msg.innerHTML = "Correct!";
  }
  else {
    msg.className = "notice--danger";
    btn.setAttributeNode(disabled);
    msg.innerHTML = "Incorrect.";
  }
  setTimeout(function() {
    msg.innerHTML = "";
    msg.className = "";
    btn.removeAttribute("disabled");
  }, 3000 );
}
</script>
