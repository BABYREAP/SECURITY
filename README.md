<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="CyberPhantom — Digital security, website protection and cybersecurity consulting.">
<title>CyberPhantom — Digital Security, Refined.</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Manrope:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root {
  --bg: #080909;
  --surface: #101111;
  --surface2: #151616;
  --border: rgba(255,255,255,.09);
  --text: #eeeeee;
  --muted: #929595;
  --red: #b5122b;
  --red-light: #df253e;
  --white: #fff;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  background: var(--bg);
  color: var(--text);
  font-family: "DM Sans", sans-serif;
  line-height: 1.7;
}

a {
  text-decoration: none;
  color: inherit;
}

.container {
  width: min(1180px, 90%);
  margin: auto;
}

/* NAVIGATION */

.navbar {
  position: sticky;
  top: 0;
  z-index: 99;
  background: rgba(8,9,9,.92);
  backdrop-filter: blur(18px);
  border-bottom: 1px solid var(--border);
}

.nav-inner {
  min-height: 82px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.brand {
  display: flex;
  align-items: center;
  gap: 12px;
}

.brand-mark {
  width: 38px;
  height: 38px;
  border: 1px solid var(--red);
  display: grid;
  place-items: center;
  color: var(--red-light);
  font-size: 18px;
  transform: rotate(45deg);
}

.brand-mark span {
  transform: rotate(-45deg);
}

.brand-name {
  font-family: Manrope, sans-serif;
  font-weight: 800;
  letter-spacing: 2px;
  font-size: 15px;
}

.brand-name span {
  color: var(--red-light);
}

.brand-sub {
  color: #777;
  font-size: 8px;
  letter-spacing: 2.3px;
  margin-top: 1px;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 34px;
}

.nav-links > a:not(.nav-button) {
  font-size: 12px;
  color: #aaa;
  transition: .2s;
}

.nav-links > a:hover {
  color: white;
}

.nav-button {
  border: 1px solid rgba(181,18,43,.7);
  padding: 10px 17px;
  font-size: 11px;
  letter-spacing: .4px;
  transition: .25s;
}

.nav-button:hover {
  background: var(--red);
}

/* HERO */

.hero {
  position: relative;
  overflow: hidden;
  min-height: 660px;
  display: flex;
  align-items: center;
  border-bottom: 1px solid var(--border);
}

.hero::before {
  content: "";
  position: absolute;
  width: 700px;
  height: 700px;
  right: -170px;
  top: -40px;
  border-radius: 50%;
  border: 1px solid rgba(181,18,43,.14);
  box-shadow:
    0 0 0 70px rgba(181,18,43,.025),
    0 0 0 140px rgba(181,18,43,.02);
}

.hero::after {
  content: "";
  position: absolute;
  inset: 0;
  background: linear-gradient(
    90deg,
    var(--bg) 10%,
    rgba(8,9,9,.98) 45%,
    rgba(8,9,9,.35) 100%
  );
  pointer-events: none;
}

.hero-grid {
  position: absolute;
  right: 0;
  top: 0;
  height: 100%;
  width: 55%;
  opacity: .12;
  background-image:
    linear-gradient(rgba(255,255,255,.07) 1px, transparent 1px),
    linear-gradient(90deg,rgba(255,255,255,.07) 1px,transparent 1px);
  background-size: 50px 50px;
}

.hero-inner {
  position: relative;
  z-index: 2;
  width: 100%;
  display: grid;
  grid-template-columns: 1.15fr .85fr;
  align-items: center;
  gap: 40px;
  padding: 100px 0;
}

.hero-copy {
  max-width: 700px;
}

.kicker {
  display: flex;
  align-items: center;
  gap: 12px;
  color: var(--red-light);
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 3px;
  text-transform: uppercase;
  margin-bottom: 26px;
}

.kicker::before {
  content: "";
  height: 1px;
  width: 32px;
  background: var(--red);
}

.hero h1 {
  font-family: Manrope, sans-serif;
  font-size: clamp(42px, 6vw, 76px);
  line-height: 1.09;
  letter-spacing: -3.5px;
  font-weight: 700;
}

.hero h1 .accent {
  color: #b5122b;
}

.hero-description {
  color: #9b9d9d;
  max-width: 490px;
  font-size: 14px;
  margin-top: 25px;
}

.hero-actions {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  gap: 14px;
  margin-top: 35px;
}

.primary-btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 13px;
  background: var(--red);
  color: white;
  padding: 14px 21px;
  font-size: 11px;
  font-weight: 700;
  letter-spacing: .5px;
  transition: .25s;
}

