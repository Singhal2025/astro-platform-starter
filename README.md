# Astro on Netlify Platform Starter

[Live Demo](https://astro-platform-starter.netlify.app/)

A modern starter based on Astro.js, Tailwind, and [Netlify Core Primitives](https://docs.netlify.com/core/overview/#develop) (Edge Functions, Image CDN, Blob Store).

## Astro Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## Deploying to Netlify

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/netlify-templates/astro-platform-starter)

## Developing Locally

| Prerequisites                                                                |
| :--------------------------------------------------------------------------- |
| [Node.js](https://nodejs.org/) v18.14+.                                      |
| (optional) [nvm](https://github.com/nvm-sh/nvm) for Node version management. |

1. Clone this repository, then run `npm install` in its root directory.

2. For the starter to have full functionality locally (e.g. edge functions, blob store), please ensure you have an up-to-date version of Netlify CLI. Run:

```
npm install netlify-cli@latest -g
```

3. Link your local repository to the deployed Netlify site. This will ensure you're using the same runtime version for both local development and your deployed site.

```
netlify link
```

4. Then, run the Astro.js development server via Netlify CLI:



```
netlify dev
```

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1.0" />
  <meta name="description" content="DOBARA – Scrap pickup & recycling in Raipur | Doorstep booking, instant payout" />
</head>
<body>
  <header>
        <nav>
     <H1 href1="#how">DOBARA - SCRAP MANAGEMENT COMPANY</H1>
             </nav> 
    </header>
  <BR>
    <header>
    <nav>
      <a href="#how">How It Works</a>
      <a href="#services">Services</a>
      <a href="#stats">Impact</a>
      <a href="#pickup">Book Pickup</a>
      <a href="#download" class="btn">Download App</a>
    </nav>
  </header>

  <!-- Hero Section -->
  <section class="hero container">
    <h1>Turn Your Waste Into Worth</h1>
    <p>Doortoorscrap pickup in Raipur—household, oil, vehicles, bulk—fast, transparent, eco-smart.</p>
    <a href="#pickup" class="btn">Book a Pickup</a>
  </section>

  <!-- How It Works -->
  <section id="how" class="features container">
    <div class="feature">
      <h3>1. Choose Material</h3>
      <p>Select household, metal, plastic, vehicle scrap or oil.</p>
    </div>
    <div class="feature">
      <h3>2. Schedule Pickup</h3>
      <p>Pick date & location. We dispatch verified agents.</p>
    </div>
    <div class="feature">
      <h3>3. Instant Payout</h3>
      <p>Agent weighs with digital scale, you get paid instantly.</p>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services" class="services container">
    <div class="service-card">
      <h3>Household Scrap</h3>
      <p>Paper, plastic, metal, glass – we collect it all.</p>
    </div>
    <div class="service-card">
      <h3>Vehicle Scrapping</h3>
      <p>₳ Clean, licensed vehicle end-of-life disposal.</p>
    </div>
    <div class="service-card">
      <h3>Cooking Oil Collection</h3>
      <p>Eco-friendly disposal with biodiesel partners.</p>
    </div>
    <div class="service-card">
      <h3>Bulk & Industrial</h3>
      <p>Office, factory, warehouse scrap service.</p>
    </div>
    <div class="service-card">
      <h3>Donation & CSR</h3>
      <p>Donate proceeds to NGOs – with tax receipts.</p>
    </div>
    <div class="service-card">
      <h3>Eco-Impact</h3>
      <p>Track recycled CO₂, trees saved, etc.</p>
    </div>
  </section>

  <!-- Impact Stats -->
  <section id="stats" class="stats container">
    <div class="stat-card">
      <h3>1,200+</h3>
      <p>Pickups Completed</p>
    </div>
    <div class="stat-card">
      <h3>50+</h3>
      <p>Tonnes Recycled</p>
    </div>
    <div class="stat-card">
      <h3>2,000 kg</h3>
      <p>Oil Collected</p>
    </div>
    <div class="stat-card">
      <h3>5</h3>
      <p>Zones Served</p>
    </div>
  </section>

  <!-- Testimonials -->
  <section class="testimonials container">
    <div class="testimonial">
      <blockquote>"Fast, reliable & eco-friendly. DOBARA made scrap pickup easy!"</blockquote>
      <cite>– Priya, Shankar Nagar</cite>
    </div>
    <div class="testimonial">
      <blockquote>"Loved the instant payment feature and tracking."</blockquote>
      <cite>– Ankit, Restaurant Owner</cite>
    </div>
    <div class="testimonial">
      <blockquote>"Our RWA partners appreciate the donation option."</blockquote>
      <cite>– Society Admin</cite>
    </div>
  </section>

  <!-- Pickup Form Section -->
  <section id="pickup" class="container">
    <h2 style="color:#27ae60; text-align:center; margin-bottom:20px;">Book Your Pickup</h2>
    <form class="pickup-form" onsubmit="handleSubmit(event)">
      <label for="name">Full Name</label>
      <input id="name" name="name" type="text" required />
      .
      <label for="mobile">Mobile Number</label>
      <input id="mobile" name="mobile" type="tel" pattern="[0-9]{10}" required />
      .
      <label for="location">Location</label>
      <input id="location" name="location" type="text" placeholder="Use address or pin code" required />
      .
      <label for="scrap">Scrap Type</label>
      <select id="scrap" name="scrap" required>
      .
        <option value="">Select</option>
        <option>Household</option><option>Metal/Industrial</option>
        <option>Vehicle</option><option>Cooking Oil</option>
      </select>
      <label for="schedule">Pickup Date</label>
      <input id="schedule" name="schedule" type="date" required />
      <button type="submit" class="btn">Submit Request</button>
    </form>
  </section>

  <!-- App Download Section -->
  <section id="download" class="container" style="text-align:center; margin:40px 0;">
    <h2 style="color:#27ae60; margin-bottom:15px;">Get the DOBARA App</h2>
    <p>For a seamless experience: live rates, wallet payouts & tracking</p>
    <a href="#" class="btn">Android Version</a>
    <a href="#" class="btn" style="margin-left:15px;">iOS Version</a>
  </section>

  <!-- Footer -->
  <footer>
    <p>Email: info@dobara.co.in | Phone: +91‑70001‑93040 | Raipur, Chhattisgarh</p>
    <p>&copy; 2025 SINGHAL REMETALS PRIVATE LIMITED (DOBARA)</p>
  </footer>
</body>
</html>


If your browser doesn't navigate to the site automatically, visit [localhost:8888](http://localhost:8888).
