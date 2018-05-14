---
title: "Insurance"
date: 2017-08-22
permalink: /concepts/insurance.html
excerpt: ""
header:
  teaser: /assets/images/insurance.jpg
---

## What is Insurance?
Insurance is protection through a contract from financial losses.

## Question

### Question Test

<form class="form">
  {% comment %}
  The 'radio-container' classes are a workaround for a chrome bug, see https://crbug.com/29427
  {% endcomment %}
  <div><div class="radio-container"><input class="radio" type="radio" name="choice" id="0" value="0"></div> <label for="0">Test 1</label></div>
  <div><div class="radio-container"><input class="radio" type="radio" name="choice" id="1" value="1"></div> <label for="1">Test 2</label></div>
  <div><div class="radio-container"><input class="radio" type="radio" name="choice" id="2" value="2"></div> <label for="2">Test 3</label></div>
  <div><div class="radio-container"><input class="radio" type="radio" name="choice" id="3" value="3"></div> <label for="3">Test 4</label></div>
</form>

<button class="btn btn--info btn--large" id="btn" type="button" onclick="submitAnswer()">Submit</button>
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
