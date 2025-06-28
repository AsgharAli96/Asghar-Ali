<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Asghar Ali - Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet" />
  <style>
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      font-family: 'Roboto', sans-serif;
      background: linear-gradient(135deg, #2b5876, #4e4376);
      color: #fff;
      scroll-behavior: smooth;
    }
    .container {
      max-width: 1000px;
      margin: auto;
      padding: 30px 20px;
    }
    .hero {
      text-align: center;
      padding: 50px 20px;
    }
    .hero img {
      width: 150px;
      height: 150px;
      object-fit: cover;
      border-radius: 50%;
      border: 4px solid #00c3ff;
      margin-bottom: 15px;
    }
    .hero h1 {
      font-size: 2.8rem;
      margin: 10px 0 5px;
      color: #00c3ff;
    }
    .hero p {
      font-size: 1.2rem;
      opacity: 0.9;
    }section {
  margin-top: 50px;
  animation: slide-up 1s ease forwards;
  opacity: 0;
}

@keyframes slide-up {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

h2 {
  border-left: 5px solid #00c3ff;
  padding-left: 10px;
  font-size: 1.8rem;
  margin-bottom: 20px;
}

.card {
  background: rgba(255, 255, 255, 0.05);
  padding: 20px;
  border-radius: 10px;
  margin-bottom: 20px;
  border-left: 4px solid #00c3ff;
}

ul {
  padding-left: 20px;
}

a {
  color: #00c3ff;
  text-decoration: none;
  font-weight: bold;
}

.contact-btn {
  display: inline-block;
  margin-top: 10px;
  padding: 10px 25px;
  background: #00c3ff;
  color: #000;
  border-radius: 25px;
  font-weight: 700;
  letter-spacing: 1px;
  transition: background 0.3s ease;
}

.contact-btn:hover {
  background: #0099cc;
}

@media (max-width: 600px) {
  .hero h1 {
    font-size: 2rem;
  }
  .container {
    padding: 20px 15px;
  }
}

  </style>
</head>
<body>
  <div class="container">
    <div class="hero">
      <img src="profile.jpg" alt="Asghar Ali" />
      <h1>Asghar Ali</h1>
      <p>Junior Scientific Assistant<br />Chemical Testing Lab, Saindak, Chaghi, Balochistan</p>
    </div><section style="animation-delay: 0.1s;">
  <h2>About Me</h2>
  <div class="card">
    <p>I’m Asghar Ali, a detail-oriented Junior Scientific Assistant with hands-on experience in chemical testing, specializing in Sulfur, Copper (Cu), and Gold (Au) analysis. I use both volumetric and instrumental techniques including the GBT method and sulfur analyzer. I strive to ensure accurate, reliable, and efficient testing workflows. I’m currently undergoing ISO/IEC 17025:2017 training to further elevate lab quality and compliance. My background also includes teaching science from 2021 to 2023, which sharpened my communication and leadership skills.</p>
  </div>
</section>

<section style="animation-delay: 0.2s;">
  <h2>Education</h2>
  <div class="card">
    <p><strong>Associate Degree of Science</strong> (2022–2024)<br />University of Balochistan</p>
  </div>
</section>

<section style="animation-delay: 0.3s;">
  <h2>Certifications</h2>
  <div class="card">
    <ul>
      <li>Primary Teaching Certification (1 Year)</li>
      <li>Safety Manager Certification from Saindak</li>
      <li>ISO/IEC 17025:2017 Training (In Progress)</li>
    </ul>
  </div>
</section>

<section style="animation-delay: 0.4s;">
  <h2>Work Experience</h2>
  <div class="card">
    <p><strong>Junior Scientific Assistant</strong><br />Saindak Chemical Testing Lab – Present</p>
    <p><strong>Science Teacher</strong> (2021–2023)<br />Taught general science and chemistry at a private school. Developed practical lessons and simplified complex topics for young learners.</p>
  </div>
</section>

<section style="animation-delay: 0.5s;">
  <h2>Skills</h2>
  <div class="card">
    <ul>
      <li>Sulfur, Copper (Cu), and Gold (Au) Analysis</li>
      <li>GBT Method & Sulfur Analyzer</li>
      <li>Volumetric and Gravimetric Techniques</li>
      <li>Lab Equipment: Burette, Muffle Furnace, Crucibles</li>
      <li>Sample Heating up to 1300°C</li>
      <li>Microsoft Excel & Lab Documentation</li>
      <li>Lab Safety and ISO/IEC 17025:2017 Principles</li>
    </ul>
  </div>
</section>

<section style="animation-delay: 0.6s;">
  <h2>Achievements</h2>
  <div class="card">
    <ul>
      <li>Improved test accuracy in sulfur analysis through better technique optimization</li>
      <li>Contributed to lab quality system by applying ISO/IEC 17025:2017 principles</li>
    </ul>
  </div>
</section>

<section style="animation-delay: 0.7s;">
  <h2>Languages</h2>
  <div class="card">
    <p>Balochi (native), Urdu, English, Pashto, Brahui</p>
  </div>
</section>

<section style="animation-delay: 0.8s;">
  <h2>Hobbies & Interests</h2>
  <div class="card">
    <p>Teaching, drawing, exploring science, and learning new technologies.</p>
  </div>
</section>

<section style="animation-delay: 0.9s;">
  <h2>Contact</h2>
  <div class="card">
    <p>Email: <a href="mailto:asgharsanjarani318@gmail.com">asgharsanjarani318@gmail.com</a></p>
    <a href="mailto:asgharsanjarani318@gmail.com" class="contact-btn">Get in Touch</a>
  </div>
</section>

  </div>
</body>
</html>
