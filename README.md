<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ragam Elyssia - Luxury Branding</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
    <style>
        body {
            font-family: 'Playfair Display', serif;
            margin: 0;
            padding: 0;
            background-color: #0d0d0d;
            color: #fff;
            text-align: center;
            scroll-behavior: smooth;
        }
        nav {
            background-color: #111;
            padding: 15px;
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
        }
        nav a {
            color: gold;
            text-decoration: none;
            margin: 0 15px;
            font-size: 1.2rem;
        }
        .hero {
            background: url('luxury-background.jpg') no-repeat center center/cover;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            opacity: 0;
        }
        h1 {
            font-size: 3rem;
            letter-spacing: 2px;
            color: gold;
        }
        p {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 10px auto;
        }
        .cta {
            background-color: gold;
            color: #0d0d0d;
            padding: 10px 20px;
            text-decoration: none;
            font-size: 1.2rem;
            border-radius: 5px;
            margin-top: 20px;
            display: inline-block;
            transition: transform 0.3s ease;
        }
        .cta:hover {
            transform: scale(1.1);
        }
        .section {
            padding: 50px 20px;
        }
        .portfolio img {
            width: 100%;
            border-radius: 10px;
            margin-top: 20px;
            cursor: pointer;
            transition: transform 0.3s;
        }
        .portfolio img:hover {
            transform: scale(1.05);
        }
        .testimonial-slider {
            display: flex;
            overflow: hidden;
            white-space: nowrap;
            width: 100%;
            max-width: 600px;
            margin: auto;
        }
        .testimonial {
            display: inline-block;
            width: 100%;
            font-style: italic;
            padding: 10px;
        }
        .contact-form input, .contact-form textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: none;
            border-radius: 5px;
        }
        .contact-form button {
            background-color: gold;
            color: black;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            gsap.to(".hero", {opacity: 1, duration: 1.5, ease: "power2.out"});
            let testimonials = document.querySelectorAll(".testimonial");
            let index = 0;
            function rotateTestimonials() {
                testimonials[index].style.display = "none";
                index = (index + 1) % testimonials.length;
                testimonials[index].style.display = "block";
            }
            setInterval(rotateTestimonials, 3000);
        });
    </script>
</head>
<body>
    <nav>
        <a href="#home">Home</a>
        <a href="#portfolio">Portfolio</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
    </nav>
    
    <div class="hero" id="home">
        <h1>Ragam Elyssia</h1>
        <p>Where Art Meets Luxury. Elevate your brand with AI-powered luxury branding.</p>
        <a href="#contact" class="cta">Work With Us</a>
    </div>
    
    <div class="section portfolio" id="portfolio">
        <h2>Our Portfolio</h2>
        <p>Explore our finest luxury branding works crafted with AI precision and artistic expertise.</p>
        <img src="portfolio-example.jpg" alt="Luxury branding design">
    </div>
    
    <div class="section services" id="services">
        <h2>Our Services</h2>
        <p>We offer luxury branding solutions including logo design, packaging, web design, and full brand strategy.</p>
        <div class="testimonial-slider">
            <p class="testimonial">“Ragam Elyssia transformed our brand into a masterpiece.” – Luxury Client</p>
            <p class="testimonial" style="display:none;">“A true blend of AI and art, simply stunning.” – High-end Brand</p>
        </div>
    </div>
    
    <div class="section contact" id="contact">
        <h2>Contact Us</h2>
        <p>Ready to elevate your brand? Get in touch with us.</p>
        <form class="contact-form" action="https://formspree.io/f/yourformid" method="POST">
            <input type="text" name="name" placeholder="Your Name" required>
            <input type="email" name="email" placeholder="Your Email" required>
            <textarea name="message" placeholder="Your Message" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </div>
</body>
</html>
