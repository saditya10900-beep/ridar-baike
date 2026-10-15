
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Aditya Singh | Raider Bike</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: #101114;
      color: white;
    }

    header {
      padding: 22px 8%;
      background: #08090b;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 15px;
    }

    .logo {
      color: #ff303b;
      font-size: 30px;
      font-weight: 900;
      letter-spacing: 2px;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin-left: 20px;
    }

    nav a:hover {
      color: #ff303b;
    }

    .hero {
      min-height: 85vh;
      padding: 65px 8%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 35px;
      flex-wrap: wrap;
      background: linear-gradient(120deg, #111216, #292b31);
    }

    .hero-content {
      flex: 1 1 300px;
    }

    .hero h1 {
      font-size: clamp(42px, 7vw, 76px);
      font-weight: 900;
      line-height: 1.1;
      margin-bottom: 20px;
    }

    .hero h1 span {
      color: #ff303b;
    }

    .hero p {
      color: #d0d0d0;
      line-height: 1.8;
      margin-bottom: 25px;
      font-size: 17px;
    }

    .bike-image {
      flex: 1 1 300px;
    }

    .bike-image img {
      width: 100%;
      border-radius: 15px;
      filter: drop-shadow(0 0 25px #ff303b30);
    }

    .btn {
      display: inline-block;
      padding: 14px 24px;
      border: none;
      border-radius: 5px;
      background: #ff303b;
      color: white;
      text-decoration: none;
      font-size: 15px;
      font-weight: bold;
      cursor: pointer;
      margin: 5px 8px 5px 0;
    }

    .btn:hover {
      background: #d71925;
    }

    .features {
      padding: 65px 8%;
      text-align: center;
    }

    .features h2 {
      font-size: 36px;
      margin-bottom: 30px;
    }

    .feature-grid {
      display: grid;
      grid-template-columns: repeat(
        auto-fit, minmax(200px, 1fr)
      );
      gap: 22px;
    }

    .feature-card {
      background: #1d1f24;
      padding: 30px 20px;
      border-radius: 12px;
      border-bottom: 3px solid #ff303b;
    }

    .feature-card h3 {
      color: #ff454e;
      margin-bottom: 12px;
    }

    .feature-card p {
      color: #d0d0d0;
      line-height: 1.6;
    }

    .price-section {
      padding: 55px 20px;
      text-align: center;
      background: #1b1c21;
    }

    .price-section h2 {
      margin-bottom: 15px;
    }

    .price {
      font-size: 36px;
      color: #ff454e;
      font-weight: bold;
      margin: 18px 0;
    }

    footer {
      background: #08090b;
      text-align: center;
      padding: 28px 15px;
      color: #bdbdbd;
      line-height: 1.8;
    }

    @media (max-width: 600px) {
      header {
        padding: 20px 5%;
      }

      nav a {
        margin-left: 8px;
        font-size: 12px;
      }

      .hero {
        padding: 45px 6%;
      }

      .features {
        padding: 45px 6%;
      }
    }
  </style>
</head>

<body>

  <header>
    <div class="logo">RAIDER.</div>

    <nav>
      <a href="#home">Home</a>
      <a href="#features">Features</a>
      <a href="#price">Price</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="hero" id="home">
    <div class="hero-content">
      <h1>UNLEASH<br>YOUR <span>RIDE.</span></h1>

      <p>
        Discover the sporty TVS Raider 125.
        Bold styling, exciting performance and
        everyday riding comfort.
      </p>

      <a href="#features" class="btn">Explore Bike</a>

      <button class="btn" onclick="testRide()">
        Book Test Ride
      </button>

      <p id="message"></p>
    </div>

    <div class="bike-image">
      <img
        src="https://images.unsplash.com/photo-1558981806-ec527fa84c39?auto=format&fit=crop&w=1000&q=85"
        alt="Sporty motorcycle"
      >
    </div>
  </section>

  <section class="features" id="features">
    <h2>BIKE FEATURES</h2>

    <div class="feature-grid">

      <div class="feature-card">
        <h3>🏍️ Sporty Design</h3>
        <p>Bold styling for a distinctive road presence.</p>
      </div>

      <div class="feature-card">
        <h3>⚡ 125cc Class</h3>
        <p>A sporty commuter motorcycle experience.</p>
      </div>

      <div class="feature-card">
        <h3>🛣️ Riding Comfort</h3>
        <p>Designed for daily rides and city journeys.</p>
      </div>

      <div class="feature-card">
        <h3>✨ Modern Features</h3>
        <p>Features vary depending on the model variant.</p>
      </div>

    </div>
  </section>

  <section class="price-section" id="price">
    <h2>YOUR NEXT RIDE AWAITS</h2>

    <p>TVS Raider 125</p>

    <div class="price">Check Latest Price</div>

    <button class="btn" onclick="showPrice()">
      View Price Information
    </button>

    <p id="priceMessage"></p>
  </section>

  <footer id="contact">
    <h3>RAIDER BIKE WEBSITE</h3>
    <p>Website created by Aditya Singh</p>
    <p>Student project / demo website</p>
    <p>© 2026 Aditya Singh</p>
  </footer>

  <script>
    function testRide() {
      document.getElementById("message").textContent =
        "Test ride request demo! Contact an authorized dealer to book.";
    }

    function showPrice() {
      document.getElementById("priceMessage").textContent =
        "Price depends on your city and bike variant. Please check with an authorized TVS dealer.";
    }
  </script>

</body>
</html>
