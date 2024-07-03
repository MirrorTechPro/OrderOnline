<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MirrorTech Pro</title>
    <link rel="stylesheet" href="styles.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
</head>
<body>
    <header>
        <div class="container">
            <h1>MirrorTech Pro</h1>
            <p class="slogan">Transform your reflection, Elevate your life.</p>
        </div>
    </header>
    
    <section class="product-info">
        <div class="container">
            <h2>About MirrorTech Pro</h2>
            <div class="carousel">
                <img src="mirror-tech-pro-1.jpg" alt="MirrorTech Pro - Front View" class="carousel-image active">
                <img src="mirror-tech-pro-2.jpg" alt="MirrorTech Pro - Side View" class="carousel-image">
                <img src="mirror-tech-pro-3.jpg" alt="MirrorTech Pro - In Use" class="carousel-image">
                <div class="carousel-controls">
                    <button class="prev">&#10094;</button>
                    <button class="next">&#10095;</button>
                </div>
            </div>
            <p>The MirrorTech Pro is your ultimate companion for fashion and fitness. This innovative smart mirror helps you visualize outfits with stunning clarity and provides personalized gym courses to enhance your workout experience. Elevate your style and fitness routine effortlessly with the MirrorTech Pro.</p>
            <p class="price">Price: 1200 RM</p>
            <a href="#order-form" class="order-button">Order Now</a>
        </div>
    </section>

    <section class="features">
        <div class="container">
            <h2>Features</h2>
            <div class="feature-list">
                <div class="feature">
                    <img src="feature-outfit.png" alt="Outfit Visualization">
                    <h3>Outfit Visualization</h3>
                    <p>Try out new outfits and see how they look in real-time.</p>
                </div>
                <div class="feature">
                    <img src="feature-workout.png" alt="Personalized Gym Courses">
                    <h3>Personalized Gym Courses</h3>
                    <p>Access tailored workout routines and track your fitness progress.</p>
                </div>
                <div class="feature">
                    <img src="feature-display.png" alt="Interactive Display">
                    <h3>Interactive Display</h3>
                    <p>High-resolution display that integrates seamlessly with your home.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="reviews">
        <div class="container">
            <h2>Customer Reviews</h2>
            <div class="review-list">
                <div class="review">
                    <p>"Absolutely love the MirrorTech Pro! It has completely transformed my morning routine." - Sarah L.</p>
                </div>
                <div class="review">
                    <p>"The personalized gym courses are a game-changer for my fitness journey!" - John M.</p>
                </div>
                <div class="review">
                    <p>"Stylish and functional, it's a must-have for anyone who cares about their appearance." - Emily R.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="order-form" class="order-form">
        <div class="container">
            <h2>Order Your MirrorTech Pro</h2>
            <form id="orderForm">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>

                <label for="address">Shipping Address:</label>
                <textarea id="address" name="address" required></textarea>

                <label for="quantity">Quantity:</label>
                <input type="number" id="quantity" name="quantity" min="1" value="1" required>

                <button type="submit">Submit Order</button>
            </form>
        </div>
    </section>

    <section class="contact">
        <div class="container">
            <h2>Contact Us</h2>
            <form id="contactForm">
                <label for="contact-name">Name:</label>
                <input type="text" id="contact-name" name="contact-name" required>

                <label for="contact-email">Email:</label>
                <input type="email" id="contact-email" name="contact-email" required>

                <label for="message">Message:</label>
                <textarea id="message" name="message" required></textarea>

                <button type="submit">Send Message</button>
            </form>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2024 MirrorTech. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        // Carousel functionality
        let currentIndex = 0;
        const images = document.querySelectorAll('.carousel-image');
        const prev = document.querySelector('.prev');
        const next = document.querySelector('.next');

        function showImage(index) {
            images[currentIndex].classList.remove('active');
            currentIndex = (index + images.length) % images.length;
            images[currentIndex].classList.add('active');
        }

        prev.addEventListener('click', () => showImage(currentIndex - 1));
        next.addEventListener('click', () => showImage(currentIndex + 1));

        // Form functionality
        document.getElementById('orderForm').addEventListener('submit', function(event) {
            event.preventDefault();
            alert('Thank you for your order! We will contact you soon.');
            document.getElementById('orderForm').reset();
        });

        document.getElementById('contactForm').addEventListener('submit', function(event) {
            event.preventDefault();
            alert('Your message has been sent! We will get back to you soon.');
            document.getElementById('contactForm').reset();
        });
    </script>
</body>
</html>
