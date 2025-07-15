<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Asai Traders - Premium Idli Dosa Mix</title>
    <style>
        /* Basic CSS for a clean and appealing look */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f8f8;
            color: #333;
            line-height: 1.6;
        }
        header {
            background-color: #4CAF50; /* A pleasant green */
            color: #fff;
            padding: 1.5rem 0;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
            position: relative; /* Needed for cart icon positioning */
        }
        header h1 {
            margin: 0;
            font-size: 2.8em;
            letter-spacing: 1px;
        }
        header p {
            font-size: 1.1em;
            margin-top: 5px;
        }
        nav {
            background-color: #388E3C; /* Darker green */
            padding: 0.7rem 0;
            text-align: center;
        }
        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        nav ul li {
            display: inline;
            margin: 0 25px;
        }
        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.05em;
            transition: color 0.3s ease;
        }
        nav ul li a:hover {
            color: #DCEDC8; /* Lighter green on hover */
        }
        .container {
            width: 85%;
            max-width: 1200px;
            margin: 30px auto;
            padding: 25px;
            background-color: #fff;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }
        h2 {
            color: #4CAF50;
            text-align: center;
            margin-bottom: 25px;
            font-size: 2em;
        }
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 20px;
        }
        .product-item {
            border: 1px solid #e0e0e0;
            padding: 20px;
            text-align: center;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease;
        }
        .product-item:hover {
            transform: translateY(-5px);
        }
        .product-item img {
            max-width: 100%;
            height: 200px; /* Fixed height for consistency */
            object-fit: contain; /* Ensure image fits without distortion */
            margin-bottom: 15px;
            border-radius: 5px;
        }
        .product-item h3 {
            font-size: 1.5em;
            color: #333;
            margin-bottom: 10px;
        }
        .product-item p {
            font-size: 1em;
            color: #555;
            margin-bottom: 15px;
        }
        .product-item .price {
            font-size: 1.6em;
            font-weight: bold;
            color: #E65100; /* Orange for price */
            margin-bottom: 15px;
            display: block;
        }
        .product-item button {
            background-color: #FF9800; /* Orange button */
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1.1em;
            transition: background-color 0.3s ease;
        }
        .product-item button:hover {
            background-color: #FB8C00;
        }
        .section-content {
            padding: 20px 0;
            text-align: justify;
        }
        .section-content p {
            margin-bottom: 15px;
        }
        hr {
            border: 0;
            height: 1px;
            background-image: linear-gradient(to right, rgba(0, 0, 0, 0), rgba(76, 175, 80, 0.75), rgba(0, 0, 0, 0));
            margin: 40px 0;
        }
        form {
            max-width: 600px;
            margin: 20px auto;
            padding: 20px;
            border: 1px solid #ddd;
            border-radius: 8px;
            background-color: #f9f9f9;
        }
        form label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #555;
        }
        form input[type="text"],
        form input[type="email"],
        form textarea {
            width: calc(100% - 20px);
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 1em;
        }
        form textarea {
            resize: vertical;
            min-height: 100px;
        }
        form input[type="submit"] {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1.1em;
            transition: background-color 0.3s ease;
        }
        form input[type="submit"]:hover {
            background-color: #388E3C;
        }
        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 1.5rem 0;
            margin-top: 40px;
            font-size: 0.9em;
        }

        /* Cart Specific Styles */
        .cart-icon {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 2em;
            color: white;
            cursor: pointer;
            text-decoration: none;
        }
        .cart-count {
            background-color: #FF0000;
            color: white;
            border-radius: 50%;
            padding: 2px 7px;
            font-size: 0.6em;
            position: absolute;
            top: 0px;
            right: -5px;
        }
        #cart {
            display: none; /* Hidden by default */
            position: fixed;
            top: 0;
            right: 0;
            width: 350px;
            height: 100%;
            background-color: #fefefe;
            box-shadow: -5px 0 15px rgba(0,0,0,0.2);
            z-index: 1000;
            overflow-y: auto;
            padding: 20px;
            box-sizing: border-box;
        }
        #cart.open {
            display: block; /* Show when open */
        }
        #cart h2 {
            margin-top: 0;
            border-bottom: 2px solid #eee;
            padding-bottom: 10px;
        }
        #cart-items {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        #cart-items li {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 0;
            border-bottom: 1px dotted #eee;
            font-size: 0.95em;
        }
        #cart-items li:last-child {
            border-bottom: none;
        }
        .remove-item {
            background-color: #f44336;
            color: white;
            border: none;
            padding: 5px 10px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 0.8em;
            margin-left: 10px;
        }
        .cart-total {
            text-align: right;
            font-size: 1.2em;
            font-weight: bold;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 2px solid #eee;
        }
        .close-cart {
            position: absolute;
            top: 10px;
            right: 15px;
            font-size: 2em;
            color: #aaa;
            cursor: pointer;
        }
        .checkout-button {
            display: block;
            width: 100%;
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 15px;
            margin-top: 20px;
            border-radius: 5px;
            font-size: 1.2em;
            cursor: pointer;
            text-align: center;
            transition: background-color 0.3s ease;
        }
        .checkout-button:hover {
            background-color: #388E3C;
        }
    </style>
