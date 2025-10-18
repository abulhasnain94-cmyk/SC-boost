<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Social Boost — Social Media Management</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header class="hero" id="home">
    <nav class="nav">
      <div class="brand">Social Boost</div>
      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#service">Service</a></li>
        <li><a href="#packages">Package</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <button class="cta" id="get-started">Get Started</button>
    </nav>

    <div class="hero-content">
      <h1>Grow your presence. Boost your brand.</h1>
      <p>Social Boost offers friendly, data-driven social media management for small businesses.</p>
      <div class="promo-row">
        <input id="promo" placeholder="Enter promotion code" />
        <button onclick="applyPromo()">Apply</button>
      </div>
      <div class="hero-actions">
        <a href="#packages" class="btn">See Packages</a>
        <a href="#contact" class="btn ghost">Contact Us</a>
      </div>
    </div>

    <div class="hero-video">
      <video autoplay muted loop playsinline id="promoVideo1" width="420" height="236">
        <source src="promo1.mp4" type="video/mp4">
        Your browser does not support HTML5 video.
      </video>
      <video autoplay muted loop playsinline id="promoVideo2" width="420" height="236">
        <source src="promo2.mp4" type="video/mp4">
        Your browser does not support HTML5 video.
      </video>
    </div>
  </header>

  <main>
    <section id="service" class="section service">
      <h2>Our Service</h2>
      <p>Social Boost manages posting, engagement, and content strategy so you can focus on running your business.
         We create eye-catching visuals, write conversion-focused captions, and monitor analytics to grow engagement.</p>
      <ul class="service-list">
        <li><strong>Content creation</strong> — branded images, short videos, and carousel posts.</li>
        <li><strong>Community engagement</strong> — comment replies, DM triage, and audience growth.</li>
        <li><strong>Performance reporting</strong> — monthly reports with clear KPIs and action items.</li>
      </ul>
    </section>

    <section id="packages" class="section packages">
      <h2>Packages</h2>
      <p>Choose a plan that fits your goals. All packages include a strategy call and monthly reporting.</p>
      <div class="cards">
        <div class="card">
          <h3>Small</h3>
          <p class="price">£450 / month</p>
          <ul>
            <li>8 posts per month</li>
            <li>Basic analytics</li>
            <li>1 platform</li>
          </ul>
          <button class="select" onclick="selectPackage('Small',450)">Select</button>
        </div>

        <div class="card featured">
          <h3>Medium</h3>
          <p class="price">£650 / month</p>
          <ul>
            <li>12 posts per month</li>
            <li>Enhanced visuals + 1 short video</li>
            <li>2 platforms</li>
          </ul>
          <button class="select" onclick="selectPackage('Medium',650)">Select</button>
        </div>

        <div class="card">
          <h3>Large</h3>
          <p class="price">£850 / month</p>
          <ul>
            <li>20 posts per month</li>
            <li>Custom video content</li>
            <li>3 platforms + ads guidance</li>
          </ul>
          <button class="select" onclick="selectPackage('Large',850)">Select</button>
        </div>
      </div>
    </section>

    <section id="contact" class="section contact">
      <h2>Contact</h2>
      <p>Ready to boost your social presence? Send us a message and we'll get back within 48 hours.</p>
      <form id="contactForm" onsubmit="submitForm(event)">
        <label>
          Name
          <input type="text" id="name" required />
        </label>
        <label>
          Email
          <input type="email" id="email" required />
        </label>
        <label>
          Message
          <textarea id="message" rows="4" required></textarea>
        </label>
        <button type="submit" class="btn">Send Message</button>
      </form>
      <div class="contact-info">
        <p><strong>Email:</strong> hello@socialboost.example</p>
        <p><strong>Phone:</strong> +44 20 7946 0958</p>
      </div>
    </section>
  </main>

  <footer>
    <p>© Social Boost — Simple social media management for small businesses.</p>
    <div class="foot-links">
      <a href="#">Privacy</a> · <a href="#">Terms</a>
    </div>
  </footer>

  <script src="script.js"></script>
</body>
</html>

