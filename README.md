<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Grace Community Church</title>
    <style>
        :root {
            --primary: #4a6b7f;
            --secondary: #a36f56;
            --light: #f8f9fa;
            --dark: #343a40;
            --accent: #9cbfd8;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
        }
        
        header {
            background: var(--primary);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo h1 {
            font-size: 1.8rem;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--accent);
        }
        
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(74, 107, 127, 0.7), rgba(74, 107, 127, 0.7)), 
                        url('https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/406f53e0-73b3-4d09-8598-2827ebe6b12b.png') no-repeat center center/cover;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
            margin-top: 60px;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        .hero h2 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background: var(--secondary);
            color: white;
            padding: 0.8rem 1.8rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            text-decoration: none;
            font-size: 1rem;
            transition: background 0.3s;
        }
        
        .btn:hover {
            background: #8a5d44;
        }
        
        section {
            padding: 5rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            padding-bottom: 0.5rem;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: var(--secondary);
        }
        
        .about {
            background-color: white;
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }
        
        .about-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .services {
            background-color: var(--light);
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .service-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            text-align: center;
            transition: transform 0.3s;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
        }
        
        .service-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 5px;
            margin-bottom: 1rem;
        }
        
        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        .contact {
            background-color: white;
        }
        
        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }
        
        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .contact-info p {
            margin-bottom: 1.5rem;
        }
        
        .info-item {
            display: flex;
            margin-bottom: 1rem;
            align-items: center;
        }
        
        .info-item i {
            margin-right: 1rem;
            color: var(--secondary);
            font-size: 1.2rem;
        }
        
        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 1rem;
            margin-bottom: 1rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }
        
        .contact-form textarea {
            height: 150px;
        }
        
        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem 0;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .social-links {
            margin-top: 1rem;
        }
        
        .social-links a {
            color: white;
            margin: 0 0.5rem;
            text-decoration: none;
            font-size: 1.2rem;
        }
        
        /* Mobile Navigation */
        .menu-toggle {
            display: none;
            cursor: pointer;
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 70px;
                left: 0;
                width: 100%;
                background: var(--primary);
                flex-direction: column;
                padding: 1rem 0;
                text-align: center;
            }
            
            .nav-links.show {
                display: flex;
            }
            
            .nav-links li {
                margin: 0.5rem 0;
            }
            
            .menu-toggle {
                display: block;
            }
            
            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <nav>
                <div class="logo">
                    <h1>Grace Community</h1>
                </div>
                <div class="menu-toggle">
                    ☰
                </div>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="hero-content">
            <h2>Welcome to Grace Community Church</h2>
            <p>A place where faith, hope, and love abide. Join us as we grow together in Christ's love.</p>
            <a href="#services" class="btn">Our Services</a>
        </div>
    </section>

    <section class="about" id="about">
        <div class="container">
            <div class="section-title">
                <h2>Our Story</h2>
            </div>
            <div class="about-content">
                <div class="about-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/d79cb720-e56a-4509-a77e-f6f5add06ccf.png" alt="Historic church building with stained glass windows and wooden pews, sunlight streaming through the windows" />
                </div>
                <div class="about-text">
                    <h3>Who We Are</h3>
                    <p>Grace Community Church was founded in 1985 with a vision to create a welcoming space for all to worship and grow in their faith. We are a diverse congregation united by our love for Christ and commitment to serving our community.</p>
                    <p>Our mission is to spread the Gospel, nurture believers, and demonstrate God's love through acts of service and compassion. We believe in the authority of Scripture, the power of prayer, and the importance of Christian fellowship.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="services" id="services">
        <div class="container">
            <div class="section-title">
                <h2>Our Services</h2>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/dad51e0d-64d9-4a82-8c5c-de60c1d3a08a.png" alt="Sunday morning worship service with congregants singing and raising hands in praise" />
                    <h3>Sunday Worship</h3>
                    <p>Join us every Sunday at 9:00am & 11:00am for inspiring worship and biblical teaching.</p>
                </div>
                <div class="service-card">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/a48bc59f-48d4-4388-acec-33c3b6cf7e8f.png" alt="Small group Bible study with people sitting in a circle discussing scriptures" />
                    <h3>Bible Study</h3>
                    <p>Mid-week Bible study on Wednesdays at 7:00pm for deeper scripture exploration.</p>
                </div>
                <div class="service-card">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/94757bf0-2270-48df-ac48-c4f1d63e5d80.png" alt="Youth group activity with teenagers playing games and laughing together" />
                    <h3>Youth Ministry</h3>
                    <p>Friday nights at 6:30pm for teens to connect, grow, and have fun in a faith-filled environment.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Us</h2>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Get in Touch</h3>
                    <p>We'd love to hear from you! Whether you have questions, prayer requests, or want to get involved, reach out to us.</p>
                    
                    <div class="info-item">
                        <i>📍</i>
                        <p>123 Faith Avenue, Cityville, ST 12345</p>
                    </div>
                    <div class="info-item">
                        <i>📞</i>
                        <p>(555) 123-4567</p>
                    </div>
                    <div class="info-item">
                        <i>✉️</i>
                        <p>info@gracecommunity.org</p>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <input type="text" placeholder="Your Name" required>
                        <input type="email" placeholder="Your Email" required>
                        <input type="text" placeholder="Subject">
                        <textarea placeholder="Your Message" required></textarea>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <p>© 2023 Grace Community Church. All Rights Reserved.</p>
                <div class="social-links">
                    <a href="#">Facebook</a>
                    <a href="#">Twitter</a>
                    <a href="#">Instagram</a>
                    <a href="#">YouTube</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        document.querySelector('.menu-toggle').addEventListener('click', function() {
            document.querySelector('.nav-links').classList.toggle('show');
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
                
                // Close mobile menu if open
                document.querySelector('.nav-links').classList.remove('show');
            });
        });
    </script>
</body>
</html>

