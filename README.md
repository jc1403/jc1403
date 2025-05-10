<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>The JC Shop | Menswear & Jewelry</title>
  <link href="https://www.makvac.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Montserrat', sans-serif;
      background-color: #f9f9f9;
    }
    header {
      background-color: #111;
      color: white;
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    header h1 {
      margin: 0;
      font-size: 1.5rem;
    }
    nav a {
      color: white;
      margin-left: 1.5rem;
      text-decoration: none;
      font-weight: bold;
    }
    .hero {
      background: url('https://images.unsplash.com/photo-1521334884684-d80222895322') center/cover no-repeat;
      height: 80vh;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      text-shadow: 0 2px 10px rgba(0,0,0,0.5);
      text-align: center;
    }
    .hero h2 {
      font-size: 3rem;
      margin: 0;
    }
    .section {
      padding: 3rem 2rem;
      text-align: center;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
      margin-top: 2rem;
    }
    .product-card {
      background: white;
      padding: 1rem;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }
    .product-card img {
      max-width: 100%;
      border-radius: 10px;
    }
    .product-card h3 {
      margin: 0.5rem 0;
    }
    .product-card button {
      margin: 0.5rem;
      padding: 0.5rem 1rem;
      border: none;
      border-radius: 5px;
      background-color: #111;
      color: white;
      cursor: pointer;
    }
    footer {
      background-color: #111;
      color: white;
      padding: 2rem;
      text-align: center;
      margin-top: 4rem;
    }
    form {
      max-width: 600px;
      margin: 0 auto;
      text-align: left;
    }
    form label {
      display: block;
      margin: 1rem 0 0.5rem;
    }
    form input, form textarea {
      width: 100%;
      padding: 0.75rem;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-family: inherit;
    }
    form button {
      margin-top: 1rem;
      padding: 0.75rem 2rem;
      background-color: #111;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-weight: bold;
    }
    #cart, #wishlist {
      position: fixed;
      top: 0;
      right: 0;
      width: 320px;
      background: white;
      height: 100%;
      padding: 2rem;
      box-shadow: -2px 0 10px rgba(0,0,0,0.2);
      overflow-y: auto;
      display: none;
    }
    #cart h3, #wishlist h3 {
      margin-top: 0;
    }
    .cart-item, .wishlist-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin: 1rem 0;
    }
    .cart-controls {
      display: flex;
      align-items: center;
    }
    .cart-controls button {
      margin: 0 0.25rem;
      padding: 0.25rem 0.5rem;
      background: #111;
      color: white;
      border: none;
      border-radius: 3px;
      cursor: pointer;
    }
    #checkout {
      margin-top: 2rem;
      padding: 0.75rem 1.5rem;
      background: #111;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <header>
    <h1>The JC Shop</h1>
    <nav>
      <a href="#menswear">Menswear</a>
      <a href="#jewelry">Jewelry</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
      <a href="#" onclick="toggleCart()">Cart</a>
      <a href="#" onclick="toggleWishlist()">Wishlist</a>
    </nav>
  </header>  <section class="hero">
    <h2>Style That Defines You</h2>
  </section>  <section class="section" id="menswear">
    <h2>Menswear Collection</h2>
    <div class="products">
      <div class="product-card">
        <img src="https://www.makvac.com/product-page/sukuna-oversized-tee" alt="T-shirt">
        <h3>Classic T-Shirt</h3>
        <p>$24.99</p>
        <button onclick="addToCart('Classic T-Shirt')">Add to Cart</button>
        <button onclick="addToWishlist('Classic T-Shirt')">Add to Wishlist</button>
      </div>
      <div class="product-card">
        <img src="https://www.makvac.com/product-page/zoro-oversized-tee" alt="T-shirt">
        <h3>Urban Jacket</h3>
        <p>$69.99</p>
        <button onclick="addToCart('Urban Jacket')">Add to Cart</button>
        <button onclick="addToWishlist('Urban Jacket')">Add to Wishlist</button>
      </div>
    </div>
  </section>  <section class="section" id="jewelry">
    <h2>Jewelry Collection</h2>
    <div class="products">
      <div class="product-card">
        <img src="https://images.unsplash.com/photo-1599940824395-322fba6aa1a0" alt="Bracelet">
        <h3>Steel Bracelet</h3>
        <p>$19.99</p>
        <button onclick="addToCart('Steel Bracelet')">Add to Cart</button>
        <button onclick="addToWishlist('Steel Bracelet')">Add to Wishlist</button>
      </div>
      <div class="product-card">
        <img src="https://images.unsplash.com/photo-1633085281795-4b5b89e6ad10" alt="Ring">
        <h3>Minimal Ring</h3>
        <p>$14.99</p>
        <button onclick="addToCart('Minimal Ring')">Add to Cart</button>
        <button onclick="addToWishlist('Minimal Ring')">Add to Wishlist</button>
      </div>
    </div>
  </section>  <section class="section" id="about">
    <h2>About The JC Shop</h2>
    <p>The JC Shop is your destination for bold, stylish, and affordable menswear and jewelry. We believe fashion is a form of self-expression, and our mission is to empower modern men to showcase their confidence and personality through timeless pieces.</p>
  </section>  <section class="section" id="contact">
    <h2>Contact Us</h2>
    <form>
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" required><label for="email">Email:</label>
  <input type="email" id="email" name="email" required>

  <label for="message">Message:</label>
  <textarea id="message" name="message" rows="5" required></textarea>

  <button type="submit">Send Message</button>
</form>

  </section>  <div id="cart">
    <h3>Shopping Cart</h3>
    <ul id="cart-items"></ul>
    <button id="checkout" onclick="checkout()">Checkout</button>
  </div>  <div id="wishlist">
    <h3>Wishlist</h3>
    <ul id="wishlist-items"></ul>
  </div>  <footer>
    <p>&copy; 2025 The JC Shop | All rights reserved</p>
  </footer>  <script>
    const cart = {};

    function toggleCart() {
      const cartBox = document.getElementById('cart');
      cartBox.style.display = cartBox.style.display === 'block' ? 'none' : 'block';
    }

    function toggleWishlist() {
      const wishlist = document.getElementById('wishlist');
      wishlist.style.display = wishlist.style.display === 'block' ? 'none' : 'block';
    }

    function addToCart(product) {
      if (!cart[product]) cart[product] = 1;
      else cart[product]++;
      renderCart();
    }

    function removeFromCart(product) {
      delete cart[product];
      renderCart();
    }

    function updateQuantity(product, change) {
      if (cart[product]) {
        cart[product] += change;
        if (cart[product] <= 0) delete cart[product];
        renderCart();
      }
    }

    function renderCart() {
      const cartList = document.getElementById('cart-items');
      cartList.innerHTML = '';
      for (const item in cart) {
        const li = document.createElement('li');
        li.className = 'cart-item';
        li.innerHTML = `
          <span>${item}</span>
          <div class="cart-controls">
            <button onclick="updateQuantity('${item}', -1)">-</button>
            <span>${cart[item]}</span>
            <button onclick="updateQuantity('${item}', 1)">+</button>
            <button onclick="removeFromCart('${item}')">x</button>
          </div>
        `;
        cartList.appendChild(li);
      }
    }

    function addToWishlist(product) {
      const list = document.getElementById('wishlist-items');
      const li = document.createElement('li');
      li.className = 'wishlist-item';
      li.textContent = product;
      list.appendChild(li);
    }

    function checkout() {
      alert("Thank you for your purchase! This is a demo checkout.");
      for (let item in cart) delete cart[item];
      renderCart();
    }
  </script></body>
</html>
