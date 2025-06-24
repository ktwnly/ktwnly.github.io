---
layout: default
permalink: /
title: Home
---

<section id="hero" class="section">
  <div class="container">
    <div class="columns is-vcentered is-variable is-6 is-multiline">

    <!-- Image Column -->
      <div class="column is-full-mobile is-4-tablet is-4-desktop has-text-centered" 
           style="display: flex; justify-content: center; align-items: center;">
        <img id="fade-in-image" 
             src="/assets/images/website image.png" 
             alt="Katie Townley"
             style="max-width: 100%; height: auto; border-radius: 50%; opacity: 0; transition: opacity 2s ease;">
      </div>

      <!-- Text Column -->
      <div class="column is-full-mobile is-8-tablet is-8-desktop has-text-centered has-text-left-desktop">
        <h1 class="title is-2">Hello, I'm Katie Townley!</h1>
        <p class="subtitle is-4">Web Designer & Developer</p>

        <div class="buttons mt-4 is-justify-content-center is-justify-content-flex-start-desktop is-flex">
          <a class="button is-white is-light" href="https://www.linkedin.com/in/katie-townley/" target="_blank" style="color:#db6766;">
            <i class="fab fa-linkedin fa-3x"></i>
          </a>

          <a class="button is-white is-light" href="https://github.com/ktwnly" target="_blank" style="color:#db6766;">
            <i class="fab fa-github fa-3x"></i>
          </a>

          <a class="button is-white is-light" href="mailto:ktnoles@1791.com" style="color:#db6766;">
            <i class="fas fa-envelope fa-3x"></i>
          </a>
          
        </div>
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

<section id="about" class="section">
  <div class="container">
    <h2>About Me</h2>
    <p>Write a short, warm bio here — who you are, what you do, and what you love creating.</p>
  </div>
</section>

<section id="projects" class="section">
  <div class="container">
    <h2>Projects</h2>
    {% for project in site.projects %}
      <div class="box">
        <h3>{{ project.title }}</h3>
        <p>{{ project.description }}</p>
        <a href="{{ project.external_url }}" target="_blank">View Project</a>
      </div>
    {% endfor %}
  </div>
</section>

<section id="contact" class="section">
  <div class="container">
    <h2>Contact</h2>
    <p>Email me at <a href="mailto:ktnoles@1791.com">ktnoles@1791.com</a></p>
    <!-- Optionally add social icons or a contact form -->
  </div>
</section>


{% include landing.html %}
