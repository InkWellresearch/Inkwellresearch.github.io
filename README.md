<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Inkwell Research Solutions</title>
    <style>
        /* Adjust ribbon to position elements properly */
        .ribbon {
            display: flex;
            align-items: center;
            justify-content: flex-start; /* Aligns elements to the left */
            padding: 10px 20px;
            background-color: #f0f0f0;
            border-bottom: 1px solid #ccc;
            position: relative;
        }

        /* Position hamburger menu next to the logo */
        .hamburger {
            display: flex;
            flex-direction: column;
            cursor: pointer;
            margin-right: 10px;
        }

        /* Style for the lines in the hamburger menu */
        .line {
            width: 30px;
            height: 3px;
            background-color: #333;
            margin: 3px 0;
        }

        /* Align logo and hamburger to the left */
        .logo {
            display: flex;
            align-items: center;
        }

        .logo img {
            height: 50px;
        }

        /* Auth buttons moved to the right side of the ribbon */
        .auth-buttons {
            display: flex;
            position: absolute;
            right: 20px;
        }

        /* Button styles */
        .btn {
            margin-left: 15px;
            padding: 8px 15px;
            background-color: #007bff;
            color: white;
            text-decoration: none;
            border-radius: 4px;
        }

        .btn:hover {
            background-color: #0056b3;
        }

        /* Sidebar styles */
        .sidebar {
            position: fixed;
            top: 0;
            left: 0;
            width: 250px;
            height: 100%;
            background-color: #fff;
            border-right: 1px solid #ccc;
            box-shadow: 2px 0 5px rgba(0, 0, 0, 0.2);
            transform: translateX(-100%);
            transition: transform 0.3s ease;
            z-index: 1000;
        }

        .sidebar.visible {
            transform: translateX(0);
        }

        .sidebar .close-btn {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 24px;
            cursor: pointer;
            color: #333;
        }

        .sidebar ul {
            list-style: none;
            padding: 20px;
        }

        .sidebar ul li {
            margin: 15px 0;
        }

        .sidebar ul li a {
            text-decoration: none;
            color: #333;
        }

        .sidebar ul li a:hover {
            background-color: #f0f0f0;
        }

        /* Banner section styles */
        .banner {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            text-align: center;
            padding: 20px;
        }

        /* Other styles for sections */
        section {
            padding: 20px;
            margin: 20px 0;
        }
    </style>
</head>
<body>
    <!-- Ribbon -->
    <div class="ribbon">
        <div class="hamburger" id="hamburger">
            <div class="line"></div>
            <div class="line"></div>
            <div class="line"></div>
        </div>
        <div class="logo">
            <img src="logo.png" alt="Inkwell Research Solutions Logo" />
        </div>
        <div class="auth-buttons">
            <a href="#login" class="btn">Log In</a>
            <a href="#signup" class="btn">Sign Up</a>
        </div>
    </div>

    <!-- Sidebar Navigation -->
    <nav id="sidebar" class="sidebar">
        <div class="close-btn" id="close-btn">&times;</div>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About Us</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#quotation">Get Quotation</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Banner Section -->
    <section id="home" class="banner">
        <h1>Welcome to Inkwell Research Solutions</h1>
        <p>Your go-to solution for professional research and thesis writing services.</p>
        <a href="#quotation" class="cta-button btn">Get a Quotation</a>
    </section>

    <!-- About Us Section -->
    <section id="about" class="about-us">
        <h2>About Us</h2>
        <p>At Inkwell Research Solutions, we provide comprehensive support for students and professionals in writing and refining research papers, theses, and more.</p>
    </section>

    <!-- Services Section -->
    <section id="services" class="services">
        <h2>Our Services</h2>
        <ul>
            <li>Research Paper Writing</li>
            <li>Thesis and Dissertation Assistance</li>
            <li>Editing and Proofreading</li>
            <li>Formatting Services</li>
        </ul>
    </section>

    <!-- Get Quotation Section -->
    <section id="quotation" class="quotation">
        <h2>Get a Quotation</h2>
        <p>Interested in our services? Fill out our form and we’ll get back to you with a customized quote.</p>
        <a href="#contact" class="cta-button btn">Contact Us</a>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <h2>Contact Us</h2>
        <p>Email: <a href="mailto:info@inkwellresearch.com">info@inkwellresearch.com</a> | Phone: +123 456 7890</p>
        <form action="submit_form.php" method="post">
            <label for="name">Your Name:</label>
            <input type="text" id="name" name="name" required>

            <label for="email">Your Email:</label>
            <input type="email" id="email" name="email" required>

            <label for="message">Message:</label>
            <textarea id="message" name="message" rows="4" required></textarea>

            <button type="submit">Send Message</button>
        </form>
    </section>

    <!-- Footer Section -->
    <footer>
        <p>&copy; 2024 Inkwell Research Solutions</p>
        <div class="journal-logos">
            <a href="https://example.com/journal1" target="_blank"><img src="journal1-logo.png" alt="Journal 1 Logo"></a>
            <a href="https://example.com/journal2" target="_blank"><img src="journal2-logo.png" alt="Journal 2 Logo"></a>
            <a href="https://example.com/journal3" target="_blank"><img src="journal3-logo.png" alt="Journal 3 Logo"></a>
        </div>
    </footer>

    <script>
        // JavaScript for toggling sidebar
        const hamburger = document.getElementById('hamburger');
        const sidebar = document.getElementById('sidebar');
        const closeBtn = document.getElementById('close-btn');

        hamburger.addEventListener('click', () => {
            sidebar.classList.toggle('visible');
        });

        closeBtn.addEventListener('click', () => {
            sidebar.classList.remove('visible');
        });
    </script>
</body>
</html>
