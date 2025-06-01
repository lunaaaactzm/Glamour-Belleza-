<!DOCTYPE html><html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Glamour Belleza - Tienda de Maquillaje</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #fff8f4;
    }
    header {
      background-color: #ff5e78;
      color: white;
      padding: 1rem 2rem;
      text-align: center;
    }
    nav {
      background-color: #ffc2cc;
      padding: 0.5rem 2rem;
      display: flex;
      justify-content: center;
      gap: 2rem;
    }
    nav a {
      text-decoration: none;
      color: #800020;
      font-weight: bold;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
      padding: 2rem;
    }
    .product {
      background: white;
      border-radius: 10px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      padding: 1rem;
      text-align: center;
    }
    .product img {
      max-width: 100%;
      border-radius: 10px;
    }
    .product h3 {
      color: #ff5e78;
    }
    .product button {
      background-color: #ff5e78;
      color: white;
      border: none;
      padding: 0.5rem 1rem;
      border-radius: 5px;
      cursor: pointer;
    }
    footer {
      background-color: #ff5e78;
      color: white;
      text-align: center;
      padding: 1rem;
      margin-top: 2rem;
    }
    #cart {
      position: fixed;
      top: 1rem;
      right: 1rem;
      background-color: white;
      border: 2px solid #ff5e78;
      padding: 1rem;
      border-radius: 10px;
      width: 250px;
      max-height: 400px;
      overflow-y: auto;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }
    #cart h2 {
      margin-top: 0;
      color: #ff5e78;
    }
    .cart-item {
      border-bottom: 1px solid #ddd;
      padding: 0.5rem 0;
    }
  </style>
</head>
<body>
  <header>
    <h1>Glamour Belleza</h1>
    <p>Tu tienda de maquillaje de confianza</p>
  </header>
  <nav>
    <a href="#">Inicio</a>
    <a href="#">Productos</a>
    <a href="#">Ofertas</a>
    <a href="#">Contacto</a>
  </nav>
  <main class="products">
    <div class="product">
      <img src="https://via.placeholder.com/250x250?text=Base+L%C3%ADquida" alt="Base Líquida">
      <h3>Base Líquida</h3>
      <p>$15.99</p>
      <button onclick="addToCart('Base Líquida', 15.99)">Comprar</button>
    </div>
    <div class="product">
      <img src="https://via.placeholder.com/250x250?text=Labial+Mate" alt="Labial Mate">
      <h3>Labial Mate</h3>
      <p>$8.99</p>
      <button onclick="addToCart('Labial Mate', 8.99)">Comprar</button>
    </div>
    <div class="product">
      <img src="https://via.placeholder.com/250x250?text=Paleta+de+Sombras" alt="Paleta de Sombras">
      <h3>Paleta de Sombras</h3>
      <p>$22.50</p>
      <button onclick="addToCart('Paleta de Sombras', 22.50)">Comprar</button>
    </div>
    <div class="product">
      <img src="https://via.placeholder.com/250x250?text=R%C3%ADmel+Volumen" alt="Rímel Volumen">
      <h3>Rímel Volumen</h3>
      <p>$10.99</p>
      <button onclick="addToCart('Rímel Volumen', 10.99)">Comprar</button>
    </div>
  </main>
  <div id="cart">
    <h2>Carrito</h2>
    <div id="cart-items"></div>
    <p><strong>Total:</strong> $<span id="cart-total">0.00</span></p>
  </div>
  <footer>
    <p>&copy; 2025 Glamour Belleza. Todos los derechos reservados.</p>
  </footer>  <script>
    const cartItems = document.getElementById('cart-items');
    const cartTotal = document.getElementById('cart-total');
    let total = 0;

    function addToCart(name, price) {
      const item = document.createElement('div');
      item.className = 'cart-item';
      item.textContent = `${name} - $${price.toFixed(2)}`;
      cartItems.appendChild(item);
      total += price;
      cartTotal.textContent = total.toFixed(2);
    }
  </script></body>
</html>
