# Ex02 Commercial Website
## Date:30-10-2026

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
index.html
```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ShopNova - Online Shopping</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <div class="logo">Shop<span>Nova.</span></div>
    <nav>
        <a href="#home">Home</a>
        <a href="#products">Products</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
        <a href="#account">Account</a>
    </nav>
    <a href="#products" class="cart">🛒 Shop Now</a>
</header>

<section class="hero" id="home">
    <div class="hero-content">
        <h1>Discover Your Style</h1>
        <p>Explore the latest trends and shop your favourite products at amazing prices.</p>
        <a href="#products" class="btn">Explore Products →</a>
    </div>
</section>

<section class="products" id="products">
    <h2>Our Popular Products</h2>
    <p class="subtitle">Discover our best-selling collections</p>

    <div class="product-container">

        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?w=500" alt="Headphones">
            <h3>Wireless Headphones</h3>
            <p>Premium sound quality</p>
            <h4>₹1,999</h4>
            <button onclick="buy('Wireless Headphones')">Buy Now</button>
        </div>

        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?w=500" alt="Watch">
            <h3>Smart Watch</h3>
            <p>Modern lifestyle watch</p>
            <h4>₹2,499</h4>
            <button onclick="buy('Smart Watch')">Buy Now</button>
        </div>

        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?w=500" alt="Shoes">
            <h3>Sports Shoes</h3>
            <p>Comfortable running shoes</p>
            <h4>₹1,799</h4>
            <button onclick="buy('Sports Shoes')">Buy Now</button>
        </div>

        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f?w=500" alt="Camera">
            <h3>Digital Camera</h3>
            <p>Capture every moment</p>
            <h4>₹5,999</h4>
            <button onclick="buy('Digital Camera')">Buy Now</button>
        </div>

    </div>
</section>

<section class="about" id="about">
    <h2>About ShopNova</h2>
    <p>
        ShopNova is an online shopping platform that provides
        high-quality products at affordable prices. Our goal is
        to make shopping simple, convenient and enjoyable.
    </p>
</section>

<section class="contact" id="contact">
    <h2>Contact Us</h2>
    <p>Email: support@shopnova.com</p>
    <p>Phone: +91 98765 43210</p>
    <p>Location: Chennai, Tamil Nadu</p>
</section>

<section class="account" id="account">
    <h2>User Account</h2>
    <form onsubmit="login(event)">
        <input type="email" placeholder="Enter your email" required>
        <input type="password" placeholder="Enter your password" required>
        <button type="submit">Login</button>
    </form>
</section>

<footer>
    <h2>ShopNova.</h2>
    <p>Follow us on social media</p>
    <div class="social">
        <a href="https://www.instagram.com/">Instagram</a>
        <a href="https://www.facebook.com/">Facebook</a>
        <a href="https://www.youtube.com/">YouTube</a>
    </div>
    <p>© 2026 ShopNova. All Rights Reserved.</p>
</footer>

<script>
    function buy(product) {
        alert("Thank you for choosing " + product + "!");
    }

    function login(event) {
        event.preventDefault();
        alert("Login successful! Welcome to ShopNova.");
    }
</script>

</body>
</html>
```
style.css
```

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
    scroll-behavior: smooth;
}

body {
    background: #f8f9fc;
    color: #222;
}

header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 7%;
    background: white;
    box-shadow: 0 3px 12px rgba(0,0,0,0.08);
    position: sticky;
    top: 0;
    z-index: 100;
}

.logo {
    font-size: 28px;
    font-weight: bold;
    color: #172554;
}

.logo span {
    color: #f97316;
}

nav {
    display: flex;
    gap: 25px;
}

nav a {
    text-decoration: none;
    color: #333;
    font-weight: bold;
    transition: 0.3s;
}

nav a:hover {
    color: #f97316;
}

.cart, .btn {
    background: #f97316;
    color: white;
    padding: 12px 20px;
    border-radius: 25px;
    text-decoration: none;
    font-weight: bold;
}

.hero {
    min-height: 430px;
    display: flex;
    align-items: center;
    padding: 60px 10%;
    background: linear-gradient(90deg, rgba(0,0,0,0.8), rgba(0,0,0,0.1)),
    url("https://images.unsplash.com/photo-1441986300917-64674bd600d8?w=1600")
    center/cover;
    color: white;
}

.hero-content {
    max-width: 550px;
}

.hero h1 {
    font-size: 55px;
    margin-bottom: 20px;
}

.hero p {
    font-size: 18px;
    line-height: 1.7;
    margin-bottom: 30px;
}

.btn:hover, .cart:hover {
    background: #ea580c;
}

.products {
    padding: 65px 7%;
    text-align: center;
}

.products h2, .about h2, .contact h2,
.account h2 {
    font-size: 32px;
    color: #172554;
    margin-bottom: 12px;
}

.subtitle {
    color: #777;
    margin-bottom: 35px;
}

.product-container {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 25px;
}

.product-card {
    background: white;
    width: 250px;
    padding: 15px;
    border-radius: 15px;
    box-shadow: 0 5px 20px rgba(0,0,0,0.08);
    transition: 0.3s;
}

.product-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 25px rgba(0,0,0,0.15);
}

.product-card img {
    width: 100%;
    height: 180px;
    object-fit: cover;
    border-radius: 10px;
}

.product-card h3 {
    margin: 15px 0 8px;
}

.product-card p {
    color: #777;
    margin-bottom: 10px;
}

.product-card h4 {
    color: #f97316;
    font-size: 20px;
    margin-bottom: 15px;
}

button {
    background: #172554;
    color: white;
    border: none;
    padding: 12px 25px;
    border-radius: 7px;
    cursor: pointer;
    transition: 0.3s;
}

button:hover {
    background: #f97316;
}

.about {
    background: #eaf0ff;
    text-align: center;
    padding: 65px 15%;
}

.about p {
    line-height: 1.8;
    color: #555;
    font-size: 17px;
}

.contact {
    padding: 60px 20px;
    text-align: center;
    line-height: 2;
}

.account {
    background: #eaf0ff;
    padding: 55px 20px;
    text-align: center;
}

.account form {
    display: flex;
    flex-direction: column;
    gap: 15px;
    max-width: 350px;
    margin: 25px auto 0;
}

.account input {
    padding: 14px;
    border: 1px solid #ccc;
    border-radius: 7px;
}

footer {
    background: #172554;
    color: white;
    padding: 35px 20px;
    text-align: center;
    line-height: 2;
}

.social {
    display: flex;
    justify-content: center;
    gap: 25px;
    margin: 12px;
}

.social a {
    color: #fb923c;
    text-decoration: none;
}

.social a:hover {
    color: white;
}

@media (max-width: 768px) {
    header {
        flex-direction: column;
        gap: 18px;
    }

    nav {
        flex-wrap: wrap;
        justify-content: center;
        gap: 15px;
    }

    .hero h1 {
        font-size: 38px;
    }

    .product-container {
        align-items: center;
    }
}

```

## OUTPUT

<img width="1910" height="931" alt="1" src="https://github.com/user-attachments/assets/aaa5b6c6-ec2e-4522-9997-85e80d4ad431" />

<img width="1908" height="842" alt="2" src="https://github.com/user-attachments/assets/90566d1e-7478-4fb2-b005-2419f02e2f4b" />

<img width="1888" height="867" alt="3" src="https://github.com/user-attachments/assets/a335f1fe-058a-4b40-adfd-f1012c88c318" />

<img width="1907" height="797" alt="4" src="https://github.com/user-attachments/assets/af098917-8d42-4642-9ca9-8d60237cd0cd" />

<img width="1912" height="916" alt="5" src="https://github.com/user-attachments/assets/93601541-a30e-40f3-bfe2-cda900655309" />


## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
