# Introduction

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/gitalk@1/dist/gitalk.css">
<script src="https://cdn.jsdelivr.net/npm/gitalk@1/dist/gitalk.min.js"></script>
<div id="gitalk-container"></div>
var gitalk = new Gitalk({
  "clientID": "3f62415a283d19cbd696",
  "clientSecret": "aed0e1db0620bf5d0e3a3f0225f801997ad74e58",
  "repo": "snowdreams1006.github.io",
  "owner": "snowdreams1006",
  "admin": ["snowdreams1006"],
  "id": location.pathname,      
  "distractionFreeMode": false  
});
gitalk.render("gitalk-container");
