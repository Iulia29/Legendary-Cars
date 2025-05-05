<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Legendary Cars</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&family=Staatliches&family=Open+Sans&display=swap" rel="stylesheet">
  <style>
    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      font-family: 'Orbitron', sans-serif;
      background: linear-gradient(#110022, #220033);
      background-image: url('https://thumbs.dreamstime.com/b/d-render-abstract-background-glowing-lines-neon-lights-laser-show-stage-design-virtual-reality-environment-zigzag-rays-ultraviolet-141906293.jpg');
      background-size: cover;
      background-attachment: fixed;
      color: #fff;
      text-align: center;
    }

    .fade-in {
      opacity: 0;
      transform: translateY(20px);
      animation: fadeInUp 1s ease forwards;
    }

    .fade-in.delay-1 { animation-delay: 0.3s; }
    .fade-in.delay-2 { animation-delay: 0.6s; }
    .fade-in.delay-3 { animation-delay: 0.9s; }

    @keyframes fadeInUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    header {
      padding: 2em 1em 1em;
    }

    h1 {
      font-family: 'Staatliches', cursive;
      font-size: 4em;
      color: #ff00ff;
      text-shadow: 2px 2px 0 #000, 4px 4px 0 #6600cc, 0 0 25px #cc00ff;
      letter-spacing: 5px;
      text-transform: uppercase;
      margin-bottom: 0.3em;
    }

    p.subtitle {
      font-family: 'Open Sans', sans-serif;
      font-size: 1.3em;
      color: #00ffff;
      margin-top: 0;
    }

    nav {
      display: flex;
      justify-content: center;
      gap: 1em;
      flex-wrap: wrap;
      margin: 1.5em 0;
    }

    .nav-tab {
      padding: 0.7em 2em;
      background: #220044cc;
      border: 1px solid #ff00ff;
      border-radius: 30px;
      color: white;
      font-size: 1em;
      cursor: pointer;
      text-transform: uppercase;
      text-decoration: none;
      transition: 0.3s ease;
    }

    .nav-tab:hover {
      background: #ff00ff33;
      box-shadow: 0 0 10px #ff00ff;
    }

    h2 {
      font-size: 2.5em;
      color: #ff00ff;
      margin-top: 1em;
    }

    .car-images {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 2em;
      padding: 2em 1em;
    }

    .car {
      background-color: #110022cc;
      border: 2px solid #00ffff;
      padding: 1em;
      border-radius: 10px;
      width: 200px;
      animation: fadeInUp 1s ease forwards;
    }

    .car img {
      width: 100%;
      border-radius: 10px;
    }

    .car figcaption {
      margin-top: 0.5em;
      font-size: 1em;
      color: #fff;
      font-family: 'Open Sans', sans-serif;
    }

    .history {
      background: #330066cc;
      padding: 2em;
      border-radius: 10px;
      max-width: 600px;
      margin: 2em auto;
      font-family: 'Open Sans', sans-serif;
      animation: fadeInUp 1s ease forwards;
    }

    .history h3 {
      color: #00ffff;
      font-size: 1.5em;
    }

    .timeline {
      list-style: none;
      padding: 0;
      margin-top: 1em;
      font-size: 1em;
    }

    .timeline li {
      margin: 0.5em 0;
    }

    .newsletter {
      background-color: #220044cc;
      padding: 2em;
      color: #ff00ff;
      font-size: 1.5em;
      margin-top: 3em;
      font-family: 'Open Sans', sans-serif;
      animation: fadeInUp 1s ease forwards;
    }

    .contact-form {
      background: #1a0033cc;
      margin: 2em auto;
      padding: 2em;
      max-width: 600px;
      border-radius: 10px;
      animation: fadeInUp 1s ease forwards;
    }

    .contact-form input, .contact-form textarea {
      width: 100%;
      padding: 0.5em;
      margin: 0.5em 0;
      border: none;
      border-radius: 5px;
    }

    .contact-form button {
      padding: 0.7em 2em;
      background: #ff00ff;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    .light-theme {
      background: #f0f0f0;
      color: #000;
    }

    .light-theme .nav-tab {
      background: #fff;
      color: #000;
      border-color: #6600cc;
    }

    .light-theme .nav-tab:hover {
      background: #e0e0e0;
      box-shadow: 0 0 10px #6600cc;
    }

    .light-theme .car {
      background-color: #fff;
      border-color: #6600cc;
      color: #000;
    }

    .light-theme .car figcaption {
      color: #333;
    }

    .light-theme .history {
      background-color: #fff;
      color: #000;
    }

    .light-theme .newsletter {
      background-color: #ddd;
      color: #000;
    }

    .light-theme .contact-form {
      background-color: #fff;
      color: #000;
    }

    .light-theme footer {
      background-color: #ccc !important;
      color: #000 !important;
    }

    .light-theme footer a {
      color: #000;
    }

    footer a {
      color: #ccc;
      text-decoration: underline;
    }

    @media (max-width: 768px) {
      .car-images {
        flex-direction: column;
        align-items: center;
      }

      .car {
        width: 90%;
      }

      .contact-form, .history {
        width: 90%;
        padding: 1em;
      }

      nav {
        flex-direction: column;
        gap: 0.5em;
      }

      h1 {
        font-size: 2.5em;
      }

      h2 {
        font-size: 1.8em;
      }

      .newsletter {
        font-size: 1.2em;
      }
    }
  </style>
  <script>
    const translations = {
      en: {
        title: "Legendary Cars",
        subtitle: "Welcome to the world of classic automobiles!",
        gallery: "Gallery",
        contact: "Contact",
        newsletter: "SUBSCRIBE TO OUR NEWSLETTER",
      },
      ro: {
        title: "Mașini Legendare",
        subtitle: "Bun venit în lumea automobilelor clasice!",
        gallery: "Galerie",
        contact: "Contact",
        newsletter: "ABONEAZĂ-TE LA NEWSLETTER",
      }
    };

    let currentLang = 'en';

    function toggleLanguage() {
      currentLang = currentLang === 'en' ? 'ro' : 'en';
      const t = translations[currentLang];
      document.getElementById('title').textContent = t.title;
      document.getElementById('subtitle').textContent = t.subtitle;
      document.getElementById('nav-gallery').textContent = t.gallery;
      document.getElementById('nav-contact').textContent = t.contact;
      document.getElementById('newsletter').textContent = t.newsletter;
    }

    function validateForm(e) {
      const name = document.getElementById("name").value.trim();
      const email = document.getElementById("email").value.trim();
      const message = document.getElementById("message").value.trim();
      if (!name || !email || !message) {
        alert("Please fill in all fields.");
        e.preventDefault();
      } else if (!/^[^@\s]+@[^@\s]+\.[^@\s]+$/.test(email)) {
        alert("Please enter a valid email address.");
        e.preventDefault();
      }
    }

    function submitForm(e) {
      e.preventDefault();
      const name = document.getElementById("name").value.trim();
      const email = document.getElementById("email").value.trim();
      const message = document.getElementById("message").value.trim();
      const status = document.getElementById("form-status");

      if (!name || !email || !message) {
        alert("Please fill in all fields.");
        return;
      }

      if (!/^[^@\s]+@[^@\s]+\.[^@\s]+$/.test(email)) {
        alert("Please enter a valid email address.");
        return;
      }

      status.style.display = "block";
      status.textContent = "Thanks for your message!";
      e.target.reset();
    }
  </script>
