---
title: "Scarcity"
permalink: /concepts/scarcity.html
header:
  teaser: http://placehold.it/600x400
---

### What is Scarcity?
Scarcity is the principle that limited amounts of goods and services are available to meet unlimited wants.

### Video

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/mRSBjFkbH0I?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

### Question

#### Question Test

<form class="form">
<input class="radio" type="radio" name="choice" value="0"> Test 1

<input class="radio" type="radio" name="choice" value="1"> Test 2

<input class="radio" type="radio" name="choice" value="2"> Test 3

<input class="radio" type="radio" name="choice" value="3"> Test 4
</form>

[Submit](submitAnswer()){: .btn .btn--info}

<script>
function submitAnswer() {
  var radios = document.getElementsByName("choice");
  var i = 0, len = radios.length;
  var checked = false;
  var userAnswer;
  
  for( ; i < len; i++ ) {
     if(radios[i].checked) {
       checked = true;
       userAnswer = radios[i].value;
     }
  } 
  // if user click submit button without selecting any option, alert box should be say "please select choice answer".
  if(!checked) {
    alert("Please select an answer.");
    return;
  }
  // Correct answer
  if(userAnswer === "1") {
     alert("Correct");
  }
  // incorrect answer
  else {
     alert("Incorrect");
  }
  
}
</script>