:root{
  --pink:#ff6fa3;
  --purple:#8b5cf6;
  --lightblue:#67e8f9;
  --bg: linear-gradient(135deg, rgba(139,92,246,0.08), rgba(255,111,163,0.06));
  --card-bg: rgba(255,255,255,0.9);
  --max-width:1100px;
}
*{box-sizing:border-box}
body{
  margin:0;
  font-family:Inter,ui-sans-serif,system-ui,-apple-system,"Segoe UI",Roboto,"Helvetica Neue",Arial;
  color:#222;
  background:radial-gradient(circle at 10% 10%, rgba(255,111,163,0.06), transparent 10%), #f8fbff;
  -webkit-font-smoothing:antialiased;
}

/* Navigation */
.nav{
  display:flex;align-items:center;justify-content:space-between;
  padding:18px 24px;max-width:var(--max-width);margin:0 auto;
}
.brand{font-weight:700;color:var(--purple);font-size:20px}
.nav-links{list-style:none;display:flex;gap:14px;margin:0;padding:0}
.nav-links a{color:#333;text-decoration:none;padding:8px 10px;border-radius:8px}
.cta{background:linear-gradient(90deg,var(--pink),var(--purple));color:white;border:none;padding:8px 12px;border-radius:10px;cursor:pointer}

/* Hero */
.hero{
  display:grid;grid-template-columns:1fr 420px;gap:20px;
  padding:40px 24px;align-items:center;max-width:var(--max-width);
  margin:10px auto;border-radius:18px;background:var(--bg);
}
.hero-content h1{
  font-size:34px;margin:0 0 8px;
  background:linear-gradient(90deg,var(--purple),var(--pink));
  -webkit-background-clip:text;color:transparent;
}
.hero-content p{margin:0 0 16px;color:#444}
.promo-row{display:flex;gap:8px;margin:12px 0}
.promo-row input{padding:10px;border-radius:10px;border:1px solid rgba(0,0,0,0.08);min-width:180px}
.hero-actions{display:flex;gap:12px;margin-top:10px}
.btn{background:linear-gradient(90deg,var(--purple),var(--pink));color:white;padding:10px 14px;border-radius:10px;text-decoration:none}
.btn.ghost{background:transparent;border:1px solid rgba(0,0,0,0.06);color:#333}

/* Hero videos */
.hero-video{display:flex;flex-direction:column;gap:12px;align-items:center}
.hero-video video{border-radius:12px;box-shadow:0 6px 22px rgba(139,92,246,0.12)}

/* Sections */
.section{padding:48px 24px;max-width:var(--max-width);margin:0 auto}
.section h2{font-size:26px;color:var(--purple);margin-bottom:8px}
.service-list{margin-top:12px}
.packages .cards{display:flex;gap:16px;flex-wrap:wrap}
.card{background:var(--card-bg);padding:18px;border-radius:14px;flex:1;min-width:220px;box-shadow:0 6px 18px rgba(0,0,0,0.05)}
.card.featured{border:2px solid rgba(139,92,246,0.12);transform:translateY(-6px)}
.price{font-weight:800;font-size:18px;color:var(--pink)}

/* Contact */
.contact form{display:grid;gap:10px;max-width:560px}
.contact input,.contact textarea{padding:10px;border-radius:10px;border:1px solid rgba(0,0,0,0.08)}
.contact .btn{width:160px}

/* Footer */
footer{padding:18px 24px;text-align:center;color:#666;margin-top:24px}
.foot-links{margin-top:8px}

/* Responsive */
@media(max-width:900px){
  .hero{grid-template-columns:1fr; text-align:center}
  .hero-video{flex-direction:row;justify-content:center}
  .nav-links{display:none}
}

function applyPromo(){
  const code = document.getElementById('promo').value.trim();
  if(!code){ alert('Please enter a promotion code. Example: BOOST10'); return; }
  if(code.toUpperCase().includes('BOOST')){
    alert('Promo applied: 10% off your first month!');
  } else {
    alert('Promo code not recognized. Contact us for custom offers.');
  }
}

function selectPackage(name,price){
  const confirmed = confirm('Select ' + name + ' package for £' + price + '/month?');
  if(confirmed){
    location.hash = '#contact';
    setTimeout(()=> {
      document.getElementById('message').value = `Hi — I'd like the ${name} package (£${price}/month). Please contact me with next steps.`;
    },400);
  }
}

function submitForm(e){
  e.preventDefault();
  const name = document.getElementById('name').value;
  const email = document.getElementById('email').value;
  const message = document.getElementById('message').value;
  alert('Thanks ' + name + "! We'll contact you at " + email + " — message received.");
  document.getElementById('contactForm').reset();
}
