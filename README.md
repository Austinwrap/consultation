<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>austinwrap | Your Web Vision Unleashed</title>
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
      background: linear-gradient(145deg, #0f0f1a, #1e2a44);
      color: #e0e0e0;
      line-height: 1.8;
      overflow-x: hidden;
      position: relative;
    }
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 15px;
    }

    /* Header Styling */
    header {
      text-align: center;
      padding: 80px 15px;
      position: relative;
      overflow: hidden;
    }
    header h1 {
      font-size: 4rem;
      font-weight: 900;
      letter-spacing: 2px;
      background: linear-gradient(90deg, #00eaff, #ff1a8c);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      animation: glow 3s infinite alternate;
      text-shadow: 0 0 15px rgba(0, 234, 255, 0.5);
    }
    header p {
      font-size: 1.4rem;
      color: #c0c0c0;
      max-width: 550px;
      margin: 20px auto;
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
      background: rgba(0, 0, 0, 0.3);
    }

    /* Landing Button */
    .btn {
      display: inline-flex;
      align-items: center;
      background: linear-gradient(135deg, #00eaff, #ff1a8c);
      color: #fff;
      padding: 18px 35px;
      margin: 25px 10px;
      border: none;
      border-radius: 50px;
      font-size: 1.2rem;
      font-weight: 700;
      text-transform: uppercase;
      cursor: pointer;
      transition: all 0.4s ease;
      box-shadow: 0 5px 20px rgba(0, 234, 255, 0.5);
    }
    .btn:hover {
      transform: translateY(-5px);
      box-shadow: 0 15px 30px rgba(0, 234, 255, 0.7);
    }
    .btn::before {
      content: "\f005";
      font-family: "Font Awesome 5 Free";
      font-weight: 900;
      margin-right: 10px;
    }

    /* Back Button */
    .back-btn {
      display: inline-block;
      background: linear-gradient(135deg, #ff1a8c, #00eaff);
      color: #fff;
      padding: 12px 25px;
      margin: 20px 0;
      border-radius: 50px;
      font-size: 1rem;
      font-weight: 600;
      text-decoration: none;
      transition: all 0.4s ease;
      box-shadow: 0 5px 15px rgba(0, 234, 255, 0.4);
    }
    .back-btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 20px rgba(0, 234, 255, 0.6);
    }

    /* Rectangular Cards */
    .bubble-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 25px;
      padding: 30px 0;
      justify-items: center;
    }
    .bubble-card {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
      background: linear-gradient(135deg, #00eaff, #ff1a8c);
      color: #fff;
      border-radius: 20px;
      text-align: center;
      padding: 20px;
      font-size: 1.1rem;
      font-weight: 700;
      text-transform: uppercase;
      cursor: pointer;
      transition: all 0.4s ease;
      box-shadow: 0 5px 20px rgba(0, 234, 255, 0.4);
      text-decoration: none;
      position: relative;
      overflow: hidden;
    }
    .bubble-card:hover {
      transform: scale(1.05);
      box-shadow: 0 15px 30px rgba(0, 234, 255, 0.7);
    }
    .bubble-card span {
      font-size: 1.5rem;
      margin-top: 10px;
      font-weight: 900;
    }
    .bubble-card .features {
      font-size: 0.9rem;
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
      margin: 5px 0;
    }
    /* Size Scaling by Price */
    .bubble-card.tier-0 { width: 280px; height: 220px; }
    .bubble-card.tier-50 { width: 300px; height: 260px; }
    .bubble-card.tier-99 { width: 320px; height: 300px; }
    .bubble-card.tier-200 { width: 340px; height: 340px; }
    .bubble-card.tier-500 { width: 360px; height: 400px; }

    /* Form Styling */
    form {
      background: rgba(255, 255, 255, 0.08);
      padding: 35px;
      border-radius: 15px;
      box-shadow: 0 10px 35px rgba(0, 0, 0, 0.4);
      backdrop-filter: blur(12px);
      max-width: 650px;
      margin: 0 auto;
    }
    form label {
      font-size: 1.1rem;
      font-weight: 700;
      color: #00eaff;
      margin-bottom: 10px;
      display: block;
    }
    form input, form textarea {
      width: 100%;
      padding: 14px;
      margin-bottom: 20px;
      border: 2px solid rgba(255, 255, 255, 0.15);
      border-radius: 8px;
      background: rgba(255, 255, 255, 0.05);
      color: #fff;
      font-size: 1rem;
      transition: border 0.3s ease, box-shadow 0.3s ease;
    }
    form input:focus, form textarea:focus {
      border-color: #ff1a8c;
      box-shadow: 0 0 10px rgba(255, 26, 140, 0.5);
      outline: none;
    }
    form textarea {
      resize: vertical;
      max-height: 300px;
    }
    form button {
      width: 100%;
      padding: 18px;
      border: none;
      border-radius: 50px;
      background: linear-gradient(135deg, #28a745, #00eaff);
      color: #fff;
      font-size: 1.2rem;
      font-weight: 700;
      cursor: pointer;
      transition: all 0.4s ease;
      box-shadow: 0 5px 20px rgba(40, 167, 69, 0.5);
    }
    form button:hover {
      background: linear-gradient(135deg, #1e7e34, #00ccff);
      transform: translateY(-5px);
      box-shadow: 0 15px 30px rgba(40, 167, 69, 0.7);
    }
    form button::before {
      content: "\f005";
      font-family: "Font Awesome 5 Free";
      font-weight: 900;
      margin-right: 10px;
    }

    /* Popup Styling */
    .popup {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: linear-gradient(135deg, #ff1a8c, #00eaff);
      color: #fff;
      padding: 15px 20px;
      border-radius: 15px;
      font-size: 0.9rem;
      font-weight: 600;
      max-width: 300px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
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
      margin-right: 10px;
    }
    .popup .close-btn {
      background: none;
      border: none;
      color: #fff;
      font-size: 1rem;
      cursor: pointer;
      margin-left: 10px;
    }

    /* Section Styling */
    .section {
      display: none;
      padding: 60px 0;
      animation: slideIn 0.8s ease forwards;
    }
    .active {
      display: block;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 40px 0;
      font-size: 1rem;
      color: #999;
      border-top: 1px solid rgba(255, 255, 255, 0.15);
    }

    /* Animations */
    @keyframes glow {
      0% { text-shadow: 0 0 15px #00eaff; }
      100% { text-shadow: 0 0 25px #ff1a8c; }
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
      header { padding: 50px 10px; }
      header h1 { font-size: 3rem; }
      header p { font-size: 1.1rem; max-width: 90%; }
      .btn { padding: 14px 28px; font-size: 1rem; }
      .bubble-grid { grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; }
      .bubble-card { font-size: 1rem; }
      .bubble-card.tier-0 { width: 250px; height: 200px; }
      .bubble-card.tier-50 { width: 270px; height: 240px; }
      .bubble-card.tier-99 { width: 290px; height: 280px; }
      .bubble-card.tier-200 { width: 310px; height: 320px; }
      .bubble-card.tier-500 { width: 330px; height: 360px; }
      .bubble-card .features { font-size: 0.85rem; }
      form { padding: 25px; max-width: 100%; }
      form input, form textarea { font-size: 0.95rem; padding: 12px; }
      form button { font-size: 1.1rem; padding: 14px; }
      footer { font-size: 0.9rem; padding: 30px 0; }
      .popup { max-width: 250px; font-size: 0.85rem; }
    }
    @media (max-width: 375px) {
      header h1 { font-size: 2.2rem; }
      header p { font-size: 0.95rem; }
      .btn { padding: 12px 24px; font-size: 0.9rem; }
      .bubble-grid { grid-template-columns: 1fr; gap: 15px; }
      .bubble-card { width: 100%; font-size: 0.9rem; }
      .bubble-card.tier-0 { height: 180px; }
      .bubble-card.tier-50 { height: 220px; }
      .bubble-card.tier-99 { height: 260px; }
      .bubble-card.tier-200 { height: 300px; }
      .bubble-card.tier-500 { height: 340px; }
      .bubble-card .features { font-size: 0.8rem; }
      form { padding: 20px; }
      form input, form textarea { padding: 10px; }
      form button { padding: 12px; font-size: 1rem; }
      .popup { bottom: 15px; right: 15px; padding: 10px 15px; }
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
        <p>Get a custom email packet tailored to your website idea.</p>
      </header>
      <div class="bubble-grid">
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
      <form id="contactForm" action="mailto:aytmout@gmail.com" method="post" enctype="text/plain">
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
      <p>© 2025 austinwrap. Forged in brilliance. All rights reserved.</p>
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
        number: { value: 60, density: { enable: true, value_area: 800 } },
        color: { value: '#00eaff' },
        shape: { type: 'circle' },
        opacity: { value: 0.6, random: true },
        size: { value: 4, random: true },
        line_linked: { enable: true, distance: 130, color: '#ff1a8c', opacity: 0.5, width: 1.5 },
        move: { enable: true, speed: 3, direction: 'none', random: false, straight: false, out_mode: 'out' }
      },
      interactivity: {
        detect_on: 'canvas',
        events: { onhover: { enable: true, mode: 'repulse' }, onclick: { enable: true, mode: 'push' }, resize: true },
        modes: { repulse: { distance: 80, duration: 0.4 }, push: { particles_nb: 4 } }
      },
      retina_detect: true
    });
  </script>
</body>
</html>
