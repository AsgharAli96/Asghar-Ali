<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dev Portfolio | Showcasing My Work</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Raleway:wght@700;800&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --secondary: #8b5cf6;
            --dark: #1e293b;
            --light: #f8fafc;
            --gray: #64748b;
            --light-gray: #e2e8f0;
            --transition: all 0.3s ease;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            padding: 20px 0;
            transition: var(--transition);
        }

        header.scrolled {
            padding: 15px 0;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Raleway', sans-serif;
            font-weight: 800;
            font-size: 28px;
            color: var(--primary);
            text-decoration: none;
        }

        .logo span {
            color: var(--secondary);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            font-size: 17px;
            transition: var(--transition);
            position: relative;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            transition: var(--transition);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 120px 0 80px;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -20%;
            width: 600px;
            height: 600px;
            border-radius: 50%;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            opacity: 0.1;
            z-index: -1;
        }

        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .hero-text {
            flex: 1;
            padding-right: 40px;
        }

        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
            animation: float 6s ease-in-out infinite;
        }

        .hero-image img {
            width: 80%;
            max-width: 400px;
            border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
        }

        .hero h3 {
            font-size: 24px;
            color: var(--primary);
            margin-bottom: 15px;
        }

        .hero h1 {
            font-family: 'Raleway', sans-serif;
            font-size: 60px;
            font-weight: 800;
            line-height: 1.1;
            margin-bottom: 20px;
            color: var(--dark);
        }

        .hero h1 span {
            color: var(--primary);
        }

        .hero p {
            font-size: 18px;
            margin-bottom: 30px;
            color: var(--gray);
            max-width: 600px;
        }

        .btn {
            display: inline-block;
            padding: 14px 32px;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            color: white;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 16px;
            box-shadow: 0 10px 20px rgba(37, 99, 235, 0.3);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 25px rgba(37, 99, 235, 0.4);
        }

        /* Section Styling */
        section {
            padding: 100px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 70px;
        }

        .section-title h2 {
            font-family: 'Raleway', sans-serif;
            font-size: 40px;
            font-weight: 700;
            color: var(--dark);
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            border-radius: 2px;
        }

        /* About Section */
        .about-content {
            display: flex;
            align-items: center;
            gap: 60px;
        }

        .about-text {
            flex: 1;
        }

        .about-text h3 {
            font-size: 28px;
            margin-bottom: 20px;
            color: var(--dark);
        }

        .about-text p {
            margin-bottom: 20px;
            color: var(--gray);
        }

        .about-stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 30px;
            margin-top: 30px;
        }

        .stat-box {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            text-align: center;
            transition: var(--transition);
        }

        .stat-box:hover {
            transform: translateY(-10px);
        }

        .stat-box i {
            font-size: 40px;
            color: var(--primary);
            margin-bottom: 15px;
        }

        .stat-box h4 {
            font-size: 20px;
            margin-bottom: 5px;
        }

        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 40px;
        }

        .skill-category h3 {
            font-size: 24px;
            margin-bottom: 25px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--light-gray);
        }

        .skill-bar {
            margin-bottom: 25px;
        }

        .skill-info {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }

        .skill-bar-container {
            height: 10px;
            background-color: var(--light-gray);
            border-radius: 5px;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            border-radius: 5px;
            position: relative;
            width: 0;
            transition: width 1.5s ease-in-out;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }

        .project-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: var(--transition);
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
        }

        .project-img {
            height: 220px;
            overflow: hidden;
        }

        .project-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .project-card:hover .project-img img {
            transform: scale(1.05);
        }

        .project-content {
            padding: 25px;
        }

        .project-content h3 {
            font-size: 22px;
            margin-bottom: 10px;
        }

        .project-content p {
            color: var(--gray);
            margin-bottom: 20px;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }

        .project-tag {
            background-color: var(--light-gray);
            color: var(--dark);
            padding: 5px 12px;
            border-radius: 50px;
            font-size: 14px;
        }

        /* Contact Section */
        .contact-container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 50px;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .contact-item {
            display: flex;
            gap: 20px;
        }

        .contact-item i {
            font-size: 24px;
            color: var(--primary);
            width: 60px;
            height: 60px;
            background-color: rgba(37, 99, 235, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .contact-text h4 {
            font-size: 20px;
            margin-bottom: 8px;
        }

        .contact-text p {
            color: var(--gray);
        }

        .contact-form .form-group {
            margin-bottom: 25px;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 15px;
            border: 1px solid var(--light-gray);
            border-radius: 8px;
            font-family: 'Poppins', sans-serif;
            font-size: 16px;
            transition: var(--transition);
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.1);
        }

        .contact-form textarea {
            height: 150px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 70px 0 30px;
        }

        .footer-content {
            display: flex;
            justify-content: space-between;
            margin-bottom: 50px;
        }

        .footer-about {
            flex: 2;
            padding-right: 50px;
        }

        .footer-links {
            flex: 1;
        }

        .footer-about h3,
        .footer-links h3 {
            font-size: 24px;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-about h3::after,
        .footer-links h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
        }

        .footer-about p {
            color: var(--light-gray);
            margin-bottom: 20px;
        }

        .social-links {
            display: flex;
            gap: 15px;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            transition: var(--transition);
        }

        .social-links a:hover {
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            transform: translateY(-5px);
        }

        .footer-links ul {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 15px;
        }

        .footer-links a {
            text-decoration: none;
            color: var(--light-gray);
            transition: var(--transition);
        }

        .footer-links a:hover {
            color: var(--primary);
            padding-left: 5px;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--light-gray);
            font-size: 14px;
        }

        /* Animations */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .hero-content {
                flex-direction: column;
                text-align: center;
            }
            
            .hero-text {
                padding-right: 0;
                margin-bottom: 50px;
            }
            
            .hero h1 {
                font-size: 48px;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .skills-container,
            .contact-container {
                grid-template-columns: 1fr;
            }
            
            .footer-content {
                flex-direction: column;
                gap: 40px;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero h3 {
                font-size: 20px;
            }
            
            .section-title h2 {
                font-size: 32px;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .about-stats {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="container nav-container">
            <a href="#" class="logo">Dev<span>Portfolio</span></a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container hero-content">
            <div class="hero-text">
                <h3>Hello, I'm a</h3>
                <h1>Full Stack <span>Developer</span></h1>
                <p>I build exceptional digital experiences that are fast, accessible, visually appealing, and responsive. Even if you don't realize it, I believe in creating solutions that users love.</p>
                <div class="hero-btns">
                    <a href="#projects" class="btn">View My Work</a>
                    <a href="#contact" class="btn" style="background: white; color: var(--primary); margin-left: 15px; box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);">Contact Me</a>
                </div>
            </div>
            <div class="hero-image">
                <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=400&q=80" alt="Developer">
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Curious about me? Here you go!</h3>
                    <p>I'm a passionate software developer with expertise in building high-quality websites and applications. With a strong foundation in computer science and several years of experience, I specialize in creating efficient, scalable, and user-friendly solutions.</p>
                    <p>My approach combines technical excellence with creative problem-solving. I enjoy turning complex problems into simple, intuitive solutions. When I'm not coding, you'll find me exploring new technologies, contributing to open-source projects, or hiking in nature.</p>
                    
                    <div class="about-stats">
                        <div class="stat-box">
                            <i class="fas fa-code"></i>
                            <h4>50+</h4>
                            <p>Projects Completed</p>
                        </div>
                        <div class="stat-box">
                            <i class="fas fa-users"></i>
                            <h4>30+</h4>
                            <p>Happy Clients</p>
                        </div>
                        <div class="stat-box">
                            <i class="fas fa-award"></i>
                            <h4>15+</h4>
                            <p>Awards Received</p>
                        </div>
                        <div class="stat-box">
                            <i class="fas fa-coffee"></i>
                            <h4>1000+</h4>
                            <p>Cups of Coffee</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" style="background-color: #f5f9ff;">
        <div class="container">
            <div class="section-title">
                <h2>My Skills</h2>
            </div>
            <div class="skills-container">
                <div class="skill-category">
                    <h3>Technical Skills</h3>
                    <div class="skill-bar">
                        <div class="skill-info">
                            <span>JavaScript</span>
                            <span>95%</span>
                        </div>
                        <div class="skill-bar-container">
                            <div class="skill-progress" data-width="95"></div>
                        </div>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-info">
                            <span>React</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar-container">
                            <div class="skill-progress" data-width="90"></div>
                        </div>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-info">
                            <span>Node.js</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar-container">
                            <div class="skill-progress" data-width="85"></div>
                        </div>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-info">
                            <span>HTML/CSS</span>
                            <span>98%</span>
                        </div>
                        <div class="skill-bar-container">
                            <div class="skill-progress" data-width="98"></div>
                        </div>
                    </div>
                </div>
                <div class="skill-category">
                    <h3>Professional Skills</h3>
                    <div class="skill-bar">
                        <div class="skill-info">
                            <span>Communication</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar-container">
                            <div class="skill-progress" data-width="90"></div>
                        </div>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-info">
                            <span>Problem Solving</span>
                            <span>92%</span>
                        </div>
                        <div class="skill-bar-container">
                            <div class="skill-progress" data-width="92"></div>
                        </div>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-info">
                            <span>Project Management</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar-container">
                            <div class="skill-progress" data-width="85"></div>
                        </div>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-info">
                            <span>Teamwork</span>
                            <span>88%</span>
                        </div>
                        <div class="skill-bar-container">
                            <div class="skill-progress" data-width="88"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <div class="section-title">
                <h2>My Projects</h2>
            </div>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-img">
                        <img src="https://images.unsplash.com/photo-1555066931-4365d14bab8c?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=600&q=80" alt="Project">
                    </div>
                    <div class="project-content">
                        <h3>E-Commerce Platform</h3>
                        <p>A full-featured online shopping platform with payment processing, inventory management, and user accounts.</p>
                        <div class="project-tags">
                            <span class="project-tag">React</span>
                            <span class="project-tag">Node.js</span>
                            <span class="project-tag">MongoDB</span>
                        </div>
                        <a href="#" class="btn">View Project</a>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-img">
                        <img src="https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=600&q=80" alt="Project">
                    </div>
                    <div class="project-content">
                        <h3>Task Management App</h3>
                        <p>A productivity application for teams to manage projects, assign tasks, and track progress in real-time.</p>
                        <div class="project-tags">
                            <span class="project-tag">Vue.js</span>
                            <span class="project-tag">Firebase</span>
                            <span class="project-tag">Tailwind CSS</span>
                        </div>
                        <a href="#" class="btn">View Project</a>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-img">
                        <img src="https://images.unsplash.com/photo-1531403009284-440f080d1e12?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=600&q=80" alt="Project">
                    </div>
                    <div class="project-content">
                        <h3>Fitness Tracking App</h3>
                        <p>Mobile application that helps users track workouts, set goals, and monitor fitness progress over time.</p>
                        <div class="project-tags">
                            <span class="project-tag">React Native</span>
                            <span class="project-tag">Redux</span>
                            <span class="project-tag">GraphQL</span>
                        </div>
                        <a href="#" class="btn">View Project</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" style="background-color: #f5f9ff;">
        <div class="container">
            <div class="section-title">
                <h2>Contact Me</h2>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <div class="contact-text">
                            <h4>Location</h4>
                            <p>San Francisco, California</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <div class="contact-text">
                            <h4>Email</h4>
                            <p>contact@devportfolio.com</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <div class="contact-text">
                            <h4>Phone</h4>
                            <p>+1 (555) 123-4567</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <input type="text" placeholder="Your Name" required>
                        </div>
                        <div class="form-group">
                            <input type="email" placeholder="Your Email" required>
                        </div>
                        <div class="form-group">
                            <input type="text" placeholder="Subject" required>
                        </div>
                        <div class="form-group">
                            <textarea placeholder="Your Message" required></textarea>
                        </div>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-about">
                    <h3>DevPortfolio</h3>
                    <p>Creating innovative digital solutions with passion and precision. I specialize in building responsive, user-friendly websites and applications that help businesses thrive online.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-github"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-dribbble"></i></a>
                    </div>
                </div>
                <div class="footer-links">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#skills">Skills</a></li>
                        <li><a href="#projects">Projects</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2023 DevPortfolio. All rights reserved. Designed with ❤️</p>
            </div>
        </div>
    </footer>

    <script>
        // Header scroll effect
        window.addEventListener('scroll', function() {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });

        // Initialize skill bars when they come into view
        const skillBars = document.querySelectorAll('.skill-progress');
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const width = entry.target.getAttribute('data-width');
                    entry.target.style.width = width + '%';
                    observer.unobserve(entry.target);
                }
            });
        }, { threshold: 0.5 });
        
        skillBars.forEach(bar => {
            observer.observe(bar);
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
