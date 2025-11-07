<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>LuxMart — Beauty & Gadgets</title>

<!-- Recommended: change to a hosted font if you prefer -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
:root{
  --bg:#0b0f12;
  --card:#0f1416;
  --muted:#9aa6a8;
  --emerald:#08b76d; /* emerald money green */
  --glass: rgba(255,255,255,0.04);
  --accent-glow: 0 8px 30px rgba(8,183,109,0.12);
  --radius:16px;
  font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
  color-scheme: dark;
}

*{box-sizing:border-box}
html,body{height:100%}
body{
  margin:0;
  background:
    radial-gradient(1200px 400px at 10% 10%, rgba(8,183,109,0.03), transparent 8%),
    linear-gradient(180deg,#061018 0%, var(--bg) 60%);
  color:#eef3f2;
  -webkit-font-smoothing:antialiased;
  -moz-osx-font-smoothing:grayscale;
  line-height:1.4;
}

/* Header / Nav */
.header{
  position:sticky; top:0; z-index:40;
  backdrop-filter: blur(6px);
  background: linear-gradient(180deg, rgba(255,255,255,0.02), transparent);
  border-bottom: 1px solid rgba(255,255,255,0.02);
}
.container{
  max-width:1100px; margin:0 auto; padding:22px;
  display:flex; gap:20px; align-items:center; justify-content:space-between;
}
.brand{display:flex; gap:14px; align-items:center}
.logo{
  display:inline-grid; place-items:center;
  width:56px; height:56px; border-radius:12px;
  background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
  box-shadow: var(--accent-glow);
  border: 1px solid rgba(255,255,255,0.03);
  padding:6px;
}
.logo svg{width:36px;height:36px; display:block}
.title{font-weight:700; letter-spacing:0.6px}
.nav{
  display:flex; gap:18px; align-items:center;
}
.nav a{
  color:var(--muted); text-decoration:none; font-weight:600;
  padding:8px 10px; border-radius:8px; transition:all .18s;
}
.nav a:hover{ color: white; background: rgba(255,255,255,0.02) }
.cta{
  background:linear-gradient(90deg,var(--emerald), #07a86a);
  color:#05120f; padding:10px 14px; border-radius:12px;
  font-weight:700; border:none; cursor:pointer;
  box-shadow: 0 8px 30px rgba(8,183,109,0.18);
}

/* Mobile nav */
.menu-toggle{display:none; background:none; border:0; color:var(--muted)}

/* Hero */
.hero{
  max-width:1100px; margin:36px auto; padding:36px 22px 10px;
  display:grid; grid-template-columns: 1fr 420px; gap:28px; align-items:center;
}
.hero-left h1{
  margin:0 0 10px; font-size:34px; letter-spacing:-0.6px;
}
.hero-left p{margin:0 0 22px; color:var(--muted)}
.hero-card{
  padding:22px; border-radius:16px; background: linear-gradient(180deg, rgba(255,255,255,0.015), rgba(255,255,255,0.01));
  border:1px solid rgba(255,255,255,0.02);
  box-shadow: var(--accent-glow);
}

/* Products */
.products{
  max-width:1100px; margin:12px auto 80px; padding:0 22px;
  display:grid; gap:18px;
}
.grid{
  display:grid; grid-template-columns: repeat(3, 1fr); gap:18px;
}
.card{
  background: linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.015));
  border-radius:14px; padding:14px; border:1px solid rgba(255,255,255,0.02);
  transition: transform .22s ease, box-shadow .22s ease;
  display:flex; flex-direction:column; gap:12px; min-height:320px;
}
.card:hover{ transform: translateY(-8px); box-shadow: var(--accent-glow) }

