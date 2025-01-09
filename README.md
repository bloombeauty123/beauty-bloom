<!DOCTYPE html>
<html>
<head>
    <title>Skin Care Product</title>
    <style>
        body {
            font-family: 'Verdana', sans-serif;
            margin: 0;
            padding: 0;
            background-color: pink;
            color: #333;
        }

        header {
            background-color: tan;
            color: black;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center; 
            text-align: center; 
        }

        .logo-container {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 10px;
        }

        .logo-container .logo {
            width: 120px;
            height: auto;
            margin-right: 20px;
        }

        header h1 {
            margin: 0;
            text-align: center;
        }

        header p {
            margin-top: 10px;
            font-style: italic;
        }

        nav {
            background-color: pink;
            padding: 10px;
            text-align: center;
        }

        nav a {
            margin: 0 15px;
            text-decoration: none;
            color: solid black;
            font-size: 1em;
        }

        nav a:hover {
            text-decoration: underline;
        }

        .hero {
            background:linear-gradient(45deg, #ffebe0, #fff5f2);;
            text-align: center;
            padding: 60px 20px;
			color:solid black
        }

        .hero h1 {
            font-size: 2em;
            margin: 0;
        }

        .hero p {
            font-size: 1.2em;
            margin: 20px 0 0;
        }

        section {
            padding: 20px;
        }

        .products {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .product-card {
            background-color: white;
            border: 1px solid black;
            border-radius: 9px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            text-align: center;
            padding: 15px;
        }

        .product-card img {
            width: 50%;
            height: auto;
        }

        .product-card h3 {
            margin: 10px 0 5px;
            font-size: 1.2em;
            color: black;
        }

        .product-card p {
            font-size: 0.95em;
            color: black;
        }

        .product-card button {
            margin-top: 10px;
            padding: 10px 15px;
            background-color: black;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .product-card button:hover {
            background-color: pink;
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 15px;
            font-size: 0.9em;
        }

        /* Cart and Checkout Styles */
        .cart {
            margin-top: 20px;
            border: 1px solid #ccc;
            padding: 20px;
            border-radius: 5px;
            display: none;
        }

        .cart-items {
            list-style: none;
            padding: 0;
        }

        .cart-items li {
            margin: 10px 0;
        }

        .button {
            display: inline-block;
            margin: 10px 5px;
            padding: 10px 15px;
            background-color: #28a745;
            color: #fff;
            text-decoration: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .button:hover {
            background-color: #218838;
        }

        .buy-section {
            display: none;
        }

        .buy-section input {
            margin: 10px 0;
            width: 100%;
            padding: 10px;
        }
    </style>
</head>
<body>
    <header>
        <div class="logo-container">
            <img src="abc.png" alt="Company Logo" class="logo"> <!-- Add your logo image -->
        </div>
        <h1>BLOOM BEAUTY</h1>
        <p>Unlock your natural radiance!</p>
    </header>

    <nav>
        <b>
            <a href="#about">About</a>
            <a href="#products">Our Products</a>
            <a href="#contact">Contact</a>
        </b>
    </nav>

    <section class="hero">
        <h1>Self-love Journey</h1>
        <p> Hello Everyone! Welcome to Bloom Beauty. Let's transform your skincare routine with Bloom Beauty's natural and effective products.</p>
    </section>

    <section id="about">
        <h2>About Bloom Beauty</h2>
        <p>At Bloom Beauty, we are dedicated to creating skincare solutions that are as unique as you are. Our products blend natural ingredients with the latest innovations to ensure healthy and glowing skin.</p>
    </section>

    <section id="products">
        <h2>Our Bestsellers</h2>
        <div class="products">
            <!-- Product Cards -->
            <!-- Example Product Card -->
            <div class="product-card">
                <img src="download.JPEG" alt="Golden Pearl Skin Serum">
                <h3>Golden Pearl Skin Serum</h3>
                <p>Rejuvenate your skin with Skin Serum.</p>
                <button onclick="addToCart('Golden Pearl Skin Serum', 750)">Add to Cart</button>
                <button onclick="buyNow()">Buy Now</button>
            </div>
			<div class="product-card">
                <img src="cleasner.WEBP" alt="Garnier Vitamin C Serum">
                <h3>Trego Facial cleasner</h3>
                <p>Anti-acne Cleanser "No Acne,No problems".</p>
                <button onclick="addToCart('Garnier Vitamin C Serum', 400)">Add to Cart</button>
                <button onclick="buyNow()">Buy Now</button>
            </div>
			 <div class="product-card">
                <img src="sunscreen.JPEG" alt="Garnier Vitamin C Serum">
                <h3>BN sunscreen</h3>
                <p> Burn less, live more.</p>
                <button onclick="addToCart('Garnier Vitamin C Serum', 300)">Add to Cart</button>
                <button onclick="buyNow()">Buy Now</button>
            </div>
			 <div class="product-card">
                <img src="luxx.JPG" alt="Garnier Vitamin C Serum">
                <h3>Lux boby scrub  </h3>
                <p>Exudes fragrance notes of praline, amber.</p>
                <button onclick="addToCart('Garnier Vitamin C Serum', 540)">Add to Cart</button>
                <button onclick="buyNow()">Buy Now</button>
            </div>
			 <div class="product-card">
                <img src="olay.WEBP" alt="Garnier Vitamin C Serum">
                <h3> Olay nourshing cream </h3>
                <p>Even skin tone.</p>
                <button onclick="addToCart('Garnier Vitamin C Serum', 740)">Add to Cart</button>
                <button onclick="buyNow()">Buy Now</button>
            </div>
			 <div class="product-card">
                <img src="images.JPEG" alt="Garnier Vitamin C Serum">
                <h3>Garnier Softening Toner</h3>
                <p>Remove Dark Spots And Rivives Dull Skin</p>
                <button onclick="addToCart('Garnier Vitamin C Serum', 700)">Add to Cart</button>
                <button onclick="buyNow()">Buy Now</button>
            </div>
			 <div class="product-card">
                <img src="golden.WEBP" alt="Garnier Vitamin C Serum">
                <h3> Skin Serum</h3>
                <p>Rejuvenate your skin with the Skin Serum.</p>
                <button onclick="addToCart('Garnier Vitamin C Serum', 450)">Add to Cart</button>
                <button onclick="buyNow()">Buy Now</button>
            </div>
			<div class="product-card">
                <img src="men.JPEG" alt="Garnier Vitamin C Serum">
                <h3>Mark 30 Men's Face wash</h3>
                <p> Getting clear skin is not impossible</p>
                <button onclick="addToCart('Garnier Vitamin C Serum', 500)">Add to Cart</button>
                <button onclick="buyNow()">Buy Now</button>
            </div>
			<div class="product-card">
                <img src="face wash.JPEG" alt="Garnier Vitamin C Serum">
                <h3>Face Wash</h3>
                <p>The secrect To Clear Skin.</p>
                <button onclick="addToCart('Garnier Vitamin C Serum', 400)">Add to Cart</button>
                <button onclick="buyNow()">Buy Now</button>
            </div>
        </div>
    </section>

    <div class="cart" id="cart">
        <h2>Shopping Cart</h2>
        <ul class="cart-items" id="cartItems"></ul>
        <p>Total: RS.<span id="cartTotal">0</span></p>
        <button class="button" onclick="proceedToCheckout()">Proceed to Checkout</button>
    </div>

    <div class="buy-section" id="buySection">
        <h2>Checkout</h2>
        <form id="checkoutForm">
            <input type="text" placeholder="Your Name" required />
            <input type="email" placeholder="Your Email" required />
            <input type="text" placeholder="Shipping Address" required />
            <button type="submit" class="button">Place Order</button>
        </form>
    </div>

    <section id="contact">
        <h2>Contact Us</h2>
        <p>Have questions or need support? Reach us:</p>
        <p>Email: aroomamujtaba10@gmail.com</p>
        <p>Phone: <a href="tel:+923306764506">+92 330 6764506</a></p>
        <p>Direct Order on WhatsApp: 
            <a href="https://wa.me/923306764506" target="_blank">
                <button class="button">Place Order on WhatsApp</button>
            </a>
        </p>
    </section>

    <footer>
        <p>&copy; 2025 Bloom Beauty. Crafted for your glow, naturally.</p>
    </footer>

    <script>
        let cart = [];
        let total = 0;

        function addToCart(productName, price) {
            cart.push({ name: productName, price: price });
            total += price;
            updateCart();
        }

        function updateCart() {
            const cartElement = document.getElementById('cart');
            const cartItemsElement = document.getElementById('cartItems');
            const cartTotalElement = document.getElementById('cartTotal');
            cartElement.style.display = 'block';
            cartTotalElement.textContent = total;
        }

        function buyNow() {
            window.location.href = 'https://wa.me/923306764506?text=I%20would%20like%20to%20order%20products%20from%20Bloom%20Beauty.';
        }

        function proceedToCheckout() {
            document.getElementById('buySection').style.display = 'block';
        }

        const checkoutForm = document.getElementById('checkoutForm');
        checkoutForm.addEventListener('submit', function (e) {
            e.preventDefault();
            alert('Order placed successfully!');
            cart = [];
            total = 0;
            updateCart();
            document.getElementById('cart').style.display = 'none';
            document.getElementById('buySection').style.display = 'none';
        });
    </script>
</body>
</html>
