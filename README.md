# Introduction

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/gitalk@1/dist/gitalk.css">
<script src="https://cdn.jsdelivr.net/npm/gitalk@1/dist/gitalk.min.js"></script>
<div id="gitalk-container"></div>
var gitalk = new Gitalk({
  "clientID": "941df607ad0d8a39b204",
  "clientSecret": "bd5e6cd6336fcebff410676a7c5d41235030a2f7",
  "repo": "https://github.com/shenshanlaoyuan/InterviewBook",
  "owner": "shenshanlaoyuan",
  "admin": ["shenshanlaoyuan"],
  "id": location.pathname,      
  "distractionFreeMode": false  
});
gitalk.render("gitalk-container");
