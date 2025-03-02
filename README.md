<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>austinwrap | Unleash Your Web Vision</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
  <style>
    /* Reset & Core Styling */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Montserrat', sans-serif;
      background: linear-gradient(145deg, #0a0a14, #162038);
      color: #e6e6e6;
      line-height: 1.8;
      overflow-x: hidden;
      position: relative;
    }
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    /* Header Styling */
    header {
      text-align: center;
      padding: 100px 20px;
      position: relative;
      overflow: hidden;
    }
    header h1 {
      font-size: 4.5rem;
      font-weight: 900;
      letter-spacing: 3px;
      background: linear-gradient(90deg, #00f2ff, #ff007a);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      animation: glow 3s infinite alternate;
      text-shadow: 0 0 20px rgba(0, 242, 255, 0.6);
    }
    header p {
      font-size: 1.5rem;
      color: #d0d0d0;
      max-width: 600px;
      margin: 25px auto;
      opacity: 0;
      animation: fadeInUp 1s ease forwards 0.5s;
    }

    /* Particles Background */
    #particles {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
      background: rgba(0, 0, 0, 0.4);
    }

    /* Landing Button */
    .btn {
      display: inline-flex;
      align-items: center;
      background: linear-gradient(135deg, #00f2ff, #ff007a);
      color: #fff;
      padding: 20px 40px;
      margin: 30px 10px;
      border: none;
      border-radius: 50px;
      font-size: 1.3rem;
      font-weight: 700;
      text-transform: uppercase;
      cursor: pointer;
      transition: all 0.4s ease;
      box-shadow: 0 6px 25px rgba(0, 242, 255, 0.6);
    }
    .btn:hover {
      transform: translateY(-5px);
      box-shadow: 0 15px 35px rgba(0, 242, 255, 0.8);
    }
    .btn::before {
      content: "\f005";
      font-family: "Font Awesome 5 Free";
      font-weight: 900;
      margin-right: 12px;
    }

    /* Back Button */
    .back-btn {
      display: inline-block;
      background: linear-gradient(135deg, #ff007a, #00f2ff);
      color: #fff;
      padding: 14px 30px;
      margin: 25px 0;
      border-radius: 50px;
      font-size: 1.1rem;
      font-weight: 600;
      text-decoration: none;
      transition: all 0.4s ease;
      box-shadow: 0 5px 15px rgba(0, 242, 255, 0.4);
    }
    .back-btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 25px rgba(0, 242, 255, 0.6);
    }

    /* Pyramid Cards */
    .pyramid-grid {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 20px;
      padding: 40px 0;
    }
    .bubble-card {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
      background: linear-gradient(135deg, #00f2ff, #ff007a);
      color: #fff;
      border-radius: 25px;
      text-align: center;
      padding: 25px;
      font-size: 1.2rem;
      font-weight: 700;
      text-transform: uppercase;
      cursor: pointer;
      transition: all 0.4s ease;
      box-shadow: 0 6px 25px rgba(0, 242, 255, 0.5);
      text-decoration: none;
      position: relative;
      overflow: hidden;
    }
    .bubble-card:hover {
      transform: scale(1.05);
      box-shadow: 0 15px 35px rgba(0, 242, 255, 0.7);
    }
    .bubble-card span {
      font-size: 1.6rem;
      margin-top: 12px;
      font-weight: 900;
    }
    .bubble-card .features {
      font-size: 0.95rem;
      font-weight: 400;
      text-transform: none;
      margin-top: 15px;
      text-align: left;
    }
    .bubble-card .features ul {
      list-style: none;
      padding: 0;
    }
    .bubble-card .features li {
      margin: 6px 0;
    }
    /* Pyramid Sizes */
    .bubble-card.tier-0 { width: 280px; height: 220px; }
    .bubble-card.tier-50 { width: 340px; height: 260px; }
    .bubble-card.tier-99 { width: 400px; height: 300px; }
    .bubble-card.tier-200 { width: 460px; height: 340px; }
    .bubble-card.tier-500 { width: 520px; height: 400px; }

    /* Form Styling */
    form {
      background: rgba(255, 255, 255, 0.1);
      padding: 40px;
      border-radius: 20px;
      box-shadow: 0 10px 40px rgba(0, 0, 0, 0.5);
      backdrop-filter: blur(15px);
      max-width: 700px;
      margin: 0 auto;
    }
    form label {
      font-size: 1.2rem;
      font-weight: 700;
      color: #00f2ff;
      margin-bottom: 12px;
      display: block;
    }
    form input, form textarea {
      width: 100%;
      padding: 16px;
      margin-bottom: 25px;
      border: 2px solid rgba(255, 255, 255, 0.2);
      border-radius: 10px;
      background: rgba(255, 255, 255, 0.05);
      color: #fff;
      font-size: 1.1rem;
      transition: border 0.3s ease, box-shadow 0.3s ease;
    }
    form input:focus, form textarea:focus {
      border-color: #ff007a;
      box-shadow: 0 0 12px rgba(255, 0, 122, 0.6);
      outline: none;
    }
    form textarea {
      resize: vertical;
      max-height: 320px;
    }
    form button {
      width: 100%;
      padding: 20px;
      border: none;
      border-radius: 50px;
      background: linear-gradient(135deg, #28a745, #00f2ff);
      color: #fff;
      font-size: 1.3rem;
      font-weight: 700;
      cursor: pointer;
      transition: all 0.4s ease;
      box-shadow: 0 6px 25px rgba(40, 167, 69, 0.6);
    }
    form button:hover {
      background: linear-gradient(135deg, #1e7e34, #00d4ff);
      transform: translateY(-5px);
      box-shadow: 0 15px 35px rgba(40, 167, 69, 0.8);
    }
    form button::before {
      content: "\f005";
      font-family: "Font Awesome 5 Free";
      font-weight: 900;
      margin-right: 12px;
    }

    /* Popup Styling */
    .popup {
      position: fixed;
      bottom: 25px;
      right: 25px;
      background: linear-gradient(135deg, #ff007a, #00f2ff);
      color: #fff;
      padding: 18px 25px;
      border-radius: 20px;
      font-size: 1rem;
      font-weight: 600;
      max-width: 320px;
      box-shadow: 0 6px 20px rgba(0, 0, 0, 0.5);
      z-index: 100;
      animation: slideInPopup 0.5s ease forwards;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .popup::before {
      content: "\f0a1";
      font-family: "Font Awesome 5 Free";
      font-weight: 900;
      margin-right: 12px;
    }
    .popup .close-btn {
      background: none;
      border: none;
      color: #fff;
      font-size: 1.1rem;
      cursor: pointer;
      margin-left: 12px;
    }

    /* Section Styling */
    .section {
      display: none;
      padding: 80px 0;
      animation: slideIn 0.8s ease forwards;
    }
    .active {
      display: block;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 50px 0;
      font-size: 1.1rem;
      color: #a0a0a0;
      border-top: 1px solid rgba(255, 255, 255, 0.2);
    }

    /* Animations */
    @keyframes glow {
      0% { text-shadow: 0 0 15px #00f2ff; }
      100% { text-shadow: 0 0 25px #ff007a; }
    }
    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes slideIn {
      from { opacity: 0; transform: translateX(-50px); }
      to { opacity: 1; transform: translateX(0); }
    }
    @keyframes slideInPopup {
      from { opacity: 0; transform: translateY(100px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* iPhone Optimization */
    @media (max-width: 768px) {
      header { padding: 60px 15px; }
      header h1 { font-size: 3.5rem; }
      header p { font-size: 1.2rem; max-width: 90%; }
      .btn { padding: 16px 32px; font-size: 1.1rem; }
      .pyramid-grid { gap: 15px; }
      .bubble-card { font-size: 1rem; padding: 20px; }
      .bubble-card.tier-0 { width: 250px; height: 200px; }
      .bubble-card.tier-50 { width: 300px; height: 240px; }
      .bubble-card.tier-99 { width: 350px; height: 280px; }
      .bubble-card.tier-200 { width: 400px; height: 320px; }
      .bubble-card.tier-500 { width: 450px; height: 360px; }
      .bubble-card .features { font-size: 0.9rem; }
      form { padding: 30px; max-width: 100%; }
      form input, form textarea { font-size: 1rem; padding: 14px; }
      form button { font-size: 1.2rem; padding: 16px; }
      footer { font-size: 1rem; padding: 40px 0; }
      .popup { max-width: 280px; font-size: 0.9rem; }
    }
    @media (max-width: 375px) {
      header h1 { font-size: 2.5rem; }
      header p { font-size: 1rem; }
      .btn { padding: 14px 28px; font-size: 1rem; }
      .pyramid-grid { gap: 12px; }
      .bubble-card { width: 100% !important; font-size: 0.9rem; padding: 15px; }
      .bubble-card.tier-0 { height: 180px; }
      .bubble-card.tier-50 { height: 220px; }
      .bubble-card.tier-99 { height: 260px; }
      .bubble-card.tier-200 { height: 300px; }
      .bubble-card.tier-500 { height: 340px; }
      .bubble-card .features { font-size: 0.85rem; }
      form { padding: 25px; }
      form input, form textarea { padding: 12px; }
      form button { padding: 14px; font-size: 1.1rem; }
      .popup { bottom: 20px; right: 20px; padding: 12px 20px; max-width: 250px; }
    }
  </style>
</head>
<body>
  <div id="particles"></div>
  <div class="container">
    <!-- Landing Page -->
    <section id="landing" class="active">
      <header>
        <h1>austinwrap</h1>
        <p>We help beginners launch their website today—tell us your idea!</p>
        <button class="btn" id="enterBtn">Get Started</button>
      </header>
    </section>

    <!-- Packages Screen -->
    <section id="packages" class="section">
      <a href="#" class="back-btn" id="packages-back">Back to Home</a>
      <header>
        <h1>Your Options</h1>
        <p>Get a custom email packet tailored to your website vision.</p>
      </header>
      <div class="pyramid-grid">
        <a href="#consultation?package=Quick Start Guide" class="bubble-card tier-0">
          Quick Start Guide <span>$0</span>
          <div class="features">
            <ul>
              <li>Basic email guide</li>
              <li>Intro to website basics</li>
            </ul>
          </div>
        </a>
        <a href="#consultation?package=AI Starter Pack" class="bubble-card tier-50">
          AI Starter Pack <span>$50</span>
          <div class="features">
            <ul>
              <li>Detailed email packet</li>
              <li>AI tool basics (ChatGPT, etc.)</li>
              <li>Simple website steps</li>
            </ul>
          </div>
        </a>
        <a href="#consultation?package=DIY Launch Guide" class="bubble-card tier-99">
          DIY Launch Guide <span>$99</span>
          <div class="features">
            <ul>
              <li>Comprehensive email guide</li>
              <li>AI idea generation</li>
              <li>Step-by-step creation</li>
              <li>Launch instructions</li>
            </ul>
          </div>
        </a>
        <a href="#consultation?package=Pro Website Blueprint" class="bubble-card tier-200">
          Pro Website Blueprint <span>$200</span>
          <div class="features">
            <ul>
              <li>Advanced email packet</li>
              <li>AI tool mastery</li>
              <li>Detailed website plan</li>
              <li>Optimization tips</li>
              <li>Launch strategy</li>
            </ul>
          </div>
        </a>
        <a href="#consultation?package=Complete Launch Kit" class="bubble-card tier-500">
          Complete Launch Kit <span>$500</span>
          <div class="features">
            <ul>
              <li>Premium email packet</li>
              <li>Full AI integration guide</li>
              <li>Custom website blueprint</li>
              <li>Launch plan with domain</li>
              <li>Email setup instructions</li>
              <li>Optional clarification call</li>
            </ul>
          </div>
        </a>
      </div>
    </section>

    <!-- Consultation Form -->
    <section id="consultation" class="section">
      <a href="#" class="back-btn" id="consultation-back">Back to Home</a>
      <header>
        <h1>Tell Us Your Vision</h1>
        <p>Describe your website idea in 1000 words or less—be creative! We’ll send you a custom email packet.</p>
      </header>
      <form id="contactForm">
        <label for="name">Your Name:</label>
        <input type="text" id="name" name="name" placeholder="Enter your full name" required />

        <label for="email">Your Email:</label>
        <input type="email" id="email" name="email" placeholder="you@example.com" required />

        <label for="phone">Your Phone Number (Optional, for clarification if needed):</label>
        <input type="tel" id="phone" name="phone" placeholder="e.g., 123-456-7890" />

        <label for="venmo" id="venmo-label">Your Venmo (Username or Link, Required for Paid Tiers):</label>
        <input type="text" id="venmo" name="venmo" placeholder="e.g., @username or https://venmo.com/username" />

        <label for="package">Selected Package:</label>
        <input type="text" id="package" name="package" placeholder="Your chosen package" readonly />

        <label for="website">Desired Website Name (Optional):</label>
        <input type="text" id="website" name="website" placeholder="e.g., www.mywebsite.com" />

        <label for="details">Your Website Idea (1000 words or less):</label>
        <textarea id="details" name="details" rows="8" maxlength="4000" placeholder="Tell us everything—your wildest ideas, goals, and details (1000 words max)!" required></textarea>

        <button type="submit">Send Your Idea</button>
      </form>
    </section>

    <!-- Popup -->
    <div class="popup" id="popup">
      <span>This site brings your wildest website ideas to life today!</span>
      <button class="close-btn" id="close-popup">✖</button>
    </div>

    <footer>
      <p>© 2025 austinwrap. Crafted with brilliance. All rights reserved.</p>
    </footer>
  </div>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/particles.js/2.0.0/particles.min.js"></script>
  <script>
    // Page Transitions
    const landing = document.getElementById('landing');
    const packages = document.getElementById('packages');
    const consultation = document.getElementById('consultation');
    const packageInput = document.getElementById('package');
    const venmoInput = document.getElementById('venmo');
    const venmoLabel = document.getElementById('venmo-label');
    const contactForm = document.getElementById('contactForm');

    document.getElementById('enterBtn').addEventListener('click', function () {
      landing.style.display = 'none';
      packages.classList.add('active');
      window.scrollTo({ top: 0, behavior: 'smooth' });
    });

    document.getElementById('packages-back').addEventListener('click', function (e) {
      e.preventDefault();
      packages.classList.remove('active');
      landing.style.display = 'block';
      landing.classList.add('active');
      window.scrollTo({ top: 0, behavior: 'smooth' });
    });

    document.getElementById('consultation-back').addEventListener('click', function (e) {
      e.preventDefault();
      consultation.classList.remove('active');
      landing.style.display = 'block';
      landing.classList.add('active');
      window.scrollTo({ top: 0, behavior: 'smooth' });
    });

    document.querySelectorAll('.bubble-card').forEach(card => {
      card.addEventListener('click', function (e) {
        e.preventDefault();
        const href = this.getAttribute('href');
        const packageName = href.split('=')[1].replace(/%20/g, ' ');
        packageInput.value = packageName;
        packages.classList.remove('active');
        consultation.classList.add('active');
        if (packageName === 'Quick Start Guide') {
          venmoInput.style.display = 'none';
          venmoLabel.style.display = 'none';
          venmoInput.required = false;
        } else {
          venmoInput.style.display = 'block';
          venmoLabel.style.display = 'block';
          venmoInput.required = true;
        }
        window.scrollTo({ top: 0, behavior: 'smooth' });
      });
    });

    // Form Submission - Generate Drafted Email
    contactForm.addEventListener('submit', function (e) {
      e.preventDefault();
      const name = document.getElementById('name').value;
      const email = document.getElementById('email').value;
      const phone = document.getElementById('phone').value || 'Not provided';
      const venmo = packageInput.value === 'Quick Start Guide' ? 'Not applicable' : document.getElementById('venmo').value;
      const package = packageInput.value;
      const website = document.getElementById('website').value || 'Not provided';
      const details = document.getElementById('details').value;

      const subject = `Website Idea Submission - ${name}`;
      const body = `
austinwrap Website Idea Submission
=====================================

**Name:** ${name}
**Email:** ${email}
**Phone Number:** ${phone}
**Venmo (Username or Link):** ${venmo}
**Selected Package:** ${package}
**Desired Website Name:** ${website}

**Website Idea (1000 words or less):**
${details}

=====================================
Thank you for choosing austinwrap! We'll craft your custom email packet based on this info.
      `.trim();

      const mailtoLink = `mailto:aytmout@gmail.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
      window.location.href = mailtoLink;
    });

    // Popup Handling
    const popup = document.getElementById('popup');
    const closePopup = document.getElementById('close-popup');
    closePopup.addEventListener('click', function () {
      popup.style.display = 'none';
    });
    setTimeout(() => {
      popup.style.display = 'none';
    }, 5000);

    // Particles Background
    particlesJS('particles', {
      particles: {
        number: { value: 80, density: { enable: true, value_area: 800 } },
        color: { value: '#00f2ff' },
        shape: { type: 'circle' },
        opacity: { value: 0.7, random: true },
        size: { value: 5, random: true },
        line_linked: { enable: true, distance: 140, color: '#ff007a', opacity: 0.6, width: 1.8 },
        move: { enable: true, speed: 4, direction: 'none', random: false, straight: false, out_mode: 'out' }
      },
      interactivity: {
        detect_on: 'canvas',
        events: { onhover: { enable: true, mode: 'repulse' }, onclick: { enable: true, mode: 'push' }, resize: true },
        modes: { repulse: { distance: 100, duration: 0.4 }, push: { particles_nb: 4 } }
      },
      retina_detect: true
    });
  </script>
</body>
</html>
