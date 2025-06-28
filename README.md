<!DOCTYPE html>
<html lang="en">
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
    }

    section {
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
    </div>

    <section style="animation-delay: 0.1s;">
      <h2>About Me</h2>
      <div class="card">
        <p>Hello! I'm Asghar Ali, a dedicated and detail-oriented Junior Scientific Assistant currently working in the Chemical Testing Lab at Saindak. I specialize in sulfur analysis, volumetric testing, and lab documentation. With a strong foundation in science and practical lab safety, I take pride in precise work and continuous learning. Outside the lab, I enjoy technology, teaching, and working on creative personal projects.</p>
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
        </ul>
      </div>
    </section>

    <section style="animation-delay: 0.4s;">
      <h2>Skills</h2>
      <div class="card">
        <ul>
          <li>Chemical Testing and Volumetric Analysis</li>
          <li>Sulfur Analysis using Compensation Method</li>
          <li>Lab Safety and Report Management</li>
          <li>Teaching and Scientific Communication</li>
        </ul>
      </div>
    </section>

    <section style="animation-delay: 0.5s;">
      <h2>Contact</h2>
      <div class="card">
        <p>Email: <a href="mailto:asgharsanjarani318@gmail.com">asgharsanjarani318@gmail.com</a></p>
        <a href="mailto:asgharsanjarani318@gmail.com" class="contact-btn">Get in Touch</a>
      </div>
    </section>
  </div>
</body>
</html>
