<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AutoMasters - Premium Car Sales</title>
    <style>
        /* Global Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header Styles */
        header {
            background-color: #1a1a1a;
            color: white;
            padding: 20px 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 28px;
            font-weight: bold;
            color: #ff6b00;
        }
        
        .logo span {
            color: white;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: #ff6b00;
        }
        
        /* Hero Section */
        .hero {
            background-image: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1494976388531-d1058494cdd8?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 500px;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
        }
        
        .btn {
            display: inline-block;
            background-color: #ff6b00;
            color: white;
            padding: 12px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #e05d00;
        }
        
        /* Featured Cars */
        .featured {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 36px;
            color: #1a1a1a;
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: #666;
            font-size: 18px;
        }
        
        .cars-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .car-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .car-card:hover {
            transform: translateY(-10px);
        }
        
        .car-img {
            height: 200px;
            overflow: hidden;
        }
        
        .car-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .car-card:hover .car-img img {
            transform: scale(1.1);
        }
        
        .car-info {
            padding: 20px;
        }
        
        .car-info h3 {
            font-size: 22px;
            margin-bottom: 10px;
        }
        
        .car-details {
            display: flex;
            justify-content: space-between;
            margin-bottom: 15px;
            color: #666;
        }
        
        .price {
            font-size: 20px;
            font-weight: bold;
            color: #ff6b00;
        }
        
        /* Services */
        .services {
            background-color: #1a1a1a;
            color: white;
            padding: 80px 0;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .service-card {
            text-align: center;
            padding: 30px 20px;
            background-color: #2a2a2a;
            border-radius: 8px;
            transition: transform 0.3s;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
        }
        
        .service-icon {
            font-size: 40px;
            color: #ff6b00;
            margin-bottom: 20px;
        }
        
        .service-card h3 {
            font-size: 22px;
            margin-bottom: 15px;
        }
        
        /* Testimonials */
        .testimonials {
            padding: 80px 0;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial-card {
            background-color: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 15px;
        }
        
        .author-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .author-info h4 {
            font-size: 18px;
            margin-bottom: 5px;
        }
        
        .author-info p {
            color: #666;
            font-size: 14px;
        }
        
        /* Footer */
        footer {
            background-color: #1a1a1a;
            color: white;
            padding: 50px 0 20px;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .footer-col h3 {
            font-size: 20px;
            margin-bottom: 20px;
            color: #ff6b00;
        }
        
        .footer-col ul {
            list-style: none;
        }
        
        .footer-col ul li {
            margin-bottom: 10px;
        }
        
        .footer-col ul li a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-col ul li a:hover {
            color: #ff6b00;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            color: white;
            font-size: 20px;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: #ff6b00;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #333;
            color: #999;
            font-size: 14px;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 20px;
            }
            
            nav ul li {
                margin: 0 10px;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 18px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">Auto<span>Masters</span></div>
            <nav>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Inventory</a></li>
                    <li><a href="#">Services</a></li>
                    <li><a href="#">Financing</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Find Your Dream Car Today</h1>
                <p>Browse our extensive collection of premium vehicles at unbeatable prices</p>
                <a href="#" class="btn">View Inventory</a>
            </div>
        </div>
    </section>

    <!-- Featured Cars -->
    <section class="featured">
        <div class="container">
            <div class="section-title">
                <h2>Featured Vehicles</h2>
                <p>Check out our latest arrivals</p>
            </div>
            <div class="cars-grid">
                <!-- Car 1 -->
                <div class="car-card">
                    <div class="car-img">
                        <img src="https://images.unsplash.com/photo-1541899481282-d53bffe3c35d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="BMW M5">
                    </div>
                    <div class="car-info">
                        <h3>2022 BMW M5 Competition</h3>
                        <div class="car-details">
                            <span>12,000 mi</span>
                            <span>Automatic</span>
                            <span>Sedan</span>
                        </div>
                        <div class="price">$89,999</div>
                        <a href="#" class="btn">View Details</a>
                    </div>
                </div>
                
                <!-- Car 2 -->
                <div class="car-card">
                    <div class="car-img">
                        <img src="https://images.unsplash.com/photo-1492144534655-ae79c964c9d7?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Ford Mustang">
                    </div>
                    <div class="car-info">
                        <h3>2021 Ford Mustang GT</h3>
                        <div class="car-details">
                            <span>8,500 mi</span>
                            <span>Manual</span>
                            <span>Coupe</span>
                        </div>
                        <div class="price">$42,500</div>
                        <a href="#" class="btn">View Details</a>
                    </div>
                </div>
                
                <!-- Car 3 -->
                <div class="car-card">
                    <div class="car-img">
                        <img src="https://images.unsplash.com/photo-1555215695-3004980ad54e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Audi Q7">
                    </div>
                    <div class="car-info">
                        <h3>2020 Audi Q7 Premium Plus</h3>
                        <div class="car-details">
                            <span>24,000 mi</span>
                            <span>Automatic</span>
                            <span>SUV</span>
                        </div>
                        <div class="price">$54,999</div>
                        <a href="#" class="btn">View Details</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services -->
    <section class="services">
        <div class="container">
            <div class="section-title">
                <h2>Our Services</h2>
                <p>We offer more than just great cars</p>
            </div>
            <div class="services-grid">
                <!-- Service 1 -->
                <div class="service-card">
                    <div class="service-icon">🚗</div>
                    <h3>Car Financing</h3>
                    <p>Competitive rates and flexible terms to get you behind the wheel faster</p>
                </div>
                
                <!-- Service 2 -->
                <div class="service-card">
                    <div class="service-icon">🔧</div>
                    <h3>Certified Pre-Owned</h3>
                    <p>Rigorous inspections and extended warranties for peace of mind</p>
                </div>
                
                <!-- Service 3 -->
                <div class="service-card">
                    <div class="service-icon">🔄</div>
                    <h3>Trade-In Appraisal</h3>
                    <p>Get top dollar for your current vehicle when you trade it in</p>
                </div>
                
                <!-- Service 4 -->
                <div class="service-card">
                    <div class="service-icon">🛡️</div>
                    <h3>Extended Warranties</h3>
                    <p>Comprehensive coverage plans to protect your investment</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>What Our Customers Say</h2>
                <p>Hear from people who've driven away happy</p>
            </div>
            <div class="testimonial-grid">
                <!-- Testimonial 1 -->
                <div class="testimonial-card">
                    <p class="testimonial-text">"AutoMasters made the car buying process so easy. They found exactly what I was looking for and at a great price. Highly recommend!"</p>
                    <div class="testimonial-author">
                        <div class="author-img">
                            <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Michael Johnson">
                        </div>
                        <div class="author-info">
                            <h4>Michael Johnson</h4>
                            <p>BMW M5 Owner</p>
                        </div>
                    </div>
                </div>
                
                <!-- Testimonial 2 -->
                <div class="testimonial-card">
                    <p class="testimonial-text">"The financing options were fantastic and the staff was incredibly knowledgeable. I drove off the lot in my dream car!"</p>
                    <div class="testimonial-author">
                        <div class="author-img">
                            <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Sarah Williams">
                        </div>
                        <div class="author-info">
                            <h4>Sarah Williams</h4>
                            <p>Audi Q7 Owner</p>
                        </div>
                    </div>
                </div>
                
                <!-- Testimonial 3 -->
                <div class="testimonial-card">
                    <p class="testimonial-text">"Best car buying experience I've ever had. No pressure, great selection, and they really cared about finding me the right vehicle."</p>
                    <div class="testimonial-author">
                        <div class="author-img">
                            <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="David Chen">
                        </div>
                        <div class="author-info">
                            <h4>David Chen</h4>
                            <p>Ford Mustang Owner</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <!-- Column 1 -->
                <div class="footer-col">
                    <h3>AutoMasters</h3>
                    <p>Your trusted partner for premium pre-owned vehicles since 2005.</p>
                    <div class="social-links">
                        <a href="#">📱</a>
                        <a href="#">📘</a>
                        <a href="#">📸</a>
                        <a href="#">🐦</a>
                    </div>
                </div>
                
                <!-- Column 2 -->
                <div class="footer-col">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#">Home</a></li>
                        <li><a href="#">Inventory</a></li>
                        <li><a href="#">Services</a></li>
                        <li><a href="#">Financing</a></li>
                        <li><a href="#">Contact</a></li>
                    </ul>
                </div>
                
                <!-- Column 3 -->
                <div class="footer-col">
                    <h3>Contact Us</h3>
                    <ul>
                        <li>123 Auto Plaza</li>
                        <li>Detroit, MI 48201</li>
                        <li>Phone: (555) 123-4567</li>
                        <li>Email: info@automasters.com</li>
                    </ul>
                </div>
                
                <!-- Column 4 -->
                <div class="footer-col">
                    <h3>Business Hours</h3>
                    <ul>
                        <li>Monday - Friday: 9am - 7pm</li>
                        <li>Saturday: 9am - 6pm</li>
                        <li>Sunday: 11am - 5pm</li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 AutoMasters. All Rights Reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>
