---
layout: archive
title: "News"
permalink: /news/
author_profile: true

---

<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
.collapsible {
  background-color: #777;
  color: white;
  cursor: pointer;
  padding: 18px;
  width: 100%;
  border: none;
  text-align: left;
  outline: none;
  font-size: 15px;
}

.active, .collapsible:hover {
  background-color: #555;
}

.collapsible:after {
  content: '\002B';
  color: white;
  font-weight: bold;
  float: right;
  margin-left: 5px;
}

.active:after {
  content: "\2212";
}

.content {
  padding: 0 18px;
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.2s ease-out;
  background-color: #f1f1f1;
}
</style>
</head>
<body>

<h2>Animated Collapsibles</h2>

---

<p>A Collapsible:</p>
<button class="collapsible">2021/Apr/1 New paper!</button>
<div class="content">
  <p>Our first paper was published in The Journal of Clinical Investigation as a collaboration with The University of Michigan. </p>
  <p>Dr. Yoshida is the 1st co-first author and a co-corresponding author. Two undergraduates, Wenyue Zheng, and Rui Hua contribute this as co-authors.</p>
  <p>This paper was highlighted as the cover article. For more information, please see the Publication page. </p>
</div>

---

<p>A Collapsible:</p>
<button class="collapsible">2021/Apr/1 New paper!</button>
<div class="content">
  <p>Our first paper was published in The Journal of Clinical Investigation as a collaboration with The University of Michigan. </p>
  <p>Dr. Yoshida is the 1st co-first author and a co-corresponding author. Two undergraduates, Wenyue Zheng, and Rui Hua contribute this as co-authors.</p>
  <p>This paper was highlighted as the cover article. For more information, please see the Publication page. </p>
</div>

---

<p>Collapsible Set:</p>
<button class="collapsible">Open Section 1</button>
<div class="content">
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
</div>
<button class="collapsible">Open Section 2</button>
<div class="content">
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
</div>
<button class="collapsible">Open Section 3</button>
<div class="content">
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
</div>

<script>
var coll = document.getElementsByClassName("collapsible");
var i;

for (i = 0; i < coll.length; i++) {
  coll[i].addEventListener("click", function() {
    this.classList.toggle("active");
    var content = this.nextElementSibling;
    if (content.style.maxHeight){
      content.style.maxHeight = null;
    } else {
      content.style.maxHeight = content.scrollHeight + "px";
    } 
  });
}
</script>
</body>
