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

const handleComment = (e)=>{
  e.preventDefault();
  const newDiv = document.createElement("div");
  
  newDiv.innerText = e.target.comments.value;
  const comments = document.getElementById("comments")
  comments.append(newDiv)
}

const form = document.getElementById("commentForm")
form.addEventListener("submit", handleComment, true);
<div id="comments"></div>
<div class="commentform">
             <h1>Leave your comment!</h1>
             <br>
             <br>
             <form id="commentForm" class="commentform" >
                 <p>Nickname or Name</p> <input id="name" required="required" type="text">
                 <br>
                 <p>Comments: </p><textarea id="comment" name="comments" rows="8" cols="20"></textarea>
                 <button type="submit" name="commentsubmit">Comment!</button>
            </form>
</div>
