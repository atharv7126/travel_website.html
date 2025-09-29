<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>WanderLite — Simple Travel Website</title>
  <style>
    :root{
      --accent:#0284c7;
      --muted:#6b7280;
      --bg:#f8fafc;
      --card:#ffffff;
      --radius:12px;
      font-family: system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
    }
    *{box-sizing:border-box}
    body{margin:0;background:var(--bg);color:#0f172a;line-height:1.4}
    header{background:linear-gradient(90deg,#0ea5e9, #0369a1);color:white;padding:18px 20px}
    .container{max-width:1100px;margin:0 auto;padding:18px}
    .nav{display:flex;align-items:center;justify-content:space-between;gap:12px}
    #logo{font-weight:700;letter-spacing:1px}
    nav ul{list-style:none;padding:0;margin:0;display:flex;gap:14px}
    nav a{color:rgba(255,255,255,0.95);text-decoration:none;font-weight:600}
    .btn{background:white;color:var(--accent);padding:8px 12px;border-radius:10px;font-weight:700;text-decoration:none}

    /* Hero */
    .hero{display:grid;grid-template-columns:1fr 420px;gap:22px;align-items:center;padding:40px 0}
    .hero h1{margin:0;font-size:34px}
    .hero p{color:var(--muted);margin:12px 0}
    .search-card{background:var(--card);padding:14px;border-radius:12px;box-shadow:0 6px 18px rgba(2,6,23,0.08)}
    .search-row{display:flex;gap:8px}
    .search-row input, .search-row select{flex:1;padding:10px;border-radius:8px;border:1px solid #e6eef6}
    .search-row button{background:var(--accent);color:white;border:none;padding:10px 14px;border-radius:8px;font-weight:700}

    /* Destinations */
    .section-title{display:flex;align-items:center;justify-content:space-between;margin:18px 0}
    .grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:16px}
    .card{background:var(--card);border-radius:12px;overflow:hidden;box-shadow:0 6px 18px rgba(2,6,23,0.06)}
    .card img{width:100%;height:140px;object-fit:cover;display:block}
    .card-body{padding:12px}
    .card-body h3{margin:0 0 6px 0;font-size:16px}
    .card-body p{margin:0;color:var(--muted);font-size:14px}

    /* Features */
    .features{display:grid;grid-template-columns:repeat(auto-fit,minmax(160px,1fr));gap:12px;margin-top:18px}
    .feature{background:linear-gradient(180deg,rgba(2,132,199,0.06),transparent);padding:12px;border-radius:10px}
    .feature h4{margin:6px 0 0 0}

    footer{padding:28px 0;color:var(--muted)}
    .footer-grid{display:flex;gap:24px;flex-wrap:wrap}

    /* Responsive */
    @media (max-width:900px){
      .hero{grid-template-columns:1fr}
      nav ul{display:none}
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <div id="logo">WanderLite</div>
      <nav>
        <ul>
          <li><a href="#destinations">Destinations</a></li>
          <li><a href="#deals">Deals</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
      <div>
        <a class="btn" href="#book">Book Now</a>
      </div>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <div>
        <h1>Find your next adventure</h1>
        <p>Hand-picked destinations, simple booking, and local tips. Explore cities, beaches, and hidden gems.</p>

        <div class="section-title">
          <h2 style="margin:0">Popular Destinations</h2>
          <a href="#destinations" style="color:var(--muted);text-decoration:none">View all →</a>
        </div>

        <div class="grid" id="destinations">
          <article class="card">
            <img src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=800&q=60" alt="Beach">
            <div class="card-body">
              <h3>Maldives Beaches</h3>
              <p>White sand, clear water — perfect for relaxing or snorkeling.</p>
            </div>
          </article>

          <article class="card">
            <img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?auto=format&fit=crop&w=800&q=60" alt="Mountains">
            <div class="card-body">
              <h3>Swiss Alps</h3>
              <p>Alpine hikes, cable cars and postcard views.</p>
            </div>
          </article>

          <article class="card">
            <img src="https://images.unsplash.com/photo-1491553895911-0055eca6402d?auto=format&fit=crop&w=800&q=60" alt="City">
            <div class="card-body">
              <h3>Paris, France</h3>
              <p>Romance, museums and great food.</p>
            </div>
          </article>

          <article class="card">
            <img src="https://images.unsplash.com/photo-1518684079-10f1a9e746c4?auto=format&fit=crop&w=800&q=60" alt="Desert">
            <div class="card-body">
              <h3>Dubai</h3>
              <p>Shopping, desert safaris and modern skylines.</p>
            </div>
          </article>
        </div>

        <div class="section-title" style="margin-top:18px">
          <h2 style="margin:0">Why book with us</h2>
        </div>
        <div class="features">
          <div class="feature">
            <strong>Best Price Guarantee</strong>
            <h4>Competitive rates &amp; deals</h4>
          </div>
          <div class="feature">
            <strong>24/7 Support</strong>
            <h4>We're here to help</h4>
          </div>
          <div class="feature">
            <strong>Hand-picked Stays</strong>
            <h4>Trusted hotels and hosts</h4>
          </div>
        </div>
      </div>

      <aside>
        <div class="search-card" id="book">
          <h3 style="margin-top:0">Search & Book</h3>
          <form onsubmit="event.preventDefault(); alert('Search submitted — replace this with real booking logic.');">
            <div style="margin-bottom:8px">
              <label style="font-size:13px;color:var(--muted)">Where</label>
              <input type="text" placeholder="City or destination" required />
            </div>
            <div style="margin-bottom:8px" class="search-row">
              <input type="date" required />
              <input type="date" required />
            </div>
            <div style="margin-bottom:8px" class="search-row">
              <select>
                <option>1 guest</option>
                <option>2 guests</option>
                <option>3 guests</option>
              </select>
              <button type="submit">Search</button>
            </div>
            <small style="color:var(--muted)">No payment here — this is a demo layout.</small>
          </form>
        </div>

        <div style="margin-top:12px;padding:12px;border-radius:10px;background:linear-gradient(180deg,#ffffff,#f1f5f9);box-shadow:0 6px 16px rgba(2,6,23,0.04)">
          <h4 style="margin:6px 0">Travel Tips</h4>
          <p style="margin:0;color:var(--muted);font-size:14px">Carry a copy of important documents and check visa rules before travel.</p>
        </div>
      </aside>
    </section>

    <section style="margin-top:30px" id="deals">
      <div class="section-title">
        <h2 style="margin:0">Hot Deals</h2>
        <a href="#" style="color:var(--muted);text-decoration:none">See all</a>
      </div>
      <div class="grid">
        <div class="card">
          <img src="https://images.unsplash.com/photo-1501117716987-c8e2b1a8b40a?auto=format&fit=crop&w=800&q=60" alt="Deal">
          <div class="card-body">
            <h3>7 nights in Bali</h3>
            <p>Starting from $499 — includes villa stay and airport pickup.</p>
          </div>
        </div>
        <div class="card">
          <img src="https://images.unsplash.com/photo-1549880338-65ddcdfd017b?auto=format&fit=crop&w=800&q=60" alt="Deal">
          <div class="card-body">
            <h3>Rome Weekend</h3>
            <p>3-night city break — museums and food tour.</p>
          </div>
        </div>
      </div>
    </section>

    <section style="margin-top:30px" id="contact">
      <div class="section-title">
        <h2 style="margin:0">Get in touch</h2>
      </div>
      <div style="display:grid;grid-template-columns:1fr 340px;gap:18px;align-items:start">
        <form style="background:var(--card);padding:16px;border-radius:12px;box-shadow:0 6px 18px rgba(2,6,23,0.04)" onsubmit="event.preventDefault(); alert('Thanks — message received (demo).');">
          <div style="display:flex;gap:8px;margin-bottom:8px">
            <input type="text" placeholder="Your name" required style="flex:1;padding:10px;border-radius:8px;border:1px solid #e6eef6" />
            <input type="email" placeholder="Email" required style="flex:1;padding:10px;border-radius:8px;border:1px solid #e6eef6" />
          </div>
          <textarea placeholder="How can we help?" required style="width:100%;padding:10px;border-radius:8px;border:1px solid #e6eef6;min-height:100px"></textarea>
          <div style="margin-top:8px">
            <button class="btn" type="submit">Send Message</button>
          </div>
        </form>

        <aside style="padding:12px">
          <div style="background:linear-gradient(180deg,#ffffff,#f8fafc);padding:12px;border-radius:10px;box-shadow:0 6px 16px rgba(2,6,23,0.04)">
            <h4 style="margin:4px 0">Office</h4>
            <p style="margin:4px 0;color:var(--muted);font-size:14px">123 Traveler Lane<br/>City, Country<br/>support@wanderlite.example</p>
          </div>
        </aside>
      </div>
    </section>

  </main>

  <footer>
    <div class="container">
      <div class="footer-grid">
        <div style="min-width:220px">
          <strong>WanderLite</strong>
          <p style="margin:6px 0;color:var(--muted)">Built with ❤️ for demo and learning purposes.</p>
        </div>
        <div style="color:var(--muted)">
          <small>© 2025 WanderLite</small>
        </div>
      </div>
    </div>
  </footer>

</body>
</html>
