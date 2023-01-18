---
layout: default
title: Home
show_sidebar: true
hero_height: 10
---
<!---
<a href="https://www.flaticon.com/free-icons/science" title="science icons">Science icons created by Good Ware - Flaticon</a>
-->

<link rel="shortcut icon" type="image/x-icon" href="favicon.ico">

This is the homepage.

hi this is ed

<!-- count particles -->
<div class="count-particles">
  <span class="js-count-particles">--</span> particles
</div>

<!-- particles.js container -->
<div id="particles-js"></div>

<!-- scripts -->
<script src="../particles.js"></script>
<script src="js/app.js"></script>

<!-- stats.js -->
<script src="js/lib/stats.js"></script>
<script>
  var count_particles, stats, update;
  stats = new Stats;
  stats.setMode(0);
  stats.domElement.style.position = 'absolute';
  stats.domElement.style.left = '0px';
  stats.domElement.style.top = '0px';
  document.body.appendChild(stats.domElement);
  count_particles = document.querySelector('.js-count-particles');
  update = function() {
    stats.begin();
    stats.end();
    if (window.pJSDom[0].pJS.particles && window.pJSDom[0].pJS.particles.array) {
      count_particles.innerText = window.pJSDom[0].pJS.particles.array.length;
    }
    requestAnimationFrame(update);
  };
  requestAnimationFrame(update);
</script>
