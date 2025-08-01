# mohittechmind.
Hi My name is Mohit Paliwal.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>MohitTechMind</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    body {
      background-color: #0e0e0e;
      color: #00ffe0;
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 20px;
      text-align: center;
    }

    h1 {
      font-size: 32px;
      margin-top: 20px;
    }

    #typing {
      font-size: 18px;
      height: 24px;
      margin-bottom: 20px;
    }

    button, .social a {
      background-color: #00ffee;
      color: #000;
      border: none;
      padding: 10px 20px;
      font-size: 16px;
      border-radius: 8px;
      cursor: pointer;
      margin: 10px;
      transition: 0.3s;
      display: inline-block;
      text-decoration: none;
    }

    button:hover, .social a:hover {
      background-color: #00bbaa;
    }

    .social {
      margin-top: 20px;
    }

    form {
      margin-top: 40px;
      max-width: 400px;
      margin-left: auto;
      margin-right: auto;
      text-align: left;
      background: #1a1a1a;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px cyan;
    }

    form label {
      display: block;
      margin: 10px 0 5px;
    }

    form input, form textarea {
      width: 100%;
      padding: 10px;
      margin-bottom: 15px;
      border: none;
      border-radius: 5px;
      font-size: 14px;
    }

    form input:focus, form textarea:focus {
      outline: 2px solid #00ffee;
    }

    footer {
      margin-top: 40px;
      color: gray;
    }
  </style>
</head>
<body>

  <h1>Welcome to MohitTechMind</h1>
  <div id="typing"></div>

  <p>Hello, I'm <strong>Mohit</strong>. Learn with me!</p>

  <!-- Greet Button -->
  <button onclick="sayHi()">Click to Greet</button>

  <!-- Email & Instagram -->
  <div class="social">
    <a href="mailto:paliwalmohit783@gmail.com">📧 Email Me</a>
    <a href="https://instagram.com/mohitpaliwal_369" target="_blank">📷 Instagram</a>
  </div>

  <!-- Contact Form -->
  <form onsubmit="submitForm(event)">
    <h2 style="text-align: center; color: #00ffff;">Contact Me</h2>
    
    <label for="name">Your Name</label>
    <input type="text" id="name" placeholder="Enter your name" required>
    
    <label for="email">Your Email</label>
    <input type="email" id="email" placeholder="Enter your email" required>
    
    <label for="message">Message</label>
    <textarea id="message" rows="5" placeholder="Type your message..." required></textarea>
    
    <button type="submit">Send Message</button>
  </form>

  <footer>
    <p>© 2025 MohitTechMind. All rights reserved.</p>
  </footer>

  <!-- JavaScript Section -->
  <script>
    function sayHi() {
      alert("Hello, welcome to MohitTechMind! 🚀");
    }

    const text = "Exploring Web Development, JavaScript, and AI.";
    let i = 0;
    function typeEffect() {
      if (i < text.length) {
        document.getElementById("typing").innerHTML += text.charAt(i);
        i++;
        setTimeout(typeEffect, 50);
      }
    }
    typeEffect();

    function submitForm(event) {
      event.preventDefault();
      const name = document.getElementById("name").value.trim();
      const email = document.getElementById("email").value.trim();
      const message = document.getElementById("message").value.trim();

      if (name && email && message) {
        alert(`Thank you, ${name}! Your message has been received.`);
        document.querySelector("form").reset();
      } else {
        alert("Please fill out all fields.");
      }
    }
  </script>

</body>
</html>