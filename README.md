# Doctor-spicey-<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Doctor Spicey — 100% Organic Pure Spices</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
:root {
  --primary: #b3241d;
  --primary-dark: #7e1a15;
  --accent: #e3a712;
  --green: #2e7d32;
  --bg-main: #f8f9fa;
  --card-bg: #ffffff;
  --text-main: #1c1d1f;
  --text-muted: #6a6f73;
  --border: #e4e8eb;
  --shadow-sm: 0 2px 8px rgba(0,0,0,0.06);
  --shadow-md: 0 8px 24px rgba(0,0,0,0.1);
}

* { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Plus Jakarta Sans', sans-serif; }
body { background-color: var(--bg-main); color: var(--text-main); line-height: 1.5; }

/* Navigation Bar */
header {
  position: sticky; top: 0; z-index: 100;
  background: #ffffff; border-bottom: 1px solid var(--border);
  box-shadow: var(--shadow-sm);
}
.navbar {
  max-width: 1200px; margin: 0 auto; padding: 12px 20px;
  display: flex; align-items: center; justify-content: space-between;
}
.brand { display: flex; align-items: center; gap: 10px; font-weight: 800; font-size: 1.4rem; color: var(--primary); }
.brand span { color: var(--green); }
.nav-actions { display: flex; align-items: center; gap: 16px; }
.cart-btn {
  position: relative; background: var(--bg-main); border: 1px solid var(--border);
  padding: 8px 16px; border-radius: 20px; font-weight: 700; cursor: pointer; display: flex; align-items: center; gap: 8px;
}
.cart-count { background: var(--primary); color: #fff; border-radius: 50%; width: 20px; height: 20px; font-size: 0.75rem; display: flex; align-items: center; justify-content: center; }

/* Hero Banner */
.hero {
  background: linear-gradient(135deg, #7e1a15 0%, #b3241d 100%);
  color: white; padding: 48px 20px; text-align: center;
}
.hero h1 { font-size: 2.2rem; font-weight: 800; margin-bottom: 10px; }
.hero p { font-size: 1.1rem; opacity: 0.9; max-width: 600px; margin: 0 auto 20px; }
.hero-badges { display: flex; justify-content: center; gap: 12px; flex-wrap: wrap; }
.hero-badge { background: rgba(255,255,255,0.2); padding: 6px 16px; border-radius: 20px; font-size: 0.85rem; font-weight: 600; backdrop-filter: blur(4px); }

/* Main Section */
.container { max-width: 1200px; margin: 30px auto; padding: 0 20px; }
.section-title { font-size: 1.5rem; font-weight: 800; margin-bottom: 20px; display: flex; align-items: center; gap: 10px; }
.section-title::before { content: ''; width: 6px; height: 24px; background: var(--primary); border-radius: 4px; }

/* Product Grid */
.products-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 24px; }
.product-card {
  background: var(--card-bg); border-radius: 16px; border: 1px solid var(--border);
  padding: 20px; transition: transform 0.2s, box-shadow 0.2s; display: flex; flex-direction: column; position: relative;
}
.product-card:hover { transform: translateY(-4px); box-shadow: var(--shadow-md); }
.product-tag { position: absolute; top: 16px; left: 16px; background: #eef7ee; color: var(--green); font-size: 0.75rem; font-weight: 700; padding: 4px 10px; border-radius: 12px; }

.product-img { width: 100%; height: 200px; object-fit: contain; margin-bottom: 16px; border-radius: 8px; }
.product-title { font-size: 1.15rem; font-weight: 700; margin-bottom: 6px; }
.product-sub { color: var(--text-muted); font-size: 0.85rem; margin-bottom: 14px; }

/* Pack Selector */
.pack-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 8px; margin-bottom: 16px; }
.pack-btn {
  border: 1px solid var(--border); background: var(--bg-main); border-radius: 8px;
  padding: 8px; text-align: center; cursor: pointer; font-size: 0.8rem; font-weight: 600; transition: 0.2s;
}
.pack-btn.active { border-color: var(--primary); background: #fdf2f2; color: var(--primary); }

.price-row { display: flex; align-items: baseline; gap: 8px; margin-bottom: 16px; }
.current-price { font-size: 1.4rem; font-weight: 800; color: var(--primary); }
.mrp-price { text-decoration: line-through; color: var(--text-muted); font-size: 0.9rem; }

.add-cart-btn {
  width: 100%; background: var(--primary); color: white; border: none; padding: 12px;
  border-radius: 10px; font-weight: 700; cursor: pointer; transition: background 0.2s;
}
.add-cart-btn:hover { background: var(--primary-dark); }

/* FSSAI & Trust Footer */
.trust-bar { background: #ffffff; border-top: 1px solid var(--border); border-bottom: 1px solid var(--border); margin-top: 40px; padding: 20px; text-align: center; }
.trust-items { max-width: 1000px; margin: 0 auto; display: flex; justify-content: space-around; flex-wrap: wrap; gap: 20px; font-weight: 600; font-size: 0.9rem; color: var(--text-muted); }

footer { background: #1c1d1f; color: white; padding: 30px 20px; text-align: center; font-size: 0.85rem; }
footer a { color: var(--accent); text-decoration: none; }

/* Floating WhatsApp FAB */
.wa-fab {
  position: fixed; bottom: 20px; right: 20px; background: #25d366; color: white;
  width: 56px; height: 56px; border-radius: 50%; display: flex; align-items: center; justify-content: center;
  box-shadow: var(--shadow-md); z-index: 99; text-decoration: none; font-size: 1.8rem;
}
</style>
</head>
<body>

<header>
  <div class="navbar">
    <div class="brand">🍃 DOCTOR <span>SPICEY</span></div>
    <div class="nav-actions">
      <button class="cart-btn" onclick="alert('Cart section ready! Proceeding to WhatsApp checkout.')">
        🛒 Cart <span class="cart-count" id="cartCount">0</span>
      </button>
    </div>
  </div>
</header>

<section class="hero">
  <h1>100% Organic Pure Spices</h1>
  <p>Doctor Spicey ke shudh, mila-vat rahit masale — asli rang, tez khushbu aur behtareen swaad.</p>
  <div class="hero-badges">
    <span class="hero-badge">✔ 100% Organic</span>
    <span class="hero-badge">✔ No Preservatives</span>
    <span class="hero-badge">✔ Cash on Delivery</span>
  </div>
</section>

<div class="container">
  <div class="section-title">Our Premium Range</div>
  
  <div class="products-grid">
    <!-- Product 1: Red Chilli Powder -->
    <div class="product-card">
      <span class="product-tag">100% Organic</span>
      <img src="data:image/jpeg;base64,..." alt="Red Chilli Powder" class="product-img">
      <div class="product-title">लाल मिर्च पाउडर (Red Chilli Powder)</div>
      <div class="product-sub">Rich Colour • Authentic Taste</div>
      <div class="pack-grid">
        <div class="pack-btn active">100g<br><b>₹50</b></div>
        <div class="pack-btn">250g<br><b>₹120</b></div>
        <div class="pack-btn">500g<br><b>₹230</b></div>
      </div>
      <div class="price-row">
        <span class="current-price">₹50</span>
        <span class="mrp-price">₹65</span>
      </div>
      <button class="add-cart-btn" onclick="addToCart('Red Chilli Powder')">Add to Cart</button>
    </div>

    <!-- Product 2: Turmeric Powder -->
    <div class="product-card">
      <span class="product-tag">100% Pure</span>
      <img src="data:image/jpeg;base64,..." alt="Turmeric Powder" class="product-img">
      <div class="product-title">हल्दी पाउडर (Turmeric Powder)</div>
      <div class="product-sub">Rich Colour • Authentic Taste</div>
      <div class="pack-grid">
        <div class="pack-btn active">100g<br><b>₹45</b></div>
        <div class="pack-btn">250g<br><b>₹110</b></div>
        <div class="pack-btn">500g<br><b>₹210</b></div>
      </div>
      <div class="price-row">
        <span class="current-price">₹45</span>
        <span class="mrp-price">₹60</span>
      </div>
      <button class="add-cart-btn" onclick="addToCart('Turmeric Powder')">Add to Cart</button>
    </div>

    <!-- Product 3: Coriander Powder -->
    <div class="product-card">
      <span class="product-tag">Natural Aroma</span>
      <img src="data:image/jpeg;base64,..." alt="Coriander Powder" class="product-img">
      <div class="product-title">धनिया पाउडर (Coriander Powder)</div>
      <div class="product-sub">Fresh Grinding • Pure Taste</div>
      <div class="pack-grid">
        <div class="pack-btn active">100g<br><b>₹40</b></div>
        <div class="pack-btn">250g<br><b>₹95</b></div>
        <div class="pack-btn">500g<br><b>₹180</b></div>
      </div>
      <div class="price-row">
        <span class="current-price">₹40</span>
        <span class="mrp-price">₹55</span>
      </div>
      <button class="add-cart-btn" onclick="addToCart('Coriander Powder')">Add to Cart</button>
    </div>
  </div>
</div>

<div class="trust-bar">
  <div class="trust-items">
    <div>✅ FSSAI Lic. No: 30260602124697043</div>
    <div>🚚 Cash on Delivery Available</div>
    <div>💬 Direct WhatsApp Order</div>
  </div>
</div>

<footer>
  <p><b>Doctor Spicey</b> — Meerapur, Marehra, Etah, Uttar Pradesh, India</p>
  <p style="margin-top:8px;">📞 Customer Care: <a href="https://wa.me/917409212099">+91 74092 12099</a> | ✉️ pvsir74@gmail.com</p>
</footer>

<a href="https://wa.me/917409212099" class="wa-fab" target="_blank">💬</a>

<script>
let count = 0;
function addToCart(pName) {
  count++;
  document.getElementById('cartCount').innerText = count;
  alert(pName + ' Cart me add ho gaya!');
}
</script>
</body>
</html>
