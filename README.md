# Shopping-Website
This is a simple yet visually appealing shopping website for cosmetics. The UI features a soft pink gradient background, elegant product cards, and smooth hover effects. The project is built using HTML, CSS, and JavaScript for a seamless and responsive design. Perfect for learning the basics of e-commerce website development.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shopping Website</title>
    <style>
        body {
            background: linear-gradient(to right, #ff9a9e, #fad0c4);
            font-family: 'Poppins', sans-serif;
            text-align: center;
            color: #4a4a4a;
        }
        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        .product {
            background: white;
            padding: 15px;
            border-radius: 12px;
            width: 180px;
            text-align: center;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease-in-out;
        }
        .product:hover {
            transform: scale(1.05);
        }
        .product button {
            background: #ff5f6d;
            border: none;
            color: white;
            padding: 8px 12px;
            margin-top: 10px;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.3s;
        }
        .product button:hover {
            background: #ff2d4d;
        }
        .cart {
            margin-top: 20px;
            background: white;
            padding: 20px;
            border-radius: 12px;
            display: inline-block;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            font-size: 28px;
            font-weight: bold;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Cosmetics Store</h1>
    <div class="container" id="products">
        <div class="product" data-name="Lipstick" data-price="200">
            <p><strong>Lipstick</strong> - ₹200</p>
            <button onclick="addToCart('Lipstick', 200)">Add to Cart</button>
        </div>
        <div class="product" data-name="Foundation" data-price="500">
            <p><strong>Foundation</strong> - ₹500</p>
            <button onclick="addToCart('Foundation', 500)">Add to Cart</button>
        </div>
        <div class="product" data-name="Eyeliner" data-price="150">
            <p><strong>Eyeliner</strong> - ₹150</p>
            <button onclick="addToCart('Eyeliner', 150)">Add to Cart</button>
        </div>
        <div class="product" data-name="Mascara" data-price="300">
            <p><strong>Mascara</strong> - ₹300</p>
            <button onclick="addToCart('Mascara', 300)">Add to Cart</button>
        </div>
        <div class="product" data-name="Blush" data-price="250">
            <p><strong>Blush</strong> - ₹250</p>
            <button onclick="addToCart('Blush', 250)">Add to Cart</button>
        </div>
        <div class="product" data-name="Nail Polish" data-price="100">
            <p><strong>Nail Polish</strong> - ₹100</p>
            <button onclick="addToCart('Nail Polish', 100)">Add to Cart</button>
        </div>
    </div>
    
    <div class="cart">
        <h2>Shopping Cart</h2>
        <ul id="cart-items"></ul>
        <p>Total: ₹<span id="total">0</span></p>
    </div>
    
    <script>
        let total = 0;
        function addToCart(name, price) {
            const cartItems = document.getElementById('cart-items');
            const li = document.createElement('li');
            li.textContent = `${name} - ₹${price}`;
            cartItems.appendChild(li);
            total += price;
            document.getElementById('total').textContent = total;
        }
    </script>
</body>
</html>
