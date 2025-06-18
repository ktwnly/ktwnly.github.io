---
layout: default
permalink: /
title: Home
---

<section id="hero" class="section" style="text-align: center; padding-top: 100px;">
  <div class="container">
    <img id="fade-in-image" src="https://i.imgur.com/uyDNQnn.jpg" alt="Katie Townley" style="max-width: 200px; border-radius: 50%; opacity: 0; transition: opacity 2s ease;">
    <h1 class="title mt-4">Hi, I'm Katie Townley</h1>
    <p class="subtitle">Web Designer & Developer</p>
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

<section id="home" class="section">
  <div class="container">
    <h1 class="title">Hi, I'm Katie Townley</h1>
    <p class="subtitle">Web Designer & Developer</p>
    <p>
      <a class="button" href="#about">About Me</a>
      <a class="button" href="#projects">Projects</a>
      <a class="button" href="#contact">Contact</a>
    </p>
  </div>
</section>

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
