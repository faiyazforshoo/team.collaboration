# team.collaboration
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mobshi Computers - IT and Cyber Services</title>
    <style>
        :root {
            --primary: #4a0e78;
            --primary-light: #6b24a0;
            --secondary: #e0c6ff;
            --background: #f8f4ff;
            --text: #333333;
            --white: #ffffff;
        }

        body, html {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--background);
            color: var(--text);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            background-color: var(--primary);
            color: var(--white);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
            color: var(--white);
        }

        .logo img {
            width: 50px;
            height: auto;
            margin-right: 10px;
        }

        .nav-links a {
            color: var(--white);
            text-decoration: none;
            margin-left: 20px;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--white);
            font-size: 1.5rem;
            cursor: pointer;
        }

        .mobile-menu {
            display: none;
            position: fixed;
            top: 60px;
            left: 0;
            right: 0;
            background-color: var(--primary);
            padding: 1rem;
        }

        .mobile-menu a {
            display: block;
            color: var(--white);
            text-decoration: none;
            padding: 0.5rem 0;
        }

        main {
            padding-top: 80px;
            min-height: calc(100vh - 80px - 60px);
        }

        .hero {
            background: linear-gradient(rgba(74, 14, 120, 0.8), rgba(74, 14, 120, 0.6)), url('https://hebbkx1anhila5yf.public.blob.vercel-storage.com/mobsi%20.jpg-VKUK4BbY2EWEOWLVjRQwSEfqST6Hkv.jpeg');
            background-size: cover;
            background-position: center;
            color: var(--white);
            text-align: center;
            padding: 4rem 0;
        }

        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }

        .cta-button {
            display: inline-block;
            background-color: var(--primary);
            color: var(--white);
            padding: 0.75rem 1.5rem;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background-color 0.3s ease;
        }

        .cta-button:hover {
            background-color: var(--primary-light);
        }

        .services {
            padding: 4rem 0;
        }

        .services h2 {
            text-align: center;
            margin-bottom: 2rem;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background-color: var(--white);
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            padding: 1.5rem;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-5px);
        }

        .service-card img {
            width: 64px;
            height: 64px;
            margin-bottom: 1rem;
        }

        .about {
            background-color: var(--secondary);
            padding: 4rem 0;
        }

        .about-content {
            display: flex;
            align-items: center;
            gap: 2rem;
        }

        .about-image {
            flex: 1;
        }

        .about-image img {
            width: 100%;
            border-radius: 8px;
        }

        .about-text {
            flex: 1;
        }

        footer {
            background-color: var(--primary);
            color: var(--white);
            text-align: center;
            padding: 1rem 0;
        }

        .neural-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.1;
            pointer-events: none;
        }

        .neuron {
            position: absolute;
            width: 10px;
            height: 10px;
            background-color: var(--primary);
            border-radius: 50%;
            animation: pulse 2s infinite;
        }

        .neural-connection {
            position: absolute;
            height: 1px;
            background-color: var(--primary);
            animation: fade 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.5); opacity: 0.7; }
            100% { transform: scale(1); opacity: 1; }
        }

        @keyframes fade {
            0% { opacity: 0.1; }
            50% { opacity: 0.5; }
            100% { opacity: 0.1; }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .mobile-menu-btn {
                display: block;
            }

            .about-content {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="neural-container" id="neuralNetwork"></div>

    <header>
        <nav class="container">
            <a href="index.html" class="logo">
                <img src="https://hebbkx1anhila5yf.public.blob.vercel-storage.com/mobsi%20.jpg-VKUK4BbY2EWEOWLVjRQwSEfqST6Hkv.jpeg" alt="Mobshi Computers Logo">
                <span>Mobshi Computers</span>
            </a>
            <div class="nav-links">
                <a href="index@back to homepage.html">Home</a>
                <a href="combined mobshi@ IT page.html">IT Services</a>
                <a href="combined mobshi@ Cyber services.html">Cyber Services</a>
                <a href="#about">About</a>
                <a href="#contact">Contact</a>
            </div>
            <button class="mobile-menu-btn">☰</button>
        </nav>
    </header>

    <div class="mobile-menu">
        <a href="index.html">Home</a>
        <a href="IT katana.html">IT Services</a>
        <a href="cyber-services.html">Cyber Services</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
    </div>

    <main>
        <section class="hero">
            <div class="container">
                <h1>Welcome to Mobshi Computers</h1>
                <p>Your one-stop solution for IT and Cyber Services</p>
                <a href="#services" class="cta-button">Explore Our Services</a>
            </div>
        </section>

        <section id="services" class="services">
            <div class="container">
                <h2>Our Services</h2>
                <div class="services-grid">
                    <div class="service-card">
                        <img src="/placeholder.svg?height=64&width=64" alt="IT Services Icon">
                        <h3>IT Services</h3>
                        <p>Comprehensive IT solutions for your business needs</p>
                        <a href="IT katana.html" class="cta-button">Learn More</a>
                    </div>
                    <div class="service-card">
                        <img src="/placeholder.svg?height=64&width=64" alt="Cyber Services Icon">
                        <h3>Cyber Services</h3>
                        <p>Protect your digital assets with our cyber security services</p>
                        <a href="cyber-services.html" class="cta-button">Learn More</a>
                    </div>
                    <div class="service-card">
                        <img src="/placeholder.svg?height=64&width=64" alt="Government Services Icon">
                        <h3>Government Services</h3>
                        <p>Assistance with various government-related applications</p>
                        <a href="government-services.html" class="cta-button">Learn More</a>
                    </div>
                </div>
            </div>
        </section>

        <section id="about" class="about">
            <div class="container">
                <div class="about-content">
                    <div class="about-image">
                        <img src="/placeholder.svg?height=400&width=600" alt="About Mobshi Computers">
                    </div>
                    <div class="about-text">
                        <h2>About Mobshi Computers</h2>
                        <p>Mobshi Computers is a leading provider of IT and Cyber services. With years of experience and a team of skilled professionals, we offer cutting-edge solutions to meet all your technology needs.</p>
                        <p>Our commitment to excellence and customer satisfaction sets us apart in the industry. Whether you need IT support, cyber security services, or assistance with government applications, we've got you covered.</p>
                        <p>We also offer various certified computer classes.</p>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2024 Mobshi Computers. All rights reserved.</p>
        </div>
    </footer>

    <script>
        function createNeuralNetwork() {
            const container = document.getElementById('neuralNetwork');
            const neurons = 20;
            
            for(let i = 0; i < neurons; i++) {
                const neuron = document.createElement('div');
                neuron.className = 'neuron';
                neuron.style.left = `${Math.random() * 100}%`;
                neuron.style.top = `${Math.random() * 100}%`;
                neuron.style.animationDelay = `${Math.random() * 2}s`;
                container.appendChild(neuron);

                for(let j = 0; j < 2; j++) {
                    const connection = document.createElement('div');
                    connection.className = 'neural-connection';
                    const angle = Math.random() * 360;
                    const length = 50 + Math.random() * 100;
                    connection.style.width = `${length}px`;
                    connection.style.left = neuron.style.left;
                    connection.style.top = neuron.style.top;
                    connection.style.transform = `rotate(${angle}deg)`;
                    connection.style.animationDelay = `${Math.random() * 2}s`;
                    container.appendChild(connection);
                }
            }
        }

        document.addEventListener('DOMContentLoaded', function() {
            createNeuralNetwork();

            const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
            const mobileMenu = document.querySelector('.mobile-menu');

            mobileMenuBtn.addEventListener('click', function() {
                mobileMenu.style.display = mobileMenu.style.display === 'block' ? 'none' : 'block';
            });

            // Close mobile menu when a link is clicked
            const mobileMenuLinks = mobileMenu.querySelectorAll('a');
            mobileMenuLinks.forEach(link => {
                link.addEventListener('click', function() {
                    mobileMenu.style.display = 'none';
                });
            });

            // Smooth scrolling for anchor links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    document.querySelector(this.getAttribute('href')).scrollIntoView({
                        behavior: 'smooth'
                    });
                });
            });
        });
    </script>
</body>
</html>
