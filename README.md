Ex.07 Restuarant Website
Date:
AIM:
To develop a static Resturant website to display the menu and services provided by the resturant.

DESIGN STEPS:
Step 1:
Requirement collection.

Step 2:
Creating the layout using HTML and CSS.

Step 3:
Updating the sample content.

Step 4:
Choose the appropriate style and color scheme.

Step 5:
Validate the layout in various browsers.

Step 6:
Validate the HTML code.

Step 7:
Publish the website in the given URL.

PROGRAM:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>kings Restaurant | Authentic South Indian Cuisine</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #d4af37;
            --secondary: #c62828;
            --accent: #2e7d32;
            --dark: #1a1a1a;
            --light: #f5f5f5;
            --text: #333;
        }

        body {
            background-color: var(--light);
            color: var(--text);
            line-height: 1.6;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Header */
        header {
            background-color: var(--dark);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo-icon {
            font-size: 2rem;
            color: var(--primary);
            margin-right: 0.5rem;
        }

        .logo-text {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
        }

        .logo-text span {
            color: var(--primary);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 1.5rem;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: var(--primary);
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('logo.png') no-repeat center center/cover;
            background-size: cover;
            background-position:center;
            height: 100vh;
            display: flex;
            align-items: center;
            color: white;
            text-align: center;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 2.8rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
        }

        .hero p {
            font-size: 1.1rem;
            margin-bottom: 2rem;
        }

        .btn {
            display: inline-block;
            background-color: var(--primary);
            color: var(--dark);
            padding: 0.8rem 2rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background-color: var(--secondary);
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        /* Section Styles */
        .section {
            padding: 4rem 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 2.5rem;
        }

        .section-title h2 {
            font-size: 2.2rem;
            color: var(--dark);
            position: relative;
            display: inline-block;
            padding-bottom: 10px;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--primary);
        }

        /* Menu Section */
        .menu {
            background-color: white;
        }

        .menu-items {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .menu-item {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
            border: 1px solid #eee;
        }

        .menu-item:hover {
            transform: translateY(-5px);
        }

        .menu-item-image {
            height: 180px;
            overflow: hidden;
        }

        .menu-item-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .menu-item:hover .menu-item-image img {
            transform: scale(1.05);
        }

        .menu-item-content {
            padding: 1.2rem;
        }

        .menu-item-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
        }

        .menu-item-name {
            font-weight: 700;
            font-size: 1.1rem;
        }

        .menu-item-price {
            color: var(--secondary);
            font-weight: 700;
        }

        .menu-item-description {
            color: #666;
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
        }

        .veg-indicator {
            display: inline-block;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            margin-right: 5px;
        }

        .veg {
            background-color: var(--accent);
        }

        .non-veg {
            background-color: var(--secondary);
        }

        /* Services Section */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 1.5rem;
        }

        .service-card {
            background-color: white;
            padding: 1.5rem;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }

        .service-card:hover {
            transform: translateY(-5px);
        }

        .service-icon {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .service-card h3 {
            margin-bottom: 0.8rem;
            color: var(--dark);
        }

        /* Contact Section */
        .contact-content {
            display: flex;
            gap: 2rem;
        }

        .contact-info, .contact-form {
            flex: 1;
        }

        .contact-info h3, .contact-form h3 {
            margin-bottom: 1.2rem;
            color: var(--dark);
        }

        .contact-details {
            margin-bottom: 1.5rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 0.8rem;
        }

        .contact-icon {
            width: 35px;
            height: 35px;
            background-color: var(--primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 0.8rem;
        }

        .form-group {
            margin-bottom: 1.2rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.4rem;
            font-weight: 500;
        }

        .form-control {
            width: 100%;
            padding: 0.7rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }

        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 2.5rem 0 1rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .footer-column h3 {
            color: var(--primary);
            margin-bottom: 1.2rem;
            font-size: 1.1rem;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 0.6rem;
        }

        .footer-links a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-links a:hover {
            color: var(--primary);
        }

        .social-links {
            display: flex;
            gap: 0.8rem;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 35px;
            height: 35px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: all 0.3s;
        }

        .social-links a:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #aaa;
            font-size: 0.9rem;
        }

        /* Responsive Styles */
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            nav ul {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 70px);
                background-color: var(--dark);
                flex-direction: column;
                align-items: center;
                padding-top: 2rem;
                transition: left 0.3s;
            }
            
            nav ul.active {
                left: 0;
            }
            
            nav ul li {
                margin: 1.2rem 0;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .contact-content {
                flex-direction: column;
            }
        }

        @media (max-width: 576px) {
            .section {
                padding: 2.5rem 0;
            }
            
            .section-title h2 {
                font-size: 1.8rem;
            }
            
            .hero h1 {
                font-size: 1.6rem;
            }
            
            .menu-items {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-utensils"></i>
                    </div>
                    <div class="logo-text">kings <span>Restaurant</span></div>
                </div>
                <button class="mobile-menu-btn">
                    <i class="fas fa-bars"></i>
                </button>
                <nav>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#menu">Menu</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Authentic South Indian Cuisine</h1>
                <p>Experience the rich flavors and traditional recipes of South India, crafted with passion</p>
                <a href="#menu" class="btn">Explore Our Menu</a>
            </div>
        </div>
    </section>

    <!-- Menu Section -->
    <section class="section menu" id="menu">
        <div class="container">
            <div class="section-title">
                <h2>Our Menu</h2>
            </div>
            <div class="menu-items">
                <!-- Menu Items -->
                <div class="menu-item">
                    <div class="menu-item-image">
                        <img src="dosa.png" alt="Dosa">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-header">
                            <div class="menu-item-name">
                                <span class="veg-indicator veg"></span>
                                Masala Dosa
                            </div>
                            <div class="menu-item-price">₹120</div>
                        </div>
                        <div class="menu-item-description">
                            Crispy fermented crepe with spiced potato filling
                        </div>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-item-image">
                        <img src="pongal.png" alt="Pongal">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-header">
                            <div class="menu-item-name">
                                <span class="veg-indicator veg"></span>
                               Ven Pongal
                            </div>
                            <div class="menu-item-price">₹100</div>
                        </div>
                        <div class="menu-item-description">
                            Savory rice and lentil porridge with ghee
                        </div>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-item-image">
                        <img src="sambar.png" alt="Sambar">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-header">
                            <div class="menu-item-name">
                                <span class="veg-indicator veg"></span>
                                Idli Sambar
                            </div>
                            <div class="menu-item-price">₹80</div>
                        </div>
                        <div class="menu-item-description">
                            Soft and fluffy steamed rice cakes.
                        </div>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-item-image">
                        <img src="vada.png" alt="Vada">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-header">
                            <div class="menu-item-name">
                                <span class="veg-indicator veg"></span>
                                Medu Vada
                            </div>
                            <div class="menu-item-price">₹20</div>
                        </div>
                        <div class="menu-item-description">
                            Crispy, fluffy lentil doughnuts
                        </div>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-item-image">
                        <img src="hy biriyani.png" alt="Filter Coffee">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-header">
                            <div class="menu-item-name">
                                <span class="veg-indicator non-veg"></span>
                                Hyderabad Biryani
                            </div>
                            <div class="menu-item-price">₹350</div>
                        </div>
                        <div class="menu-item-description">
                            Hyderabadi Biryani is a Fragrant basmati rice layered with spiced chicken and herbs.
                        </div>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-item-image">
                        <img src="chettinad.png" alt="Chettinad Chicken">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-header">
                            <div class="menu-item-name">
                                <span class="veg-indicator non-veg"></span>
                                Chettinad Chicken
                            </div>
                            <div class="menu-item-price">₹280</div>
                        </div>
                        <div class="menu-item-description">
                            Spicy chicken curry with aromatic flavors
                        </div>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-item-image">
                        <img src="muttan.png" alt="Pongal">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-header">
                            <div class="menu-item-name">
                                <span class="veg-indicator non-veg"></span>
                               Mutton Sukka
                            </div>
                            <div class="menu-item-price">₹100</div>
                        </div>
                        <div class="menu-item-description">
                            Tender mutton pieces cooked with rich South Indian spices.
                        </div>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-item-image">
                        <img src="fish fry.png" alt="Uttapam">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-header">
                            <div class="menu-item-name">
                                <span class="veg-indicator non-veg"></span>
                                Fish Fry
                            </div>
                            <div class="menu-item-price">₹110</div>
                        </div>
                        <div class="menu-item-description">
                           Crispy, spiced fish fillet fried to perfection.
                        </div>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-item-image">
                        <img src="filter coffee.png" alt=" Filter Coffee">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-header">
                            <div class="menu-item-name">
                                <span class="veg-indicator veg"></span>
                                Filter Coffee
                            </div>
                            <div class="menu-item-price">₹30</div>
                        </div>
                        <div class="menu-item-description">
                            Traditional South Indian filter coffee
                        </div>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-item-image">
                        <img src="jirthanda.png" alt=" Jigarthanda">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-header">
                            <div class="menu-item-name">
                                <span class="veg-indicator veg"></span>
                                 Jigarthanda
                            </div>
                            <div class="menu-item-price">₹70</div>
                        </div>
                        <div class="menu-item-description">
                            Jigarthanda is a classic South Indian drink that originated in Madurai, Tamil Nadu. 
The name translates to "cool liver" referring to its refreshing, cooling properties.
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="section" id="services">
        <div class="container">
            <div class="section-title">
                <h2>Our Services</h2>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-utensils"></i>
                    </div>
                    <h3>Dine-In</h3>
                    <p>Enjoy our authentic dishes in our comfortable dining area</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-truck"></i>
                    </div>
                    <h3>Home Delivery</h3>
                    <p>Fast and reliable delivery to your doorstep</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-calendar-alt"></i>
                    </div>
                    <h3>Catering</h3>
                    <p>Make your events memorable with our catering</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-gift"></i>
                    </div>
                    <h3>Takeaway</h3>
                    <p>Order your favorites for takeaway</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="section" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Us</h2>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Get In Touch</h3>
                    <div class="contact-details">
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>
                                <h4>Address</h4>
                                <p>Bangaluru Highway,Anna Nager, Chennai, TN 600001</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div>
                                <h4>Phone</h4>
                                <p>+91 98765 43210</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>
                                <h4>Email</h4>
                                <p>info@kingsrestaurant.com</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-clock"></i>
                            </div>
                            <div>
                                <h4>Opening Hours</h4>
                                <p>Mon-Sun: 7:00 AM - 11:00 PM</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <h3>Send Us a Message</h3>
                    <form>
                        <div class="form-group">
                            <label for="name">Your Name</label>
                            <input type="text" id="name" class="form-control" placeholder="Enter your name">
                        </div>
                        
                        <div class="form-group">
                            <label for="email">Your Email</label>
                            <input type="email" id="email" class="form-control" placeholder="Enter your email">
                        </div>
                        
                        <div class="form-group">
                            <label for="message">Your Message</label>
                            <textarea id="message" class="form-control" placeholder="Enter your message"></textarea>
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
                <div class="footer-column">
                    <h3>kings Restaurant</h3>
                    <p>Authentic South Indian cuisine crafted with traditional recipes</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-whatsapp"></i></a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#menu">Menu</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Contact Info</h3>
                    <ul class="footer-links">
                        <li><i class="fas fa-map-marker-alt"></i>Bangaluru Highway,Anna Nager, Chennai, TN 600001</li>
                        <li><i class="fas fa-phone"></i> +91 98553 69524</li>
                        <li><i class="fas fa-envelope"></i> info@kingsrestaurant.com</li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2025 kings Restaurant. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

</body>
</html>

OUTPUT:

![alt text](<WhatsApp Image 2025-11-13 at 22.42.13_85fe4e8f.jpg>)
![alt text](<WhatsApp Image 2025-11-13 at 22.42.07_b1d422c0.jpg>)
![alt text](<WhatsApp Image 2025-11-13 at 22.42.11_3e0d37eb.jpg>)
![alt text](<WhatsApp Image 2025-11-13 at 22.42.06_0583a43b.jpg>)

RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
