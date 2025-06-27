<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Asghar Ali - Portfolio</title>
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet" />
  <style>
    /* Reset */
    * {
      box-sizing: border-box;
    }
    body {
      font-family: 'Roboto', sans-serif;
      margin: 0;
      padding: 20px;
      background: linear-gradient(135deg, #2980b9, #6dd5fa);
      min-height: 100vh;
      position: relative;
      overflow-x: hidden;
      color: #333;
      line-height: 1.6;
    }
    /* Abstract circles in background */
    body::before, body::after {
      content: "";
      position: absolute;
      border-radius: 50%;
      opacity: 0.15;
      filter: blur(100px);
      z-index: 0;
    }
    body::before {
      width: 300px;
      height: 300px;
      background: #ffffff;
      top: 10%;
      left: -150px;
    }
    body::after {
      width: 400px;
      height: 400px;
      background: #1b98e0;
      bottom: 15%;
      right: -200px;
    }
    .container {
      max-width: 900px;
      background: #fff;
      margin: 30px auto;
      padding: 30px 40px;
      border-radius: 15px;
      box-shadow: 0 12px 30px rgba(0,0,0,0.15);
      position: relative;
      z-index: 1;
    }
    header {
      text-align: center;
      margin-bottom: 40px;
    }
    header img {
      width: 140px;
      height: 140px;
      border-radius: 50%;
      object-fit: cover;
      border: 4px solid #2980b9;
      margin-bottom: 15px;
      transition: transform 0.3s ease;
    }
    header img:hover {
      transform: scale(1.05);
    }
    header h1 {
      margin: 0;
      font-weight: 700;
      font-size: 2.8rem;
      color: #2980b9;
    }
    header p {
      font-size: 1.1rem;
      color: #555;
      margin-top: 8px;
      font-weight: 500;
    }
    section {
      margin-bottom: 30px;
    }
    section h2 {
      font-weight: 700;
      color: #2980b9;
      border-bottom: 3px solid #2980b9;
      padding-bottom: 8px;
      margin-bottom: 15px;
      font-size: 1.8rem;
    }
    section p, section ul {
      font-size: 1.1rem;
    }
    ul {
      padding-left: 20px;
      list-style-type: square;
    }
    ul li {
      margin-bottom: 8px;
      transition: color 0.3s ease;
    }
    ul li:hover {
      color: #2980b9;
      cursor: default;
    }
    a {
      color: #2980b9;
      text-decoration: none;
      font-weight: 600;
      transition: color 0.3s ease;
    }
    a:hover {
      color: #1a5276;
      text-decoration: underline;
    }
    .contact-btn {
      display: inline-block;
      margin-top: 10px;
      padding: 10px 25px;
      background-color: #2980b9;
      color: white;
      border-radius: 30px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1.1px;
      box-shadow: 0 4px 12px rgba(41, 128, 185, 0.5);
      transition: background-color 0.3s ease;
    }
    .contact-btn:hover {
      background-color: #1a5276;
    }
    @media (max-width: 600px) {
      .container {
        padding: 20px 15px;
      }
      header h1 {
        font-size: 2rem;
      }
      section h2 {
        font-size: 1.5rem;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <!-- Replace profile.jpg with your picture -->
      <img src="profile.jpg" alt="Asghar Ali Profile Picture" />
      <h1>Asghar Ali</h1>
      <p>Junior Scientific Assistant | Chemical Testing Lab, Saindak, Chaghi, Balochistan</p>
    </header>

    <section>
      <h2>Education</h2>
      <p>Associate Degree of Science (2022 - 2024)<br />University of Balochistan</p>
    </section>

    <section>
      <h2>Certifications</h2>
      <ul>
        <li>Primary Teaching Certification (1 Year)</li>
        <li>Safety Manager Certification from Saindak</li>
      </ul>
    </section>

    <section>
      <h2>Skills</h2>
      <ul>
        <li>Chemical Testing and Analysis</li>
        <li>Volumetric Analysis and Sulfur Testing</li>
        <li>Lab Safety and Management</li>
        <li>Report Writing and Documentation</li>
      </ul>
    </section>

    <section>
      <h2>Contact</h2>
      <p>Email: <a href="mailto:asgharsanjarani318@gmail.com">asgharsanjarani318@gmail.com</a></p>
      <a href="mailto:asgharsanjarani318@gmail.com" class="contact-btn">Get in Touch</a>
    </section>
  </div>
</body>
</html>