.product-media{
  height:180px; border-radius:12px; overflow:hidden; position:relative;
  background: linear-gradient(135deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
  display:flex; align-items:center; justify-content:center;
  color:var(--muted); font-weight:600;
}
.product-media img{ width:100%; height:100%; object-fit:cover; display:block; }

/* Info */
.card h3{ margin:0; font-size:18px }
.card p{ margin:0; color:var(--muted); font-size:13px }
.price-row{ margin-top:auto; display:flex; align-items:center; justify-content:space-between; gap:12px }
.price{ font-weight:700; color:var(--emerald) }
.buy{
  background:transparent; border:1px solid rgba(255,255,255,0.04); padding:10px 12px; border-radius:12px;
  cursor:pointer; font-weight:700; color:var(--emerald); text-decoration:none;
  transition:all .16s;
}
.buy:hover{ background: rgba(8,183,109,0.06); transform:translateY(-2px) }

/* Footer */
.footer{
  margin-top:40px; padding:30px 22px; border-top:1px solid rgba(255,255,255,0.02);
  color:var(--muted); text-align:center;
}

/* Responsiveness */
@media (max-width:1000px){
  .hero{ grid-template-columns: 1fr; gap:18px }
  .grid{ grid-template-columns: repeat(2, 1fr) }
}
@media (max-width:640px){
  .container{ padding:14px }
  .nav{ display:none }
  .menu-toggle{ display:block }
  .grid{ grid-template-columns: 1fr }
  .logo{ width:48px; height:48px }
}
</style>
</head>

<body>

<header class="header">
  <div class="container">
    <div class="brand">
      <div class="logo" aria-hidden="true">
        <!-- Lux AA logo (SVG) -->
        <svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Logo">
          <rect x="0" y="0" width="100" height="100" rx="16" fill="url(#g)"/>
          <defs>
            <linearGradient id="g" x1="0" x2="1" y1="0" y2="1">
              <stop offset="0" stop-color="#0b2017"/>
              <stop offset="1" stop-color="#072016"/>
            </linearGradient>
          </defs>
          <g transform="translate(14,18)" fill="none" stroke="#08b76d" stroke-width="6" stroke-linecap="round" stroke-linejoin="round">
            <path d="M0 50 L22 0 L44 50" />
            <path d="M30 50 L52 0 L74 50" />
          </g>
        </svg>
      </div>
      <div>
        <div class="title">LuxMart</div>
        <div style="font-size:12px;color:var(--muted)">Beauty & Gadgets</div>
      </div>
    </div>

    <nav class="nav" aria-label="Main navigation">
      <a href="#home">Home</a>
      <a href="#products">Products</a>
      <a href="#contact">Contact</a>
    </nav>

    <div style="display:flex;gap:12px;align-items:center">
      <button class="menu-toggle" aria-label="Toggle menu" onclick="toggleMenu()">☰</button>
      <a class="cta" href="#products">Shop Now</a>
    </div>
  </div>
</header>

<main>

<section id="home" class="hero">
  <div class="hero-left">
    <div class="hero-card">
      <h1>Premium Beauty & Smart Gadgets</h1>
      <p>Curated collection. Modern design. Elevated experience. Discover products that feel premium and perform beautifully.</p>
      <p style="margin:14px 0 0">
        <a class="buy" href="#products">Explore Collection</a>
        <a class="buy" style="margin-left:8px" href="#contact">Get in Touch</a>
      </p>
    </div>
  </div>

  <aside>
    <div class="hero-card" style="display:flex;flex-direction:column;gap:12px">
      <div style="display:flex;align-items:center;gap:12px">
        <div style="width:56px;height:56px;border-radius:12px;background:linear-gradient(180deg,rgba(255,255,255,0.02),transparent);display:grid;place-items:center">★</div>
        <div>
          <div style="font-weight:700">Free shipping</div>
          <div style="font-size:13px;color:var(--muted)">On orders over $80</div>
        </div>
      </div>

      <div style="display:flex;align-items:center;gap:12px">
        <div style="width:56px;height:56px;border-radius:12px;background:linear-gradient(180deg,rgba(255,255,255,0.02),transparent);display:grid;place-items:center">🔒</div>
        <div>
          <div style="font-weight:700">Secure checkout</div>
          <div style="font-size:13px;color:var(--muted)">Trusted payment partners</div>
        </div>
      </div>

      <div style="display:flex;align-items:center;gap:12px">
        <div style="width:56px;height:56px;border-radius:12px;background:linear-gradient(180deg,rgba(255,255,255,0.02),transparent);display:grid;place-items:center">⭐</div>
        <div>
          <div style="font-weight:700">Top-rated picks</div>
          <div style="font-size:13px;color:var(--muted)">Hand-selected products</div>
        </div>
      </div>
    </div>
  </aside>
</section>

<section id="products" class="products">
  <h2 style="margin:0 22px 8px">Featured Products</h2>

  <div class="grid" id="productGrid">

    <!-- Product card template: copy/update as needed -->
    <article class="card">
      <div class="product-media">
        <!-- Replace the src with images/product1.jpg -->
        <img src="images/product1.jpg" alt="Product 1" onerror="this.style.filter='grayscale(20%)';this.parentElement.innerHTML='Image<br>placeholder'">
      </div>
      <h3>Emerald Glow Serum</h3>
      <p>Lightweight serum for radiant skin. 30ml.</p>
      <div class="price-row">
        <div class="price">$29</div>
        <a class="buy" href="https://www.alibaba.com/" target="_blank" rel="noopener">Buy on Alibaba</a>
      </div>
    </article>

    <article class="card">
      <div class="product-media">
        <img src="images/product2.jpg" alt="Product 2" onerror="this.style.filter='grayscale(20%)';this.parentElement.innerHTML='Image<br>placeholder'">
      </div>
      <h3>Sonic Facial Cleansing Gadget</h3>
      <p>Ultra-soft bristles. Rechargeable. Waterproof.</p>
      <div class="price-row">
        <div class="price">$49</div>
        <a class="buy" href="https://www.alibaba.com/" target="_blank" rel="noopener">Buy on Alibaba</a>
      </div>
    </article>

    <article class="card">
      <div class="product-media">
        <img src="images/product3.jpg" alt="Product 3" onerror="this.style.filter='grayscale(20%)';this.parentElement.innerHTML='Image<br>placeholder'">
      </div>
      <h3>Luxury Lip Tint</h3>
      <p>Long-lasting color with satin finish.</p>
      <div class="price-row">
        <div class="price">$19</div>
        <a class="buy" href="https://www.alibaba.com/" target="_blank" rel="noopener">Buy on Alibaba</a>
      </div>
    </article>

    <article class="card">
      <div class="product-media">
        <img src="images/product4.jpg" alt="Product 4" onerror="this.style.filter='grayscale(20%)';this.parentElement.innerHTML='Image<br>placeholder'">
      </div>
      <h3>Smart Makeup Mirror</h3>
      <p>LED lighting with color temperature control.</p>
      <div class="price-row">
        <div class="price">$89</div>
        <a class="buy" href="https://www.alibaba.com/" target="_blank" rel="noopener">Buy on Alibaba</a>
      </div>
    </article>

    <article class="card">
      <div class="product-media">
        <img src="images/product5.jpg" alt="Product 5" onerror="this.style.filter='grayscale(20%)';this.parentElement.innerHTML='Image<br>placeholder'">
      </div>
      <h3>Rechargeable Eyelash Curler</h3>
      <p>Gentle heat curl for lasting lift.</p>
      <div class="price-row">
        <div class="price">$34</div>
        <a class="buy" href="https://www.alibaba.com/" target="_blank" rel="noopener">Buy on Alibaba</a>
      </div>
    </article>

    <article class="card">
      <div class="product-media">
        <img src="images/product6.jpg" alt="Product 6" onerror="this.style.filter='grayscale(20%)';this.parentElement.innerHTML='Image<br>placeholder'">
      </div>
      <h3>Portable Facial Steamer</h3>
      <p>Compact. Fast steam for deep hydration.</p>
      <div class="price-row">
        <div class="price">$59</div>
        <a class="buy" href="https://www.alibaba.com/" target="_blank" rel="noopener">Buy on Alibaba</a>
      </div>
    </article>

  </div>
</section>

<section id="contact" style="max-width:1100px;margin:0 auto 60px;padding:0 22px">
  <div class="hero-card" style="padding:18px">
    <h3>Contact Us</h3>
    <p style="color:var(--muted);margin:6px 0 12px">Questions? Partnerships? Send a message.</p>
    <form onsubmit="handleContact(event)" style="display:flex;gap:8px;flex-wrap:wrap">
      <input id="name" placeholder="Name" style="flex:1;min-width:180px;padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
      <input id="email" type="email" placeholder="Email" style="flex:1;min-width:220px;padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
      <input id="subject" placeholder="Subject" style="flex-basis:100%;padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
      <button class="cta" type="submit" style="margin-left:auto">Send</button>
    </form>
  </div>
</section>

<footer class="footer">
  <div class="container" style="max-width:1100px">
    <div style="flex:1">© <span id="year"></span> LuxMart — All rights reserved</div>
    <div style="opacity:0.9">Made for your brand</div>
  </div>
</footer>

<script>
/* Minimal interactivity */
/* Toggle mobile nav: clones desktop links into mobile overlay */
function toggleMenu(){
  const nav = document.querySelector('.nav');
  if(!nav) return;
  if(getComputedStyle(nav).display === 'none'){
    // show simple prompt menu
    const items = ['Home','#home','Products','#products','Contact','#contact'];
    const html = items.reduce((acc, cur, i) => i%2===0 ? acc + `<a href="${items[i+1]}" style="display:block;padding:12px 16px;color:var(--muted);text-decoration:none">${cur}</a>` : acc,'');
    const overlay = document.createElement('div');
    overlay.id='mobileNav';
    overlay.style.position='fixed';
    overlay.style.inset='64px 18px 18px';
    overlay.style.background='linear-gradient(180deg, rgba(255,255,255,0.02), transparent)';
    overlay.style.borderRadius='14px';
    overlay.style.boxShadow='var(--accent-glow)';
    overlay.style.padding='12px';
    overlay.style.zIndex=999;
    overlay.innerHTML = html;
    overlay.addEventListener('click', e=>{
      if(e.target.tagName === 'A') overlay.remove();
    });
    document.body.appendChild(overlay);
    setTimeout(()=>overlay.style.transform='scale(1)',10);
  } else {
    // nothing for wide screens
  }
}

/* Contact placeholder */
function handleContact(e){
  e.preventDefault();
  const n = document.getElementById('name').value || '—';
  const em = document.getElementById('email').value || '—';
  alert('Message queued. Name: ' + n + '\\nEmail: ' + em + '\\n(Replace alert with real backend or mailto link.)');
}

/* Year */
document.getElementById('year').textContent = new Date().getFullYear();

/* Smooth scroll for anchors */
document.querySelectorAll('a[href^="#"]').forEach(a=>{
  a.addEventListener('click', function(e){
    const target = document.querySelector(this.getAttribute('href'));
    if(target){
      e.preventDefault();
      target.scrollIntoView({behavior:'smooth', block:'start'});
    }
  });
});
</script>

</body>
</html>
