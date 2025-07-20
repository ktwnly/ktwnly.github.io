---
layout: default
permalink: /
title: Home
---

<section id="hero" class="section no-x-padding">
  <div class="container wide">
    <div class="columns is-vcentered is-variable is-6 is-multiline padded-content">

      <!-- Text Column -->
      <div class="column is-full-mobile is-7-tablet is-7-desktop has-text-left">
        <h2 class="title is-1">Hello, I'm <span style="color: #db6766 !important;">Katie Townley</span>!</h2>
        <p class="subtitle is-4">Web Designer & Developer</p>

        <div class="buttons mt-4 is-justify-content-flex-start is-flex">
          <a class="button icon-button" href="https://www.linkedin.com/in/katie-townley/" target="_blank" style="color:#db6766;">
            <i class="fab fa-linkedin fa-3x"></i>
          </a>

          <a class="button icon-button" href="https://github.com/ktwnly" target="_blank" style="color:#db6766;">
            <i class="fab fa-github fa-3x"></i>
          </a>

          <a class="button icon-button" href="mailto:ktnoles@1791.com" style="color:#db6766;">
            <i class="fas fa-envelope fa-3x"></i>
          </a>
          
        </div>

        <br/>

        <p class="subtitle is-4">I'm a college Computer Science student who loves to design and develop coding projects in my free time, learning and absorbing crucial programming skills, as well as new languages, platforms, and frameworks, as I go. I also love creating art, listening to music, experiencing new things, and exploring interesting places! I am always looking to start a new programming project, and I especially enjoy building websites! You can find my resume <a href="https://jekyllrb.com" target="_blank" style="color: #db6766 !important;">here</a>.<br/> <br/> <br/> <strong style="color:#1B3850">Browse through some of my recent work below!</strong></p>


        
      </div>

      <!-- Image Column -->
      <div class="column is-full-mobile is-5-tablet is-5-desktop has-text-centered" 
           style="display: flex; justify-content: center; align-items: center;">
        <img id="fade-in-image" 
             src="/assets/images/website image.png" 
             alt="Katie Townley"
             style="max-width: 100%; height: auto; border-radius: 50%; opacity: 0; transition: opacity 2s ease;">
      </div>

    </div>
  </div>
</section>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    const img = document.getElementById("fade-in-image");
    setTimeout(() => {
      img.style.opacity = 1;
    }, 300); // delay before fade-in starts
  });
</script>


<section id="projects" class="section no-x-padding">
  <div class="container wide">
    <div class="padded-content">
    <h2 class="title is-2">Projects &#10022;</h2>
    {% for project in site.projects %}
      <div class="box">
        <h3>{{ project.title }}</h3>
        <p>{{ project.description }}</p>
        <a href="{{ project.external_url }}" target="_blank">View Project</a>
      </div>
    {% endfor %}
  </div>
  </div>
</section>



<section id="contact" class="section no-x-padding has-text-centered">
  <div class="container wide padded-content">
    <p>Personal Website & Portfolio &#10022; Made with &hearts; using <a href="https://jekyllrb.com" target="_blank">Jekyll</a> &#10022; Hosted on <a href="https://pages.github.com" target="_blank">GitHub Pages</a></p>
    <p>&copy; 2025 Katie Townley. All rights reserved.</p>
  </div>
</section>

