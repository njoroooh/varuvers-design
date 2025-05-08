# varuvers-design
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Varuvers Design - Contemporary Fashion Trends</title>
    <style>
        :root {
            --primary-color: #998d09; /* Vibrant orange */
            --secondary-color: #292929; /* Dark black */
            --accent-color: #FF9E1B; /* Lighter orange */
            --text-light: #F7F7F7;
            --text-dark: #333333;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Montserrat', sans-serif;
        }
        
        body {
            background-color: var(--secondary-color);
            color: var(--text-light);
        }
        
        header {
            background-color: var(--secondary-color);
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 3px solid var(--primary-color);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .logo-container {
            display: flex;
            align-items: center;
        }
        
        .logo {
            max-width: 150px;
            transition: transform 0.3s;
        }
        
        .logo:hover {
            transform: scale(1.05);
        }
        
        .logo-upload {
            margin-left: 20px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: var(--text-light);
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: color 0.3s;
            padding: 0.5rem 1rem;
            border-radius: 4px;
        }
        
        nav ul li a:hover {
            color: var(--primary-color);
            background-color: rgba(255, 107, 53, 0.1);
        }
        
        .hero {
            background: linear-gradient(rgba(41, 41, 41, 0.7), rgba(41, 41, 41, 0.7)), 
                        url('https://images.unsplash.com/photo-1483985988355-763728e1935b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 2rem;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            color: var(--primary-color);
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--primary-color);
            color: var(--text-light);
            padding: 0.8rem 1.8rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: var(--accent-color);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--primary-color);
            margin-left: 1rem;
        }
        
        .btn-outline:hover {
            background-color: var(--primary-color);
        }
        
        .section-title {
            text-align: center;
            margin: 4rem 0 2rem;
            font-size: 2.5rem;
            color: var(--primary-color);
        }
        
        .categories {
            padding: 0 2rem 4rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .category-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .category-card {
            background-color: var(--secondary-color);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s;
            border: 1px solid var(--primary-color);
        }
        
        .category-card:hover {
            transform: translateY(-10px);
        }
        
        .category-img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }
        
        .category-content {
            padding: 1.5rem;
        }
        
        .category-content h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: var(--primary-color);
        }
        
        .category-content p {
            margin-bottom: 1rem;
            color: var(--text-light);
            opacity: 0.8;
        }
        
        .subcategories {
            margin-top: 1rem;
        }
        
        .subcategories h4 {
            font-size: 1rem;
            margin-bottom: 0.5rem;
            color: var(--accent-color);
        }
        
        .subcategories ul {
            list-style: none;
            padding-left: 1rem;
        }
        
        .subcategories ul li {
            margin-bottom: 0.3rem;
            position: relative;
        }
        
        .subcategories ul li::before {
            content: "→";
            color: var(--primary-color);
            position: absolute;
            left: -1rem;
        }
        
        .testimonials {
            background-color: #1a1a1a;
            padding: 4rem 2rem;
        }
        
        .testimonial-container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .testimonial-card {
            background-color: var(--secondary-color);
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            border-left: 4px solid var(--primary-color);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 1rem;
            line-height: 1.6;
        }
        
        .testimonial-author {
            font-weight: 600;
            color: var(--primary-color);
        }
        
        .gallery {
            padding: 4rem 2rem;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 8px;
            height: 300px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .gallery-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .gallery-item:hover .gallery-img {
            transform: scale(1.1);
        }
        
        .gallery-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(0, 0, 0, 0.8), transparent);
            padding: 1rem;
            transform: translateY(100%);
            transition: transform 0.3s;
        }
        
        .gallery-item:hover .gallery-overlay {
            transform: translateY(0);
        }
        
        .gallery-overlay h3 {
            color: var(--primary-color);
            margin-bottom: 0.5rem;
        }
        
        footer {
            background-color: #1a1a1a;
            padding: 3rem 2rem;
            text-align: center;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            text-align: left;
        }
        
        .footer-column h3 {
            color: var(--primary-color);
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 0.8rem;
        }
        
        .footer-column ul li a {
            color: var(--text-light);
            text-decoration: none;
            transition: color 0.3s;
            opacity: 0.8;
        }
        
        .footer-column ul li a:hover {
            color: var(--primary-color);
            opacity: 1;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .social-links a {
            color: var(--text-light);
            font-size: 1.5rem;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: var(--primary-color);
        }
        
        .copyright {
            margin-top: 3rem;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            opacity: 0.7;
        }
        
        @media (max-width: 768px) {
            header {
                flex-direction: column;
                padding: 1rem;
            }
            
            .logo-container {
                margin-bottom: 1rem;
                flex-direction: column;
                align-items: center;
            }
            
            .logo-upload {
                margin-left: 0;
                margin-top: 10px;
            }
            
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0.5rem;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .btn {
                display: block;
                width: 100%;
                margin-bottom: 1rem;
            }
            
            .btn-outline {
                margin-left: 0;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <header>
        <div class="logo-container">
            <img src="https://via.placeholder.com/150x50?text=Varuvers+Design" alt="Varuvers Design Logo" class="logo" id="companyLogo">
            <div class="logo-upload">
                <input type="file" id="logoUpload" accept="image/*" style="display: none;">
                <button class="btn btn-outline" onclick="document.getElementById('logoUpload').click()">Change Logo</button>
            </div>
        </div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#categories">Categories</a></li>
                <li><a href="#gallery">Gallery</a></li>
                <li><a href="#testimonials">Testimonials</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section class="hero" id="home">
        <h1>Varuvers Design</h1>
        <p>Discover the latest fashion trends and elevate your style with our contemporary designs. From headwear to footwear, we've got you covered with the most up-to-date fashion pieces.</p>
        <div>
            <a href="#categories" class="btn">Explore Collections</a>
            <a href="#contact" class="btn btn-outline">Contact Us</a>
        </div>
    </section>

    <section class="categories" id="categories">
        <h2 class="section-title">Our Fashion Categories</h2>
        <div class="category-grid">
            <!-- Headwear Category -->
            <div class="category-card">
                <img src="https://i.pinimg.com/736x/a5/0f/e6/a50fe67ca2495b5d5404fd916501bda5.jpg" alt="Headwear" class="category-img">
                <div class="category-content">
                    <h3>Headwear</h3>
                    <p>Complete your look with our stylish headwear collection.</p>
                    <div class="subcategories">
                        <h4>Subcategories:</h4>
                        <ul>
                            <li>Hats</li>
                            <li>Caps</li>
                            <li>Beanies</li>
                            <li>Headbands</li>
                        </ul>
                    </div>
                </div>
            </div>
            
            <!-- Footwear Category -->
            <div class="category-card">
                <img src="https://i.pinimg.com/736x/27/69/34/2769346f88f52c75bfe17064b76d0b2f.jpg" alt="Footwear" class="category-img">
                <div class="category-content">
                    <h3>Footwear</h3>
                    <p>Step out in style with our premium footwear collection.</p>
                    <div class="subcategories">
                        <h4>Subcategories:</h4>
                        <ul>
                            <li>Heels</li>
                            <li>Sneakers</li>
                            <li>Boots</li>
                            <li>Sandals</li>
                        </ul>
                    </div>
                </div>
            </div>
            
            <!-- Accessories Category -->
            <div class="category-card">
                <img src="https://i.pinimg.com/736x/67/76/b2/6776b2edc1b044b8131607b2227b211d.jpg
                " alt="Accessories" class="category-img">
                <div class="category-content">
                    <h3>Accessories</h3>
                    <p>Elevate your style with our exquisite accessories.</p>
                    <div class="subcategories">
                        <h4>Subcategories:</h4>
                        <ul>
                            <li>Chains
                                <ul>
                                    <li>Jerseys</li>
                                    <li>Gold</li>
                                    <li>Silver</li>
                                </ul>
                            </li>
                            <li>Watches</li>
                            <li>Bracelets</li>
                            <li>Rings</li>
                        </ul>
                    </div>
                </div>
            </div>
            
            <!-- Apparel Category -->
            <div class="category-card">
                <img src="https://i.pinimg.com/736x/c8/66/9c/c8669c50fd325d0485cf1384ce25b08c.jpg" alt="Apparel" class="category-img">
                <div class="category-content">
                    <h3>Apparel</h3>
                    <p>Discover our trendy clothing collection for all occasions.</p>
                    <div class="subcategories">
                        <h4>Subcategories:</h4>
                        <ul>
                            <li>T-Shirts</li>
                            <li>Dresses</li>
                            <li>Jackets</li>
                            <li>Jeans</li>
                        </ul>
                    </div>
                </div>
            </div>
            
            <!-- Bags Category -->
            <div class="category-card">
                <img src="https://images.unsplash.com/photo-1590874103328-eac38a683ce7?ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80" alt="Bags" class="category-img">
                <div class="category-content">
                    <h3>Bags</h3>
                    <p>Carry your essentials in style with our designer bags.</p>
                    <div class="subcategories">
                        <h4>Subcategories:</h4>
                        <ul>
                            <li>Handbags</li>
                            <li>Backpacks</li>
                            <li>Clutches</li>
                            <li>Totes</li>
                        </ul>
                    </div>
                </div>
            </div>
            
            <!-- Jewelry Category -->
            <div class="category-card">
                <img src="https://i.pinimg.com/736x/25/d6/e4/25d6e4a2644188a55e1678a186f20f88.jpg" alt="Jewelry" class="category-img">
                <div class="category-content">
                    <h3>Jewelry</h3>
                    <p>Adorn yourself with our stunning jewelry pieces.</p>
                    <div class="subcategories">
                        <h4>Subcategories:</h4>
                        <ul>
                            <li>Necklaces</li>
                            <li>Earrings</li>
                            <li>Bangles</li>
                            <li>Brooches</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="gallery" id="gallery">
        <h2 class="section-title">Fashion Gallery</h2>
        <div class="gallery-grid">
            <div class="gallery-item">
                <img src="https://i.pinimg.com/736x/93/86/6c/93866c25dbc4e3a62b4ee18500c45c99.jpg" alt="Fashion 1" class="gallery-img">
                <div class="gallery-overlay">
                    <h3>Urban Streetwear</h3>
                    <p>Latest street fashion trends</p>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://i.pinimg.com/736x/e5/9b/1a/e59b1ac93ab128b08d1c3b0156336f19.jpg" alt="Fashion 2" class="gallery-img">
                <div class="gallery-overlay">
                    <h3>Casual Elegance</h3>
                    <p>Comfort meets style</p>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://i.pinimg.com/736x/47/89/db/4789db4a41c8151c6114a4ddef783cc9.jpg" alt="Fashion 3" class="gallery-img">
                <div class="gallery-overlay">
                    <h3>Luxury Accessories</h3>
                    <p>Premium quality materials</p>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://i.pinimg.com/736x/00/51/51/00515146b714606b0d2686df382ffb0e.jpg" alt="Fashion 4" class="gallery-img">
                <div class="gallery-overlay">
                    <h3>Summer Collection</h3>
                    <p>Light and breezy styles</p>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://i.pinimg.com/736x/c5/e5/6b/c5e56b1c97dd3f3ca55780ff9f5860ec.jpg" alt="Fashion 5" class="gallery-img">
                <div class="gallery-overlay">
                    <h3>Formal Attire</h3>
                    <p>Sophisticated designs</p>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://i.pinimg.com/736x/63/8f/b8/638fb8f935378d05fa86448a845b3991.jpg" alt="Fashion 6" class="gallery-img">
                <div class="gallery-overlay">
                    <h3>Winter Collection</h3>
                    <p>Warm and stylish</p>
                </div>
            </div>
        </div>
    </section>

    <section class="testimonials" id="testimonials">
        <div class="testimonial-container">
            <h2 class="section-title">Client Testimonials</h2>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <p class="testimonial-text">"Varuvers Design completely transformed my wardrobe. Their attention to detail and contemporary designs are unmatched in the industry."</p>
                    <p class="testimonial-author">- Triza Wairimu</p>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">"I've been a loyal customer for years. Their footwear collection is not only stylish but incredibly comfortable for all-day wear."</p>
                    <p class="testimonial-author">- Sarah Njeri</p>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">"The quality of materials and craftsmanship in their accessories line is exceptional. I receive compliments every time I wear their pieces."</p>
                    <p class="testimonial-author">- Paul Kamande</p>
                </div>
            </div>
        </div>
    </section>

    <footer id="contact">
        <div class="footer-content">
            <div class="footer-column">
                <h3>About Varuvers</h3>
                <p>Varuvers Design is a contemporary fashion house dedicated to creating up-to-date fashion trends with exceptional quality and style.</p>
                <div class="social-links">
                    <a href="https://www.instagram.com/varuvers?igsh=MTJwd3B4cG9hNTlnYQ==" target="_blank"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-facebook"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-pinterest"></i></a>
                </div>
            </div>
            <div class="footer-column">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#categories">Categories</a></li>
                    <li><a href="#gallery">Gallery</a></li>
                    <li><a href="#testimonials">Testimonials</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Contact Us</h3>
                <ul>
                    <li><i class="fas fa-phone"></i> 0700926815</li>
                    <li><i class="fas fa-envelope"></i> info@varuversdesign.org</li>
                    <li><i class="fas fa-globe"></i> varuversdesign.org</li>
                    <li><i class="fas fa-map-marker-alt"></i> Nairobi, Kenya</li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Newsletter</h3>
                <p>Subscribe to get updates on our latest collections and exclusive offers.</p>
                <form>
                    <input type="email" placeholder="Your email address" style="width: 100%; padding: 0.8rem; margin-bottom: 1rem; border-radius: 4px; border: none;">
                    <button type="submit" class="btn">Subscribe</button>
                </form>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2023 Varuvers Design. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Logo upload functionality
        document.getElementById('logoUpload').addEventListener('change', function(e) {
            const file = e.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(event) {
                    document.getElementById('companyLogo').src = event.target.result;
                };
                reader.readAsDataURL(file);
            }
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
    </script>
</body>
</html>
