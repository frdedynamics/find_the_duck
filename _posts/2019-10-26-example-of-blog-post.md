---
layout: post
title:  "Post example"
date:   2019-10-26 10:00:40
blurb: "A look at an example post using Bay Jekyll theme."
og_image: /assets/img/content/post-example/Banner.jpg
---

<img src="{{ "/assets/img/content/post-example/Banner.jpg" | absolute_url }}" alt="bay" class="post-pic"/>
<br />
<br />


<div class="container">
  <h1>User Input Page</h1>
  <div id="user-input"></div>

  <form id="user-form">
    <input type="text" id="user-text" placeholder="Enter text">
    <button type="submit">Submit</button>
  </form>
</div>

<script>
  // JavaScript code for handling user input and rendering it on the page
  const form = document.getElementById('user-form');
  const userInput = document.getElementById('user-text');
  const userInputDiv = document.getElementById('user-input');

  form.addEventListener('submit', function(e) {
    e.preventDefault();
    const inputValue = userInput.value;
    userInput.value = '';
    appendToUserInput(inputValue);
  });

  function appendToUserInput(text) {
    const newParagraph = document.createElement('p');
    newParagraph.textContent = text;
    userInputDiv.appendChild(newParagraph);
  }
</script>