.primary-btn:hover {
  background: var(--red-light);
  transform: translateY(-2px);
}

.secondary-btn {
  border: 1px solid var(--border);
  padding: 13px 21px;
  color: #ccc;
  font-size: 11px;
  transition: .25s;
}

.secondary-btn:hover {
  border-color: var(--red);
  color: white;
}

.hero-note {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-top: 52px;
  color: #707373;
  font-size: 10px;
  letter-spacing: 1.5px;
}

.hero-note span {
  width: 5px;
  height: 5px;
  background: var(--red);
}

/* HERO GRAPHIC */

.hero-visual {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 390px;
}

.orbit {
  width: 330px;
  height: 330px;
  border: 1px solid rgba(181,18,43,.22);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
}

.orbit::before,
.orbit::after {
  content: "";
  position: absolute;
  border-radius: 50%;
  border: 1px solid rgba(255,255,255,.06);
}

.orbit::before {
  inset: 32px;
}

.orbit::after {
  inset: 70px;
  border-color: rgba(181,18,43,.15);
}

.core {
  width: 115px;
  height: 115px;
  border: 1px solid rgba(181,18,43,.6);
  background: radial-gradient(circle, rgba(181,18,43,.2), #0a0a0a 70%);
  display: flex;
  justify-content: center;
  align-items: center;
  clip-path: polygon(50% 0, 90% 25%, 80% 80%, 50% 100%, 20% 80%, 10% 25%);
  color: #d91c36;
  font-size: 37px;
}

.orbit-label {
  position: absolute;
  font-size: 9px;
  letter-spacing: 2px;
  color: #888;
  background: #080909;
  padding: 6px 10px;
}

.label-top {
  top: 4px;
}

.label-bottom {
  bottom: 5px;
}

.label-left {
  left: -30px;
  top: 48%;
}

.label-right {
  right: -32px;
  top: 48%;
}

.visual-line {
  position: absolute;
  height: 1px;
  width: 70px;
  background: rgba(181,18,43,.4);
}

.line-one {
  top: 28%;
  right: -5px;
}

.line-two {
  bottom: 28%;
  left: -5px;
}

/* SECTION BASE */

.section {
  padding: 100px 0;
}

.section-head {
  max-width: 660px;
  margin-bottom: 50px;
}

.section-label {
  color: var(--red-light);
  font-size: 10px;
  letter-spacing: 3px;
  text-transform: uppercase;
  font-weight: 700;
  margin-bottom: 18px;
}

.section-head h2 {
  font-family: Manrope, sans-serif;
  font-size: clamp(29px, 4vw, 46px);
  line-height: 1.2;
  letter-spacing: -1.5px;
}

.section-head p {
  color: var(--muted);
  margin-top: 16px;
  font-size: 13px;
}

/* SERVICES */

.services {
  background: #0b0c0c;
  border-bottom: 1px solid var(--border);
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 1px;
  background: var(--border);
  border: 1px solid var(--border);
}

.service {
  background: #0b0c0c;
  padding: 35px;
  min-height: 235px;
  transition: .25s;
}

.service:hover {
  background: #111313;
}

.service-number {
  color: #5b5d5d;
  font-size: 10px;
  letter-spacing: 2px;
}

.service-symbol {
  font-size: 20px;
  color: var(--red);
  margin: 22px 0;
}

.service h3 {
  font-family: Manrope, sans-serif;
  font-size: 15px;
  font-weight: 700;
  margin-bottom: 12px;
}

.service p {
  color: #898c8c;
  font-size: 12px;
  line-height: 1.8;
}

/* ABOUT */

.about {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 85px;
  align-items: center;
}

.about-copy h2 {
  font-family: Manrope, sans-serif;
  font-size: clamp(32px,4vw,46px);
  line-height: 1.2;
  letter-spacing: -1.5px;
  margin-bottom: 22px;
}

.about-copy p {
  color: #959898;
  font-size: 13px;
  margin-bottom: 18px;
}

.about-panel {
  border: 1px solid var(--border);
  background: var(--surface);
}

.about-row {
  display: flex;
  gap: 20px;
  padding: 25px;
  border-bottom: 1px solid var(--border);
}

.about-row:last-child {
  border-bottom: none;
}

.about-row .symbol {
  color: var(--red);
  font-size: 16px;
  width: 25px;
}

.about-row h3 {
  font-size: 13px;
  margin-bottom: 5px;
}

.about-row p {
  color: var(--muted);
  font-size: 11px;
}

/* PROCESS */

.process {
  background: #0b0c0c;
  border-top: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
}

.process-grid {
  display: grid;
  grid-template-columns: repeat(4,1fr);
  gap: 25px;
}

.process-step {
  border-top: 1px solid rgba(181,18,43,.5);
  padding-top: 22px;
}

.process-step .number {
  color: var(--red);
  font-size: 11px;
  letter-spacing: 2px;
}

.process-step h3 {
  font-family: Manrope, sans-serif;
  font-size: 15px;
  margin: 18px 0 10px;
}

.process-step p {
  color: var(--muted);
  font-size: 12px;
}

/* CONTACT */

.contact {
  display: grid;
  grid-template-columns: .85fr 1.15fr;
  gap: 70px;
}

.contact-copy h2 {
  font-family: Manrope, sans-serif;
  font-size: 42px;
  line-height: 1.2;
  letter-spacing: -1.5px;
  margin-bottom: 20px;
}

.contact-copy p {
  color: var(--muted);
  font-size: 13px;
  margin-bottom: 25px;
}

.contact-detail {
  padding: 17px 0;
  border-bottom: 1px solid var(--border);
}

.contact-detail small {
  color: var(--red-light);
  display: block;
  font-size: 9px;
  letter-spacing: 2px;
  margin-bottom: 5px;
}

.contact-detail span {
  font-size: 12px;
  color: #ccc;
}

.contact-form {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 14px;
}

.contact-form .full {
  grid-column: 1/-1;
}

.contact-form input,
.contact-form select,
.contact-form textarea {
  width: 100%;
  background: #101111;
  color: #eee;
  border: 1px solid var(--border);
  padding: 15px;
  font-family: inherit;
  font-size: 12px;
  outline: none;
}

.contact-form input:focus,
.contact-form select:focus,
.contact-form textarea:focus {
  border-color: rgba(181,18,43,.7);
}

.contact-form textarea {
  resize: vertical;
  min-height: 140px;
}

.contact-form button {
  border: none;
  cursor: pointer;
  font-family: inherit;
}

/* FOOTER */

.footer {
  border-top: 1px solid var(--border);
  background: #050606;
  padding: 30px 0;
}

.footer-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 20px;
}