</head>
<body>
  <header class="fade-in">
    <h1 id="title">Legendary Cars</h1>
    <p id="subtitle" class="subtitle">Welcome to the world of classic automobiles!</p>
  </header>

  <nav class="fade-in delay-1">
    <a class="nav-tab" id="nav-gallery" href="#gallery">Gallery</a>
    <a class="nav-tab" id="nav-contact" href="#contact">Contact</a>
    <a class="nav-tab" href="#" onclick="toggleLanguage()">EN / RO</a>
    <button onclick="document.body.classList.toggle('light-theme')" class="nav-tab">Toggle Theme</button>
  </nav>

  <section id="gallery" class="fade-in delay-2">
    <h2>Image Gallery</h2>
    <div class="car-images">
      <figure class="car">
        <img src="https://thumbs.dreamstime.com/b/rusty-old-classic-cars-22537899.jpg" alt="Rusty Classic Cars">
        <figcaption>Rusty Classic Cars</figcaption>
      </figure>
      <figure class="car">
        <img src="https://thumbs.dreamstime.com/b/colorful-havana-cars-panorama-11097762.jpg" alt="Colorful Havana Cars">
        <figcaption>Havana Panorama</figcaption>
      </figure>
      <figure class="car">
        <img src="https://thumbs.dreamstime.com/b/full-size-pickup-truck-ford-f-ford-bonus-built-berlin-oldtimer-day-54657618.jpg" alt="Ford Bonus Built Pickup">
        <figcaption>Ford Bonus Built</figcaption>
      </figure>
    </div>
  </section>

  <section class="history fade-in delay-2">
    <h3>AUTO HISTORY — LEGENDARY MODELS</h3>
    <p>A symbol of 1950s American luxury and a design that inspired generations.</p>
    <ul class="timeline">
      <li><strong>1955</strong> – Chevrolet Bel Air</li>
      <li><strong>1967</strong> – Ford Mustang</li>
      <li><strong>1982</strong> – Ferrari GTO</li>
      <li><strong>1990</strong> – Best Sports Car: Mazda MX-5</li>
    </ul>
  </section>

  <section id="contact" class="contact-form fade-in delay-3">
    <h2>Contact Us</h2>
    <form onsubmit="submitForm(event)">
      <input type="text" id="name" placeholder="Your Name" required>
      <input type="email" id="email" placeholder="Your Email" required>
      <textarea rows="4" id="message" placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
      <p id="form-status" style="color: lightgreen; margin-top: 1em; display: none;">Thanks for your message!</p>
    </form>
  </section>

  <section class="newsletter fade-in delay-3">
    <p id="newsletter">SUBSCRIBE TO OUR NEWSLETTER</p>
  </section>

  <footer class="fade-in delay-3" style="background-color:#110022; padding: 1em; color: #888; font-size: 0.9em;">
    &copy; 2025 Legendary Cars. All rights reserved. |
    <a href="#">Terms & Conditions</a> | <a href="#">Privacy Policy</a>
  </footer>
</body>
</html>