</head>
<body>
    <header>
        <h1>Asai Traders</h1>
        <p>Your Source for Premium Idli Dosa Mix - Authentic Taste, Effortless Cooking!</p>
        <a href="#" class="cart-icon" id="openCart">🛒<span class="cart-count" id="cartCount">0</span></a>
    </header>

    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#products">Our Mixes</a></li>
            <li><a href="#benefits">Why Choose Us?</a></li>
            <li><a href="#about">About Asai Traders</a></li>
            <li><a href="#contact">Contact Us</a></li>
        </ul>
    </nav>

    <div class="container">
        <section id="home" class="section-content">
            <h2>Welcome to Asai Traders!</h2>
            <p>At **Asai Traders**, we bring the authentic taste of South India right to your kitchen with our premium **Idli Dosa Mix**. Say goodbye to soaking and grinding, and say hello to soft idlis and crispy dosas in minutes!</p>
            <p>Our carefully crafted mixes are made from the finest ingredients, ensuring a perfect fermentation every time. Whether you're a seasoned chef or a beginner, our mixes make preparing your favorite South Indian breakfast a breeze.</p>
        </section>

        <hr>

        <section id="products">
            <h2>Our Premium Idli Dosa Mixes</h2>
            <div class="product-grid">
                <div class="product-item" data-product-id="1" data-product-name="Classic Idli Dosa Mix - 1 KG" data-price="50.00">
                    <img src="https://via.placeholder.com/200x200/4CAF50/FFFFFF?text=Idli+Dosa+Mix+1KG" alt="Idli Dosa Mix 1kg Pack">
                    <h3>Classic Idli Dosa Mix - 1 KG</h3>
                    <p>Perfect for everyday use. Makes fluffy idlis and crisp golden dosas. Just add water!</p>
                    <span class="price">₹50.00</span>
                    <button class="add-to-cart">Add to Cart</button>
                </div>

                <div class="product-item" data-product-id="2" data-product-name="Classic Idli Dosa Mix - 500 G" data-price="25.00">
                    <img src="https://via.placeholder.com/200x200/4CAF50/FFFFFF?text=Idli+Dosa+Mix+500G" alt="Idli Dosa Mix 500g Pack">
                    <h3>Classic Idli Dosa Mix - 500 G</h3>
                    <p>A convenient pack size for smaller families or for trying out our delicious mix.</p>
                    <span class="price">₹25.00</span>
                    <button class="add-to-cart">Add to Cart</button>
                </div>

                <div class="product-item" data-product-id="3" data-product-name="Whole Grain Idli Dosa Mix - 250 G" data-price="15.00">
                    <img src="https://via.placeholder.com/200x200/4CAF50/FFFFFF?text=Whole+Grain+Mix+250G" alt="Whole Grain Idli Dosa Mix 250g">
                    <h3>Whole Grain Idli Dosa Mix - 250 G</h3>
                    <p>For a healthier option without compromising on taste. Rich in fiber and nutrients.</p>
                    <span class="price">₹15.00</span>
                    <button class="add-to-cart">Add to Cart</button>
                </div>

                </div>
        </section>

        <hr>

        <section id="benefits" class="section-content">
            <h2>Why Choose Asai Traders Idli Dosa Mix?</h2>
            <ul>
                <li>**Authentic Taste:** Our mixes capture the traditional South Indian flavor you love.</li>
                <li>**Premium Ingredients:** Made from carefully selected, high-quality lentils and rice.</li>
                <li>**Convenience:** Save time and effort with our easy-to-use, ready-to-mix batter.</li>
                <li>**Consistency:** Enjoy perfectly fermented batter every single time.</li>
                <li>**Hygienically Packed:** Produced and packed with the utmost care to ensure freshness and safety.</li>
            </ul>
        </section>

        <hr>

        <section id="about" class="section-content">
            <h2>About Asai Traders</h2>
            <p>Established with a passion for bringing authentic South Indian culinary experiences to every home, **Asai Traders** is a trusted name in high-quality food products. Located in **Coimbatore, Tamil Nadu, India**, we specialize in producing premium **Idli Dosa Mix** that guarantees both convenience and taste.</p>
            <p>Our commitment lies in providing products that are not only delicious but also meet the highest standards of quality and hygiene. We believe that everyone should be able to enjoy healthy and traditional meals without the hassle. Asai Traders is more than just a business; it's a dedication to culinary excellence.</p>
        </section>

        <hr>

        <section id="contact" class="section-content">
            <h2>Get in Touch with Asai Traders</h2>
            <p style="text-align: center;">Have a question about our Idli Dosa mix or need bulk orders? We'd love to hear from you!</p>
            <p style="text-align: center;"><strong>Email:</strong> <a href="mailto:info@asaitraders.com">info@asaitraders.com</a></p>
            <p style="text-align: center;"><strong>Phone:</strong> +91 98765 43210</p>
            <p style="text-align: center;"><strong>Address:</strong> [Your Shop Address/Office Address Here], Coimbatore, Tamil Nadu, India</p>

            <form action="#" method="POST">
                <label for="name">Your Name:</label>
                <input type="text" id="name" name="name" required>

                <label for="email">Your Email:</label>
                <input type="email" id="email" name="email" required>

                <label for="subject">Subject:</label>
                <input type="text" id="subject" name="subject">

                <label for="message">Your Message:</label>
                <textarea id="message" name="message" rows="6" required></textarea>

                <input type="submit" value="Send Message">
            </form>
        </section>
    </div>

    <footer>
        <p>&copy; 2025 Asai Traders. All rights reserved. Made with love in Coimbatore, Tamil Nadu.</p>
    </footer>

    <div id="cart">
        <span class="close-cart" id="closeCart">&times;</span>
        <h2>Your Cart</h2>
        <ul id="cart-items">
            </ul>
        <div class="cart-total">
            Total: <span id="cartTotal">₹0.00</span>
        </div>
        <button class="checkout-button" onclick="alert('Proceeding to checkout (this is a demo feature)')">Proceed to Checkout</button>
    </div>

    <script>
        const cart = []; // Array to store cart items
        const cartCountSpan = document.getElementById('cartCount');
        const cartItemsList = document.getElementById('cart-items');
        const cartTotalSpan = document.getElementById('cartTotal');
        const openCartBtn = document.getElementById('openCart');
        const closeCartBtn = document.getElementById('closeCart');
        const cartSidebar = document.getElementById('cart');

        // Function to update cart display
        function updateCart() {
            cartItemsList.innerHTML = ''; // Clear current cart display
            let total = 0;

            cart.forEach(item => {
                const li = document.createElement('li');
                li.innerHTML = `
                    <span>${item.name} (${item.quantity})</span>
                    <span>₹${(item.price * item.quantity).toFixed(2)}</span>
                    <button class="remove-item" data-product-id="${item.id}">Remove</button>
                `;
                cartItemsList.appendChild(li);
                total += item.price * item.quantity;
            });

            cartTotalSpan.textContent = `₹${total.toFixed(2)}`;
            cartCountSpan.textContent = cart.reduce((sum, item) => sum + item.quantity, 0); // Update total item count

            // Add event listeners for remove buttons
            document.querySelectorAll('.remove-item').forEach(button => {
                button.addEventListener('click', (event) => {
                    const productId = parseInt(event.target.dataset.productId);
                    removeItemFromCart(productId);
                });
            });
        }

        // Function to add item to cart
        function addItemToCart(productId, productName, price) {
            const existingItem = cart.find(item => item.id === productId);

            if (existingItem) {
                existingItem.quantity++;
            } else {
                cart.push({ id: productId, name: productName, price: price, quantity: 1 });
            }
            updateCart();
            openCart(); // Open cart automatically when an item is added
        }

        // Function to remove item from cart
        function removeItemFromCart(productId) {
            const itemIndex = cart.findIndex(item => item.id === productId);

            if (itemIndex > -1) {
                if (cart[itemIndex].quantity > 1) {
                    cart[itemIndex].quantity--;
                } else {
                    cart.splice(itemIndex, 1); // Remove item if quantity is 1
                }
            }
            updateCart();
        }

        // Open cart sidebar
        function openCart() {
            cartSidebar.classList.add('open');
        }

        // Close cart sidebar
        function closeCart() {
            cartSidebar.classList.remove('open');
        }

        // Event listeners for add to cart buttons
        document.querySelectorAll('.add-to-cart').forEach(button => {
            button.addEventListener('click', (event) => {
                const productItem = event.target.closest('.product-item');
                const productId = parseInt(productItem.dataset.productId);
                const productName = productItem.dataset.productName;
                const price = parseFloat(productItem.dataset.price);
                addItemToCart(productId, productName, price);
            });
        });

        // Event listeners for cart icon and close button
        openCartBtn.addEventListener('click', openCart);
        closeCartBtn.addEventListener('click', closeCart);

        // Initial cart display update (empty cart)
        updateCart();
    </script>
</body>
</html>
