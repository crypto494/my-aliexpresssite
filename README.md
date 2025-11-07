<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>LuxMart — Beauty & Gadgets</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#07090a;
  --panel:#0e1413;
  --muted:#9aa6a8;
  --emerald:#08b76d;
  --glass: rgba(255,255,255,0.03);
  --radius:14px;
  --maxw:1200px;
  color-scheme: dark;
  font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,"Helvetica Neue",Arial;
}
*{box-sizing:border-box}
html,body{height:100%;margin:0;background:
  radial-gradient(1000px 300px at 10% 8%, rgba(8,183,109,0.03), transparent 8%),
  linear-gradient(180deg,#061018 0%, var(--bg) 60%);
color:#eef3f2;-webkit-font-smoothing:antialiased}
a{color:inherit}
.container{max-width:var(--maxw);margin:0 auto;padding:20px}

/* Header */
.header{position:sticky;top:0;z-index:50;background:linear-gradient(180deg,rgba(0,0,0,0.24),transparent);backdrop-filter:blur(6px);border-bottom:1px solid rgba(255,255,255,0.02)}
.header .container{display:flex;align-items:center;justify-content:space-between;gap:16px}
.brand{display:flex;align-items:center;gap:14px}
.logo{width:56px;height:56px;border-radius:12px;display:grid;place-items:center;background:linear-gradient(180deg,rgba(255,255,255,0.02),transparent);border:1px solid rgba(255,255,255,0.03);box-shadow:0 10px 30px rgba(8,183,109,0.12)}
.logo svg{width:36px;height:36px}
.title{font-weight:700;letter-spacing:0.4px}
.nav{display:flex;gap:14px;align-items:center}
.nav a{padding:8px 10px;border-radius:10px;text-decoration:none;color:var(--muted);font-weight:600}
.nav a:hover{color:#fff;background:rgba(255,255,255,0.02)}
.cta{background:linear-gradient(90deg,var(--emerald),#07a86a);color:#05120f;padding:10px 14px;border-radius:12px;font-weight:700;border:none;box-shadow:0 12px 40px rgba(8,183,109,0.18);text-decoration:none}

/* Hero */
.hero{display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center;padding:42px 20px}
.hero-left h1{margin:0;font-size:36px}
.hero-left p{margin:10px 0;color:var(--muted);max-width:70%}
.hero-card{background:linear-gradient(180deg,rgba(255,255,255,0.015),rgba(255,255,255,0.01));padding:22px;border-radius:16px;border:1px solid rgba(255,255,255,0.02);box-shadow:0 10px 30px rgba(8,183,109,0.06)}

/* Products grid */
.products{padding:10px 20px 60px}
.products h2{margin:0 0 12px 0;padding-left:6px}
.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
.card{background:linear-gradient(180deg,rgba(255,255,255,0.01),rgba(255,255,255,0.015));border-radius:12px;padding:14px;border:1px solid rgba(255,255,255,0.02);display:flex;flex-direction:column;gap:12px;min-height:340px;transition:transform .18s,box-shadow .18s}
.card:hover{transform:translateY(-8px);box-shadow:0 18px 50px rgba(8,183,109,0.08)}
.media{height:190px;border-radius:10px;overflow:hidden;display:grid;place-items:center;background:linear-gradient(135deg,rgba(255,255,255,0.02),rgba(255,255,255,0.01))}
.media img{width:100%;height:100%;object-fit:cover;display:block}
h3{margin:0;font-size:18px}
p.desc{margin:0;color:var(--muted);font-size:13px}
.price-row{margin-top:auto;display:flex;align-items:center;justify-content:space-between;gap:12px}
.price{font-weight:800;color:var(--emerald)}
.buy{background:transparent;border:1px solid rgba(255,255,255,0.04);padding:10px 12px;border-radius:10px;font-weight:800;color:var(--emerald);text-decoration:none;display:inline-block}
.buy:hover{background:rgba(8,183,109,0.06);transform:translateY(-3px)}

/* Footer */
.footer{padding:28px 20px;border-top:1px solid rgba(255,255,255,0.02);color:var(--muted);text-align:center}

/* Mobile */
.menu-toggle{display:none;background:none;border:0;color:var(--muted);font-size:20px}
@media (max-width:1024px){
  .hero{grid-template-columns:1fr;gap:20px;padding:28px 16px}
  .hero-left p{max-width:100%}
  .grid{grid-template-columns:repeat(2,1fr)}
}
@media (max-width:640px){
  .container{padding:12px}
  .nav{display:none}
  .menu-toggle{display:block}
  .grid{grid-template-columns:1fr}
  .logo{width:48px;height:48px}
  .hero-left h1{font-size:28px}
  .hero-left p{font-size:14px}
  .hero{padding:18px 12px}
  .media{height:220px}
  body{background:linear-gradient(180deg,#00060a,#071011)}
}

/* Utility */
.sr-only{position:absolute;width:1px;height:1px;padding:0;margin:-1px;overflow:hidden;clip:rect(0,0,0,0);white-space:nowrap;border:0}
.small{font-size:13px;color:var(--muted)}
</style>
</head>
<body>

<header class="header" role="banner">
  <div class="container">
    <div class="brand">
      <div class="logo" aria-hidden="true">
        <!-- Double-A luxury mark -->
        <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="LuxMart logo">
          <rect width="100" height="100" rx="14" fill="url(#g)"/>
          <defs>
            <linearGradient id="g" x1="0" x2="1" y1="0" y2="1">
              <stop offset="0" stop-color="#081612"/>
              <stop offset="1" stop-color="#06120f"/>
            </linearGradient>
          </defs>
          <g transform="translate(10,18)" stroke="#08b76d" stroke-width="6" stroke-linecap="round" stroke-linejoin="round" fill="none">
            <path d="M4 50 L26 6 L48 50" />
            <path d="M32 50 L54 6 L76 50" />
          </g>
        </svg>
      </div>
      <div>
        <div class="title">LuxMart</div>
        <div class="small">Beauty & Gadgets</div>
      </div>
    </div>

    <nav class="nav" role="navigation" aria-label="Main">
      <a href="#home">Home</a>
      <a href="#products">Products</a>
      <a href="#contact">Contact</a>
    </nav>

    <div style="display:flex;align-items:center;gap:10px">
      <button class="menu-toggle" aria-label="Open menu" onclick="openMobileMenu()">☰</button>
      <a class="cta" href="#products">Shop Now</a>
    </div>
  </div>
</header>

<main>
  <!-- HERO -->
  <section id="home" class="hero" aria-labelledby="hero-heading">
    <div class="hero-left">
      <div class="hero-card">
        <h1 id="hero-heading">Premium Beauty & Smart Gadgets</h1>
        <p>Curated collection of skincare and smart devices. Modern aesthetics. Elevated experience.</p>
        <div style="margin-top:14px;display:flex;gap:10px;flex-wrap:wrap">
          <a class="buy" href="#products">Explore Collection</a>
          <a class="buy" href="#contact">Get in Touch</a>
        </div>
      </div>
    </div>

    <aside>
      <div class="hero-card" style="display:flex;flex-direction:column;gap:12px">
        <div style="display:flex;gap:12px;align-items:center">
          <div style="width:56px;height:56px;border-radius:10px;display:grid;place-items:center;background:rgba(255,255,255,0.02)">★</div>
          <div>
            <div style="font-weight:700">Free shipping</div>
            <div class="small">On orders over $80</div>
          </div>
        </div>
        <div style="display:flex;gap:12px;align-items:center">
          <div style="width:56px;height:56px;border-radius:10px;display:grid;place-items:center;background:rgba(255,255,255,0.02)">🔒</div>
          <div>
            <div style="font-weight:700">Secure checkout</div>
            <div class="small">Trusted partners</div>
          </div>
        </div>
        <div style="display:flex;gap:12px;align-items:center">
          <div style="width:56px;height:56px;border-radius:10px;display:grid;place-items:center;background:rgba(255,255,255,0.02)">⭐</div>
          <div>
            <div style="font-weight:700">Top-rated picks</div>
            <div class="small">Hand-selected products</div>
          </div>
        </div>
      </div>
    </aside>
  </section>

  <!-- PRODUCTS -->
  <section id="products" class="products" aria-labelledby="products-heading">
    <div class="container">
      <h2 id="products-heading">Featured Products</h2>
      <div class="grid" id="productGrid">
        <!-- Repeatable card: replace images/productX.jpg and affiliate placeholder -->
        <article class="card" aria-label="Product 1">
          <div class="media">
            <img src="images/product1.jpg" alt="Emerald Glow Serum" loading="lazy" onerror="this.src='data:image/svg+xml;utf8,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22240%22 height=%22160%22><rect width=%22100%25%22 height=%22100%25%22 fill=%22%230b0f11%22/><text x=%2250%25%22 y=%2250%25%22 fill=%22%239aa6a8%22 font-size=%2214%22 text-anchor=%22middle%22 dy=%22.35em%22>Image</text></svg>'">
          </div>
          <h3>Emerald Glow Serum</h3>
          <p class="desc">Lightweight serum for radiant skin. 30ml.</p>
          <div class="price-row">
            <div class="price">$29</div>
            <a class="buy" href="https://s.click.aliexpress.com/e/PASTE-YOUR-LINK-HERE" target="_blank" rel="noopener noreferrer">Buy on AliExpress</a>
          </div>
        </article>

        <article class="card" aria-label="Product 2">
          <div class="media">
            <img src="images/product2.jpg" alt="Sonic Facial Cleansing Gadget" loading="lazy" onerror="this.src='data:image/svg+xml;utf8,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22240%22 height=%22160%22><rect width=%22100%25%22 height=%22100%25%22 fill=%22%230b0f11%22/><text x=%2250%25%22 y=%2250%25%22 fill=%22%239aa6a8%22 font-size=%2214%22 text-anchor=%22middle%22 dy=%22.35em%22>Image</text></svg>'">
          </div>
          <h3>Sonic Facial Cleansing Gadget</h3>
          <p class="desc">Ultra-soft bristles. Rechargeable. Waterproof.</p>
          <div class="price-row">
            <div class="price">$49</div>
            <a class="buy" href="https://s.click.aliexpress.com/e/PASTE-YOUR-LINK-HERE" target="_blank" rel="noopener noreferrer">Buy on AliExpress</a>
          </div>
        </article>

        <article class="card" aria-label="Product 3">
          <div class="media">
            <img src="images/product3.jpg" alt="Luxury Lip Tint" loading="lazy" onerror="this.src='data:image/svg+xml;utf8,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22240%22 height=%22160%22><rect width=%22100%25%22 height=%22100%25%22 fill=%22%230b0f11%22/><text x=%2250%25%22 y=%2250%25%22 fill=%22%239aa6a8%22 font-size=%2214%22 text-anchor=%22middle%22 dy=%22.35em%22>Image</text></svg>'">
          </div>
          <h3>Luxury Lip Tint</h3>
          <p class="desc">Long-lasting color with satin finish.</p>
          <div class="price-row">
            <div class="price">$19</div>
            <a class="buy" href="https://s.click.aliexpress.com/e/PASTE-YOUR-LINK-HERE" target="_blank" rel="noopener noreferrer">Buy on AliExpress</a>
          </div>
        </article>

        <article class="card" aria-label="Product 4">
          <div class="media">
            <img src="images/product4.jpg" alt="Smart Makeup Mirror" loading="lazy" onerror="this.src='data:image/svg+xml;utf8,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22240%22 height=%22160%22><rect width=%22100%25%22 height=%22100%25%22 fill=%22%230b0f11%22/><text x=%2250%25%22 y=%2250%25%22 fill=%22%239aa6a8%22 font-size=%2214%22 text-anchor=%22middle%22 dy=%22.35em%22>Image</text></svg>'">
          </div>
          <h3>Smart Makeup Mirror</h3>
          <p class="desc">LED lighting with color temperature control.</p>
          <div class="price-row">
            <div class="price">$89</div>
            <a class="buy" href="https://s.click.aliexpress.com/e/PASTE-YOUR-LINK-HERE" target="_blank" rel="noopener noreferrer">Buy on AliExpress</a>
          </div>
        </article>

        <article class="card" aria-label="Product 5">
          <div class="media">
            <img src="images/product5.jpg" alt="Rechargeable Eyelash Curler" loading="lazy" onerror="this.src='data:image/svg+xml;utf8,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22240%22 height=%22160%22><rect width=%22100%25%22 height=%22100%25%22 fill=%22%230b0f11%22/><text x=%2250%25%22 y=%2250%25%22 fill=%22%239aa6a8%22 font-size=%2214%22 text-anchor=%22middle%22 dy=%22.35em%22>Image</text></svg>'">
          </div>
          <h3>Rechargeable Eyelash Curler</h3>
          <p class="desc">Gentle heat curl for lasting lift.</p>
          <div class="price-row">
            <div class="price">$34</div>
            <a class="buy" href="https://s.click.aliexpress.com/e/PASTE-YOUR-LINK-HERE" target="_blank" rel="noopener noreferrer">Buy on AliExpress</a>
          </div>
        </article>

        <article class="card" aria-label="Product 6">
          <div class="media">
            <img src="images/product6.jpg" alt="Portable Facial Steamer" loading="lazy" onerror="this.src='data:image/svg+xml;utf8,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22240%22 height=%22160%22><rect width=%22100%25%22 height=%22100%25%22 fill=%22%230b0f11%22/><text x=%2250%25%22 y=%2250%25%22 fill=%22%239aa6a8%22 font-size=%2214%22 text-anchor=%22middle%22 dy=%22.35em%22>Image</text></svg>'">
          </div>
          <h3>Portable Facial Steamer</h3>
          <p class="desc">Compact. Fast steam for deep hydration.</p>
          <div class="price-row">
            <div class="price">$59</div>
            <a class="buy" href="https://s.click.aliexpress.com/e/PASTE-YOUR-LINK-HERE" target="_blank" rel="noopener noreferrer">Buy on AliExpress</a>
          </div>
        </article>

      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" style="max-width:var(--maxw);margin:0 auto 60px;padding:0 20px">
    <div class="hero-card">
      <h3>Contact Us</h3>
      <p class="small" style="margin:6px 0 12px">Questions or partnership requests. Replace with your contact handler if needed.</p>
      <form onsubmit="handleContact(event)" style="display:flex;gap:8px;flex-wrap:wrap">
        <input id="name" placeholder="Name" style="flex:1;min-width:180px;padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
        <input id="email" type="email" placeholder="Email" style="flex:1;min-width:220px;padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
        <input id="subject" placeholder="Subject" style="flex-basis:100%;padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
        <button class="cta" type="submit" style="margin-left:auto">Send</button>
      </form>
    </div>
  </section>
</main>

<footer class="footer">
  <div class="container" style="display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap">
    <div>© <span id="year"></span> LuxMart — All rights reserved</div>
    <div class="small">Made for your brand</div>
  </div>
</footer>

<script>
/* Year */
document.getElementById('year').textContent = new Date().getFullYear();

/* Mobile menu */
function openMobileMenu(){
  if(document.getElementById('mobileNav')){ document.getElementById('mobileNav').remove(); return; }
  const overlay = document.createElement('div');
  overlay.id = 'mobileNav';
  overlay.style.position = 'fixed';
  overlay.style.left = '12px';
  overlay.style.right = '12px';
  overlay.style.top = '72px';
  overlay.style.background = 'linear-gradient(180deg, rgba(255,255,255,0.02), transparent)';
  overlay.style.borderRadius = '12px';
  overlay.style.padding = '12px';
  overlay.style.zIndex = '999';
  overlay.style.boxShadow = '0 20px 50px rgba(0,0,0,0.6)';
  overlay.innerHTML = `
    <a href="#home" style="display:block;padding:12px 8px;color:var(--muted);text-decoration:none">Home</a>
    <a href="#products" style="display:block;padding:12px 8px;color:var(--muted);text-decoration:none">Products</a>
    <a href="#contact" style="display:block;padding:12px 8px;color:var(--muted);text-decoration:none">Contact</a>
  `;
  overlay.addEventListener('click', e => {
    if(e.target.tagName === 'A') overlay.remove();
  });
  document.body.appendChild(overlay);
}

/* Contact placeholder */
function handleContact(e){
  e.preventDefault();
  const n = document.getElementById('name').value || '—';
  const em = document.getElementById('email').value || '—';
  alert('Message queued. Name: ' + n + '\\nEmail: ' + em + '\\n(Replace alert with real backend or mailto link.)');
}

/* Smooth scroll */
document.querySelectorAll('a[href^="#"]').forEach(a=>{
  a.addEventListener('click', function(e){
    const href = this.getAttribute('href');
    if(!href || href === '#') return;
    const target = document.querySelector(href);
    if(target){ e.preventDefault(); target.scrollIntoView({behavior:'smooth',block:'start'}); }
  });
});
</script>
</body>
</html>