.footer-text {
  color: #666;
  font-size: 10px;
}

.footer-links {
  display: flex;
  gap: 25px;
}

.footer-links a {
  color: #888;
  font-size: 10px;
}

.footer-links a:hover {
  color: white;
}

/* RESPONSIVE */

@media(max-width: 900px) {
  .hero-inner {
    grid-template-columns: 1fr;
  }

  .hero-visual {
    display: none;
  }

  .services-grid {
    grid-template-columns: repeat(2,1fr);
  }

  .about,
  .contact {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .process-grid {
    grid-template-columns: repeat(2,1fr);
  }
}

@media(max-width: 600px) {
  .nav-inner {
    padding: 15px 0;
    flex-direction: column;
    gap: 15px;
  }

  .nav-links {
    gap: 16px;
    flex-wrap: wrap;
    justify-content: center;
  }

  .nav-links > a:not(.nav-button) {
    font-size: 10px;
  }

  .nav-button {
    display: none;
  }

  .hero-inner {
    padding: 85px 0;
  }

  .hero h1 {
    letter-spacing: -1.5px;
  }

  .section {
    padding: 70px 0;
  }

  .services-grid,
  .process-grid {
    grid-template-columns: 1fr;
  }

  .service {
    min-height: auto;
  }

  .contact-form {
    grid-template-columns: 1fr;
  }

  .contact-form .full {
    grid-column: auto;
  }

  .footer-inner {
    flex-direction: column;
    text-align: center;
  }
}
</style>
</head>

<body>

<!-- NAVIGATION -->
<nav class="navbar">
  <div class="container nav-inner">

    <a href="#home" class="brand">
      <div class="brand-mark"><span>◈</span></div>
      <div>
        <div class="brand-name">CYBER<span>PHANTOM</span></div>
        <div class="brand-sub">DIGITAL SECURITY</div>
      </div>
    </a>

    <div class="nav-links">
      <a href="#home">Home</a>
      <a href="#services">Capabilities</a>
      <a href="#about">About</a>
      <a href="#process">Approach</a>
      <a href="#contact" class="nav-button">Contact Us ↗</a>
    </div>

  </div>
</nav>

<!-- HERO -->
<header class="hero" id="home">
  <div class="hero-grid"></div>

  <div class="container hero-inner">

    <div class="hero-copy">

      <div class="kicker">Digital security. Elevated.</div>

      <h1>
        Confidence in a<br>
        <span class="accent">connected world.</span>
      </h1>

      <p class="hero-description">
        Thoughtful digital security solutions designed to help
        businesses protect their online presence, strengthen
        security practices, and navigate technology with confidence.
      </p>

      <div class="hero-actions">
        <a href="#contact" class="primary-btn">DISCUSS YOUR NEEDS ↗</a>
        <a href="#services" class="secondary-btn">EXPLORE CAPABILITIES</a>
      </div>

      <div class="hero-note">
        <span></span>
        SECURITY · PRIVACY · RESILIENCE
      </div>

    </div>

    <div class="hero-visual">
      <div class="orbit">
        <span class="orbit-label label-top">SECURE BY DESIGN</span>
        <span class="orbit-label label-left">PRIVACY</span>
        <span class="orbit-label label-right">DEFENSE</span>
        <span class="orbit-label label-bottom">CYBERPHANTOM</span>
        <div class="core">◈</div>
        <div class="visual-line line-one"></div>
        <div class="visual-line line-two"></div>
      </div>
    </div>

  </div>
</header>

<!-- SERVICES -->
<section class="section services" id="services">
  <div class="container">

    <div class="section-head">
      <div class="section-label">CAPABILITIES</div>
      <h2>Digital protection.<br> <span class="red">Built with intention.</span></h2>
      <p>
        Practical security services and guidance designed to
        address digital risks and improve security awareness.
      </p>
    </div>

    <div class="services-grid">

      <article class="service">
        <div class="service-number">01 / WEB</div>
        <div class="service-symbol">↗</div>
        <h3>Website Security</h3>
        <p>
          Website security reviews, secure configuration guidance,
          HTTPS recommendations, and practical improvements.
        </p>
      </article>

      <article class="service">
        <div class="service-number">02 / REVIEW</div>
        <div class="service-symbol">⌘</div>
        <h3>Security Assessments</h3>
        <p>
          Authorized reviews to identify potential weaknesses
          and prioritize appropriate security improvements.
        </p>
      </article>

      <article class="service">
        <div class="service-number">03 / PRIVACY</div>
        <div class="service-symbol">◈</div>
        <h3>Account Protection</h3>
        <p>
          Guidance for authentication, password security,
          privacy settings, and account protection.
        </p>
      </article>

      <article class="service">
        <div class="service-number">04 / NETWORK</div>
        <div class="service-symbol">⌁</div>
        <h3>Network Security</h3>
        <p>
          Network security fundamentals, configuration guidance,
          and recommendations for safer connectivity.
        </p>
      </article>

      <article class="service">
        <div class="service-number">05 / STRATEGY</div>
        <div class="service-symbol">△</div>
        <h3>Security Consulting</h3>
        <p>
          Personalized security guidance to help establish
          priorities and make informed technology decisions.
        </p>
      </article>

      <article class="service">
        <div class="service-number">06 / AWARENESS</div>
        <div class="service-symbol">✳</div>
        <h3>Security Awareness</h3>
        <p>
          Educational guidance covering phishing, online scams,
          digital privacy, and common security threats.
        </p>
      </article>

    </div>
  </div>
</section>

<!-- ABOUT -->
<section class="section">
  <div class="container about" id="about">

    <div class="about-copy">
      <div class="section-label">OUR PHILOSOPHY</div>

      <h2>
        Security is more than technology.
        <span class="red">It's trust.</span>
      </h2>

      <p>
        CyberPhantom is a digital security brand focused on
        practical protection, thoughtful technology, and making
        security easier to understand.
      </p>

      <p>
        We believe effective security begins with understanding
        the risks, identifying priorities, and taking meaningful
        steps toward a safer digital environment.
      </p>

      <a href="#contact" class="primary-btn">START A CONVERSATION ↗</a>
    </div>

    <div class="about-panel">

      <div class="about-row">
        <div class="symbol">◈</div>
        <div>
          <h3>Clarity over complexity</h3>
          <p>Security guidance that makes sense without unnecessary jargon.</p>
        </div>
      </div>

      <div class="about-row">
        <div class="symbol">△</div>
        <div>
          <h3>Thoughtful solutions</h3>
          <p>Recommendations built around the individual needs of each project.</p>
        </div>
      </div>

      <div class="about-row">
        <div class="symbol">↗</div>
        <div>
          <h3>Forward-focused</h3>
          <p>A proactive mindset toward digital security and technology.</p>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- PROCESS -->
<section class="section process" id="process">
  <div class="container">

    <div class="section-head">
      <div class="section-label">OUR APPROACH</div>
      <h2>A clear path to <span class="red">stronger security.</span></h2>
      <p>
        A straightforward process built around communication,
        understanding, and practical recommendations.
      </p>
    </div>

    <div class="process-grid">

      <div class="process-step">
        <div class="number">01 — DISCOVER</div>
        <h3>Understand</h3>
        <p>Learn about your business, digital environment, and security goals.</p>
      </div>

      <div class="process-step">
        <div class="number">02 — REVIEW</div>
        <h3>Evaluate</h3>
        <p>Review relevant security concerns within the agreed scope.</p>
      </div>

      <div class="process-step">
        <div class="number">03 — STRATEGY</div>
        <h3>Recommend</h3>
        <p>Develop clear, prioritized recommendations for improvement.</p>
      </div>

      <div class="process-step">
        <div class="number">04 — IMPROVE</div>
        <h3>Move Forward</h3>
        <p>Work toward implementing practical improvements and stronger habits.</p>
      </div>

    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="section" id="contact">
  <div class="container contact">

    <div class="contact-copy">
      <div class="section-label">CONTACT</div>

      <h2>Let's talk about <span class="red">security.</span></h2>

      <p>
        Every project begins with a conversation.
        Tell us what you're looking to protect, improve,
        or build.
      </p>

      <div class="contact-detail">
        <small>EMAIL</small>
        <span>ghosty.produced1@gmail.com</span>
      </div>

      <div class="contact-detail">
        <small>BRAND</small>
        <span>CyberPhantom Digital Security</span>
      </div>

      <div class="contact-detail">
        <small>INQUIRIES</small>
        <span>Business & project inquiries welcome</span>
      </div>
    </div>

    <form class="contact-form" id="contactForm">

      <input type="text" id="name" placeholder="Full name" required>

      <input type="email" id="email" placeholder="Email address" required>

      <select id="service" required>
        <option value="">What are you interested in?</option>
        <option>Website Security</option>
        <option>Security Assessment</option>
        <option>Account Protection</option>
        <option>Network Security</option>
        <option>Security Consulting</option>
        <option>Security Awareness</option>
        <option>Other</option>
      </select>

      <input type="text" id="company" placeholder="Company (optional)">

      <textarea class="full" id="message" placeholder="Tell us a little about your project or needs..." required></textarea>

      <button type="submit" class="primary-btn full">
        SEND INQUIRY ↗
      </button>

    </form>
  </div>
</section>

<!-- FOOTER -->
<footer class="footer">
  <div class="container footer-inner">

    <a href="#home" class="brand">
      <div class="brand-mark"><span>◈</span></div>
      <div>
        <div class="brand-name">CYBER<span>PHANTOM</span></div>
        <div class="brand-sub">DIGITAL SECURITY</div>
      </div>
    </a>

    <p class="footer-text">
      © 2026 CyberPhantom. All rights reserved.
    </p>

    <div class="footer-links">
      <a href="#services">Capabilities</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </div>

  </div>
</footer>

<script>
document.getElementById("contactForm").addEventListener("submit", function(event) {
  event.preventDefault();

  const name = document.getElementById("name").value;
  const email = document.getElementById("email").value;
  const service = document.getElementById("service").value;
  const company = document.getElementById("company").value;
  const message = document.getElementById("message").value;

  const subject = encodeURIComponent("CyberPhantom Business Inquiry");

  const body = encodeURIComponent(
    "Name: " + name + "\n" +
    "Email: " + email + "\n" +
    "Company: " + company + "\n" +
    "Service: " + service + "\n\n" +
    "Message:\n" + message
  );

  window.location.href =
    "mailto:ghosty.produced1@gmail.com?subject=" +
    subject + "&body=" + body;
});
</script>

</body>
</html>
