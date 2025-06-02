<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Kemuel Rabi - Marketing Automation Specialist helping businesses streamline funnels, convert leads, and scale with smart marketing systems.">
  <title>Kemuel Rabi | Marketing Automation Specialist</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
  <style>
    :root {
      --primary-color: #0a1744;
      --accent-color: #FFD700;
      --accent-secondary: #00D4FF;
      --text-dark: #333;
      --text-light: #666;
      --bg-light: #f8f9fa;
      --bg-card: #ffffff;
      --border-color: #e9ecef;
      --gradient-primary: linear-gradient(135deg, #0a1744 0%, #1e3a8a 100%);
      --gradient-accent: linear-gradient(135deg, #FFD700 0%, #FFA500 100%);
      --gradient-hero: linear-gradient(135deg, #0a1744 0%, #1e3a8a 50%, #2563eb 100%);
      --shadow-card: 0 4px 6px rgba(0, 0, 0, 0.1);
      --shadow-hover: 0 8px 25px rgba(0, 0, 0, 0.15);
      --shadow-glow: 0 0 20px rgba(255, 215, 0, 0.3);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
      line-height: 1.6;
      color: var(--text-dark);
      background: var(--bg-light);
      overflow-x: hidden;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    /* Enhanced Navigation */
    nav {
      background: rgba(255, 255, 255, 0.95);
      backdrop-filter: blur(15px);
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 1000;
      box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
      transition: all 0.3s ease;
    }

    .nav-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 20px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .logo {
      font-weight: 700;
      font-size: 1.5rem;
      color: var(--primary-color);
      position: relative;
    }

    .logo::after {
      content: '';
      position: absolute;
      bottom: -2px;
      left: 0;
      width: 100%;
      height: 2px;
      background: var(--gradient-accent);
      border-radius: 1px;
    }

    .nav-links {
      display: flex;
      list-style: none;
      gap: 2rem;
    }

    .nav-links a {
      text-decoration: none;
      color: var(--text-dark);
      font-weight: 500;
      transition: all 0.3s ease;
      position: relative;
      padding: 0.5rem 1rem;
      border-radius: 20px;
    }

    .nav-links a:hover {
      color: var(--primary-color);
      background: rgba(255, 215, 0, 0.1);
      transform: translateY(-1px);
    }

    .nav-links a::after {
      content: '';
      position: absolute;
      width: 0;
      height: 2px;
      bottom: 0px;
      left: 50%;
      transform: translateX(-50%);
      background: var(--accent-color);
      transition: width 0.3s ease;
    }

    .nav-links a:hover::after {
      width: 60%;
    }

    /* Mobile menu toggle */
    .mobile-menu {
      display: none;
      flex-direction: column;
      cursor: pointer;
    }

    .mobile-menu span {
      width: 25px;
      height: 3px;
      background: var(--primary-color);
      margin: 3px 0;
      transition: 0.3s;
      border-radius: 2px;
    }

    /* Enhanced Hero Section */
    .hero {
      background: var(--gradient-hero);
      color: white;
      padding: 120px 0 80px;
      text-align: center;
      position: relative;
      overflow: hidden;
      min-height: 100vh;
      display: flex;
      align-items: center;
    }

    .hero::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000"><defs><pattern id="grid" width="100" height="100" patternUnits="userSpaceOnUse"><path d="M 100 0 L 0 0 0 100" fill="none" stroke="rgba(255,255,255,0.03)" stroke-width="1"/></pattern></defs><rect width="100%" height="100%" fill="url(%23grid)"/></svg>');
      opacity: 0.5;
    }

    .hero::after {
      content: '';
      position: absolute;
      top: 0;
      left: -50%;
      width: 200%;
      height: 100%;
      background: linear-gradient(45deg, transparent 30%, rgba(255, 215, 0, 0.05) 50%, transparent 70%);
      animation: shimmer 3s infinite;
    }

    @keyframes shimmer {
      0% { transform: translateX(-100%); }
      100% { transform: translateX(100%); }
    }

    .hero-content {
      position: relative;
      z-index: 2;
    }

    .hero h1 {
      font-size: clamp(2.5rem, 5vw, 4.5rem);
      font-weight: 700;
      margin-bottom: 1.5rem;
      line-height: 1.1;
      background: linear-gradient(135deg, #ffffff 0%, #FFD700 50%, #FFA500 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      animation: glow 2s ease-in-out infinite alternate;
    }

    @keyframes glow {
      from { filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.3)); }
      to { filter: drop-shadow(0 0 20px rgba(255, 215, 0, 0.6)); }
    }

    .hero .subtitle {
      font-size: 1.25rem;
      margin-bottom: 2rem;
      opacity: 0.9;
      max-width: 600px;
      margin-left: auto;
      margin-right: auto;
      animation: fadeInUp 1s ease-out 0.5s both;
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 0.9;
        transform: translateY(0);
      }
    }

    .cta-buttons {
      display: flex;
      gap: 1rem;
      justify-content: center;
      flex-wrap: wrap;
      margin-top: 2rem;
      animation: fadeInUp 1s ease-out 0.7s both;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 1rem 2rem;
      background: var(--gradient-accent);
      color: var(--primary-color);
      text-decoration: none;
      border-radius: 50px;
      font-weight: 600;
      transition: all 0.3s ease;
      box-shadow: var(--shadow-card);
      position: relative;
      overflow: hidden;
    }

    .btn::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
      transition: left 0.5s;
    }

    .btn:hover::before {
      left: 100%;
    }

    .btn:hover {
      transform: translateY(-3px) scale(1.05);
      box-shadow: var(--shadow-glow);
    }

    .btn-secondary {
      background: transparent;
      color: white;
      border: 2px solid white;
      backdrop-filter: blur(10px);
    }

    .btn-secondary:hover {
      background: white;
      color: var(--primary-color);
      box-shadow: var(--shadow-hover);
    }

    /* Floating elements */
    .floating-elements {
      position: absolute;
      width: 100%;
      height: 100%;
      overflow: hidden;
      z-index: 1;
    }

    .floating-element {
      position: absolute;
      background: rgba(255, 215, 0, 0.1);
      border-radius: 50%;
      animation: float 6s ease-in-out infinite;
    }

    .floating-element:nth-child(1) {
      width: 80px;
      height: 80px;
      top: 20%;
      left: 10%;
      animation-delay: 0s;
    }

    .floating-element:nth-child(2) {
      width: 120px;
      height: 120px;
      top: 60%;
      right: 10%;
      animation-delay: 2s;
    }

    .floating-element:nth-child(3) {
      width: 60px;
      height: 60px;
      top: 80%;
      left: 20%;
      animation-delay: 4s;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0px) rotate(0deg); }
      50% { transform: translateY(-20px) rotate(180deg); }
    }

    /* Enhanced Sections */
    section {
      padding: 100px 0;
      position: relative;
    }

    .section-title {
      text-align: center;
      font-size: 3rem;
      color: var(--primary-color);
      margin-bottom: 3rem;
      position: relative;
      font-weight: 700;
    }

    .section-title::after {
      content: '';
      position: absolute;
      bottom: -15px;
      left: 50%;
      transform: translateX(-50%);
      width: 80px;
      height: 4px;
      background: var(--gradient-accent);
      border-radius: 2px;
    }

    /* Enhanced About Section */
    .about-content {
      max-width: 900px;
      margin: 2rem auto 0;
    }

    .about-text {
      background: var(--bg-card);
      padding: 3rem;
      border-radius: 20px;
      box-shadow: var(--shadow-card);
      border: 1px solid var(--border-color);
      position: relative;
    }

    .about-text::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 4px;
      background: var(--gradient-accent);
      border-radius: 20px 20px 0 0;
    }

    .about-text p {
      margin-bottom: 1.5rem;
      color: var(--text-light);
      font-size: 1.1rem;
      line-height: 1.8;
    }

    .skills-list {
      list-style: none;
      margin: 2rem 0;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1rem;
    }

    .skills-list li {
      padding: 1rem;
      color: var(--text-dark);
      position: relative;
      background: rgba(255, 215, 0, 0.05);
      border-radius: 10px;
      border-left: 4px solid var(--accent-color);
      transition: all 0.3s ease;
    }

    .skills-list li:hover {
      transform: translateX(10px);
      background: rgba(255, 215, 0, 0.1);
    }

    .skills-list li::before {
      content: '⚡';
      position: absolute;
      left: -2px;
      top: 50%;
      transform: translateY(-50%);
      color: var(--accent-color);
      font-size: 1.2rem;
    }

    /* Enhanced Projects Section */
    .projects {
      background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
      gap: 2.5rem;
      margin-top: 3rem;
    }

    .project-card {
      background: var(--bg-card);
      border-radius: 20px;
      padding: 2.5rem;
      box-shadow: var(--shadow-card);
      transition: all 0.4s ease;
      border: 1px solid var(--border-color);
      position: relative;
      overflow: hidden;
    }

    .project-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 4px;
      background: var(--gradient-accent);
    }

    .project-card:hover {
      transform: translateY(-10px) scale(1.02);
      box-shadow: var(--shadow-hover);
      border-color: var(--accent-color);
    }

    .project-card h3 {
      color: var(--primary-color);
      margin-bottom: 1.5rem;
      font-size: 1.4rem;
      font-weight: 600;
    }

    .project-image {
      width: 100%;
      height: 220px;
      background: linear-gradient(135deg, #f8f9fa, #e9ecef);
      border-radius: 15px;
      margin: 1.5rem 0;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--text-light);
      font-style: italic;
      border: 2px dashed var(--border-color);
      position: relative;
      overflow: hidden;
    }

    .project-image::before {
      content: '📊';
      font-size: 3rem;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      opacity: 0.3;
    }

    .project-results {
      background: var(--gradient-accent);
      padding: 1.5rem;
      border-radius: 12px;
      margin-top: 1.5rem;
      color: var(--primary-color);
      font-weight: 600;
      box-shadow: inset 0 2px 4px rgba(0, 0, 0, 0.1);
    }

    .project-results strong {
      color: var(--primary-color);
      font-weight: 700;
    }

    /* Enhanced Tools Section */
    .tools-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
      gap: 1.5rem;
      margin-top: 3rem;
    }

    .tool-item {
      background: var(--bg-card);
      padding: 2rem 1.5rem;
      text-align: center;
      border-radius: 15px;
      box-shadow: var(--shadow-card);
      transition: all 0.3s ease;
      border: 1px solid var(--border-color);
      font-weight: 600;
      position: relative;
      overflow: hidden;
    }

    .tool-item::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: var(--gradient-accent);
      transition: left 0.3s ease;
      z-index: -1;
    }

    .tool-item:hover::before {
      left: 0;
    }

    .tool-item:hover {
      transform: translateY(-5px) scale(1.05);
      box-shadow: var(--shadow-hover);
      color: var(--primary-color);
    }

    /* Enhanced Testimonials */
    .testimonials {
      background: var(--bg-card);
    }

    .testimonials-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
      gap: 2.5rem;
      margin-top: 3rem;
    }

    .testimonial {
      background: linear-gradient(135deg, #ffffff 0%, #f8f9fa 100%);
      padding: 3rem;
      border-radius: 20px;
      box-shadow: var(--shadow-card);
      border-left: 6px solid var(--accent-color);
      position: relative;
      transition: all 0.3s ease;
    }

    .testimonial:hover {
      transform: translateY(-5px);
      box-shadow: var(--shadow-hover);
    }

    .testimonial::before {
      content: '"';
      font-size: 5rem;
      color: var(--accent-color);
      position: absolute;
      top: -10px;
      left: 30px;
      font-family: serif;
      opacity: 0.7;
    }

    .testimonial p {
      font-style: italic;
      color: var(--text-light);
      margin-top: 1rem;
      font-size: 1.1rem;
      line-height: 1.7;
    }

    /* Enhanced Contact Section */
    .contact {
      background: var(--gradient-primary);
      color: white;
    }

    .contact .section-title {
      color: white;
    }

    .contact .section-title::after {
      background: var(--accent-color);
    }

    .contact-content {
      text-align: center;
      max-width: 700px;
      margin: 0 auto;
    }

    .contact-content > p {
      font-size: 1.2rem;
      opacity: 0.9;
      margin-bottom: 3rem;
    }

    .contact-info {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 2rem;
      margin: 3rem 0;
    }

    .contact-item {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 1rem;
      background: rgba(255, 255, 255, 0.1);
      padding: 1.5rem;
      border-radius: 15px;
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      transition: all 0.3s ease;
    }

    .contact-item:hover {
      background: rgba(255, 215, 0, 0.2);
      transform: translateY(-5px);
    }

    .contact-item i {
      color: var(--accent-color);
      font-size: 1.5rem;
    }

    .social-links {
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      margin-top: 3rem;
    }

    .social-links a {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 60px;
      height: 60px;
      background: rgba(255, 255, 255, 0.1);
      color: white;
      border-radius: 50%;
      transition: all 0.3s ease;
      text-decoration: none;
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.2);
    }

    .social-links a:hover {
      background: var(--accent-color);
      color: var(--primary-color);
      transform: translateY(-5px) scale(1.1);
      box-shadow: var(--shadow-glow);
    }

    /* Enhanced Footer */
    footer {
      background: #000;
      color: white;
      text-align: center;
      padding: 3rem 0;
      position: relative;
    }

    footer::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 2px;
      background: var(--gradient-accent);
    }

    /* Progress indicator */
    .progress-bar {
      position: fixed;
      top: 0;
      left: 0;
      width: 0%;
      height: 3px;
      background: var(--gradient-accent);
      z-index: 9999;
      transition: width 0.1s ease;
    }

    /* Back to top button */
    .back-to-top {
      position: fixed;
      bottom: 30px;
      right: 30px;
      width: 50px;
      height: 50px;
      background: var(--gradient-accent);
      color: var(--primary-color);
      border: none;
      border-radius: 50%;
      cursor: pointer;
      font-size: 1.5rem;
      box-shadow: var(--shadow-card);
      transition: all 0.3s ease;
      opacity: 0;
      visibility: hidden;
      z-index: 1000;
    }

    .back-to-top.visible {
      opacity: 1;
      visibility: visible;
    }

    .back-to-top:hover {
      transform: translateY(-5px) scale(1.1);
      box-shadow: var(--shadow-glow);
    }

    /* Responsive Design */
    @media (max-width: 768px) {
      .nav-links {
        display: none;
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        background: rgba(255, 255, 255, 0.98);
        flex-direction: column;
        padding: 2rem;
        box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
      }

      .nav-links.active {
        display: flex;
      }

      .mobile-menu {
        display: flex;
      }

      .hero {
        min-height: 80vh;
        padding: 100px 0 60px;
      }

      .hero h1 {
        font-size: 2.5rem;
      }

      .cta-buttons {
        flex-direction: column;
        align-items: center;
      }

      .btn {
        width: 200px;
        justify-content: center;
      }

      .contact-info {
        grid-template-columns: 1fr;
      }

      section {
        padding: 80px 0;
      }

      .section-title {
        font-size: 2.5rem;
      }

      .projects-grid,
      .tools-grid {
        grid-template-columns: 1fr;
      }

      .skills-list {
        grid-template-columns: 1fr;
      }
    }

    /* Smooth scrolling */
    html {
      scroll-behavior: smooth;
    }

    /* Loading animation */
    .fade-in {
      opacity: 0;
      transform: translateY(30px);
      transition: all 0.6s ease;
    }

    .fade-in.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* Slide in animations */
    .slide-in-left {
      opacity: 0;
      transform: translateX(-50px);
      transition: all 0.6s ease;
    }

    .slide-in-right {
      opacity: 0;
      transform: translateX(50px);
      transition: all 0.6s ease;
    }

    .slide-in-left.visible,
    .slide-in-right.visible {
      opacity: 1;
      transform: translateX(0);
    }
  </style>
</head>
<body>
  <!-- Progress Bar -->
  <div class="progress-bar"></div>
  
  <!-- Navigation -->
  <nav>
    <div class="nav-container">
      <div class="logo">Kemuel Rabi</div>
      <ul class="nav-links">
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#tools">Tools</a></li>
        <li><a href="#testimonials">Testimonials</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <div class="mobile-menu">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>
  </nav>

  <!-- Hero Section -->
  <section class="hero">
    <div class="floating-elements">
      <div class="floating-element"></div>
      <div class="floating-element"></div>
      <div class="floating-element"></div>
    </div>
    <div class="container">
      <div class="hero-content fade-in">
        <h1>Ditch the Doubt.<br>Master Marketing with Precision.</h1>
        <p class="subtitle">Marketing Automation Specialist helping businesses streamline funnels, convert more leads, and scale with smart marketing systems.</p>
        <div class="cta-buttons">
          <a href="#projects" class="btn">
            <i class="fas fa-folder-open"></i>
            View My Work
          </a>
          <a href="#contact" class="btn btn-secondary">
            <i class="fas fa-envelope"></i>
            Get In Touch
          </a>
        </div>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section id="about">
    <div class="container">
      <h2 class="section-title fade-in">About Me</h2>
      <div class="about-content">
        <div class="about-text fade-in">
          <p>I'm Kemuel Rabi—a data-informed marketing strategist focused on building efficient, results-driven systems through automation and funnel optimization.</p>
          <p>I work with entrepreneurs, coaches, and small business teams to streamline lead capture, scale client acquisition, and set up high-performing campaigns using platforms like GoHighLevel, HubSpot, and Zapier.</p>
          <p><strong>My specialties include:</strong></p>
          <ul class="skills-list">
            <li>Funnel design for webinars, landing pages, and services</li>
            <li>Website design and editing (Wix, Elementor, Webflow)</li>
            <li>Conditional lead nurturing flows</li>
            <li>CRM integration and segmentation</li>
            <li>Paid ad performance tracking (Meta, Google, LinkedIn)</li>
            <li>Cross-platform content strategies</li>
          </ul>
          <p>I blend strategy, technology, and creativity to build end-to-end marketing operations that actually work.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Projects Section -->
  <section id="projects" class="projects">
    <div class="container">
      <h2 class="section-title fade-in">Featured Projects</h2>
      <div class="projects-grid">
        <div class="project-card slide-in-left">
          <h3>Webinar Funnel for Estate Planning Firm</h3>
          <div class="project-image">Webinar Funnel Screenshot</div>
          <ul>
            <li>End-to-end funnel with tiered nurturing (Basic, Premium, VIP)</li>
            <li>Tools: GoHighLevel, Zapier, Google Analytics</li>
          </ul>
          <div class="project-results">
            <strong>Results:</strong> +40% attendance rate, +27% more qualified leads
          </div>
        </div>
        
        <div class="project-card fade-in">
          <h3>Brand Awareness Campaigns</h3>
          <div class="project-image">Social Media Campaign Screenshot</div>
          <ul>
            <li>Strategic campaigns with automated chat flows (Facebook Ads + ManyChat)</li>
            <li>Branded content creation in Canva</li>
          </ul>
          <div class="project-results">
            <strong>Results:</strong> 15–30% increase in page engagement
          </div>
        </div>

        <div class="project-card slide-in-right">
          <h3>Marketing Automation Workflow</h3>
          <div class="project-image">Automation Workflow Diagram</div>
          <p><strong>Example Workflow:</strong></p>
          <ul>
            <li><strong>Trigger:</strong> Lead signs up for webinar</li>
            <li><strong>Condition:</strong> If consultation booked → Move to VIP tier</li>
            <li><strong>Else:</strong> Start follow-up email sequence</li>
            <li><strong>System:</strong> Tag → Notify team → Update CRM</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- Tools Section -->
  <section id="tools">
    <div class="container">
      <h2 class="section-title fade-in">Tools & Platforms</h2>
      <div class="tools-grid fade-in">
        <div class="tool-item">GoHighLevel</div>
        <div class="tool-item">HubSpot</div>
        <div class="tool-item">Zapier</div>
        <div class="tool-item">Facebook Ads</div>
        <div class="tool-item">Google Ads</div>
        <div class="tool-item">LinkedIn Ads</div>
        <div class="tool-item">ManyChat</div>
        <div class="tool-item">Google Analytics</div>
        <div class="tool-item">Google Tag Manager</div>
        <div class="tool-item">UTM Tracking</div>
        <div class="tool-item">Canva</div>
        <div class="tool-item">Adobe Creative Suite</div>
        <div class="tool-item">Figma</div>
        <div class="tool-item">Wix</div>
        <div class="tool-item">Webflow</div>
        <div class="tool-item">Elementor</div>
      </div>
    </div>
  </section>

  <!-- Testimonials Section -->
  <section id="testimonials" class="testimonials">
    <div class="container">
      <h2 class="section-title fade-in">Client Results</h2>
      <div class="testimonials-grid">
        <div class="testimonial slide-in-left">
          <p>"Working with Kemuel has been a game-changer for our brand. His strategic approach to social media not only boosted our online presence but also drove real engagement and conversions. Highly recommended!"</p>
        </div>
        <div class="testimonial slide-in-right">
          <p>"We've seen a noticeable improvement in our visibility and customer interaction since partnering with Kemuel. His strategies are spot-on and proactive. A true professional!"</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="contact">
    <div class="container">
      <div class="contact-content fade-in">
        <h2 class="section-title">Let's Work Together</h2>
        <p>Ready to scale your marketing systems and convert more leads? Let's discuss how I can help transform your business.</p>
        
        <div class="contact-info">
          <div class="contact-item">
            <i class="fas fa-envelope"></i>
            <span>kemuel.rabi@gmail.com</span>
          </div>
          <div class="contact-item">
            <i class="fas fa-phone"></i>
            <span>(+63) 945 734 3302</span>
          </div>
          <div class="contact-item">
            <i class="fas fa-map-marker-alt"></i>
            <span>Tacloban, Philippines</span>
          </div>
        </div>

        <div class="social-links">
          <a href="https://linkedin.com/in/kemuelrabi" target="_blank" rel="noopener noreferrer">
            <i class="fab fa-linkedin-in"></i>
          </a>
          <a href="https://www.instagram.com/iammrkrab30/" target="_blank" rel="noopener noreferrer">
            <i class="fab fa-instagram"></i>
          </a>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="container">
      <p>&copy; 2025 Kemuel Rabi | Marketing Automation Specialist</p>
    </div>
  </footer>

  <!-- Back to Top Button -->
  <button class="back-to-top" id="backToTop">
    <i class="fas fa-arrow-up"></i>
  </button>

  <script>
    // Mobile menu toggle
    const mobileMenu = document.querySelector('.mobile-menu');
    const navLinks = document.querySelector('.nav-links');

    mobileMenu.addEventListener('click', () => {
      navLinks.classList.toggle('active');
      mobileMenu.classList.toggle('active');
    });

    // Close mobile menu when clicking on a link
    document.querySelectorAll('.nav-links a').forEach(link => {
      link.addEventListener('click', () => {
        navLinks.classList.remove('active');
        mobileMenu.classList.remove('active');
      });
    });

    // Smooth scrolling for navigation links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          target.scrollIntoView({
            behavior: 'smooth',
            block: 'start'
          });
        }
      });
    });

    // Progress bar
    const progressBar = document.querySelector('.progress-bar');
    
    function updateProgressBar() {
      const scrollTop = window.pageYOffset;
      const docHeight = document.documentElement.scrollHeight - window.innerHeight;
      const scrollPercent = (scrollTop / docHeight) * 100;
      progressBar.style.width = scrollPercent + '%';
    }

    // Fade in animation on scroll
    const observerOptions = {
      threshold: 0.1,
      rootMargin: '0px 0px -50px 0px'
    };

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, observerOptions);

    // Observe all fade-in elements
    document.querySelectorAll('.fade-in, .slide-in-left, .slide-in-right').forEach(el => {
      observer.observe(el);
    });

    // Back to top button
    const backToTop = document.getElementById('backToTop');

    function toggleBackToTop() {
      if (window.scrollY > 300) {
        backToTop.classList.add('visible');
      } else {
        backToTop.classList.remove('visible');
      }
    }

    backToTop.addEventListener('click', () => {
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      });
    });

    // Navbar background on scroll
    function updateNavbar() {
      const nav = document.querySelector('nav');
      if (window.scrollY > 100) {
        nav.style.background = 'rgba(255, 255, 255, 0.98)';
        nav.style.boxShadow = '0 2px 20px rgba(0, 0, 0, 0.15)';
      } else {
        nav.style.background = 'rgba(255, 255, 255, 0.95)';
        nav.style.boxShadow = '0 2px 20px rgba(0, 0, 0, 0.1)';
      }
    }

    // Parallax effect for hero section
    function parallaxEffect() {
      const hero = document.querySelector('.hero');
      const scrolled = window.pageYOffset;
      const rate = scrolled * -0.5;
      
      if (hero) {
        hero.style.transform = `translate3d(0, ${rate}px, 0)`;
      }
    }

    // Throttle function for performance
    function throttle(func, limit) {
      let inThrottle;
      return function() {
        const args = arguments;
        const context = this;
        if (!inThrottle) {
          func.apply(context, args);
          inThrottle = true;
          setTimeout(() => inThrottle = false, limit);
        }
      }
    }

    // Event listeners with throttling
    window.addEventListener('scroll', throttle(() => {
      updateProgressBar();
      toggleBackToTop();
      updateNavbar();
      parallaxEffect();
    }, 16));

    // Typing effect for hero title
    function typeWriter(element, text, speed = 100) {
      let i = 0;
      element.innerHTML = '';
      
      function type() {
        if (i < text.length) {
          element.innerHTML += text.charAt(i);
          i++;
          setTimeout(type, speed);
        }
      }
      
      type();
    }

    // Initialize typing effect when page loads
    window.addEventListener('load', () => {
      const heroTitle = document.querySelector('.hero h1');
      if (heroTitle) {
        const originalText = heroTitle.textContent;
        setTimeout(() => {
          typeWriter(heroTitle, originalText, 50);
        }, 1000);
      }
    });

    // Smooth reveal animation for skills
    const skillsObserver = new IntersectionObserver((entries) => {
      entries.forEach((entry, index) => {
        if (entry.isIntersecting) {
          setTimeout(() => {
            entry.target.style.transform = 'translateX(0) scale(1)';
            entry.target.style.opacity = '1';
          }, index * 100);
        }
      });
    }, { threshold: 0.1 });

    document.querySelectorAll('.skills-list li').forEach((skill, index) => {
      skill.style.transform = 'translateX(-50px) scale(0.8)';
      skill.style.opacity = '0';
      skill.style.transition = `all 0.6s ease ${index * 0.1}s`;
      skillsObserver.observe(skill);
    });

    // Tool items hover effect with stagger
    document.querySelectorAll('.tool-item').forEach((tool, index) => {
      tool.addEventListener('mouseenter', () => {
        tool.style.animationDelay = `${index * 0.05}s`;
      });
    });

    // Contact form submission (if you add a form later)
    function handleFormSubmission(event) {
      event.preventDefault();
      // Add your form handling logic here
      console.log('Form submitted');
    }

    // Initialize AOS-like animations
    function initAnimations() {
      const animatedElements = document.querySelectorAll('[data-animate]');
      
      const animationObserver = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            const animationType = entry.target.getAttribute('data-animate');
            entry.target.classList.add(`animate-${animationType}`);
          }
        });
      }, { threshold: 0.1 });

      animatedElements.forEach(el => {
        animationObserver.observe(el);
      });
    }

    // Initialize everything when DOM is loaded
    document.addEventListener('DOMContentLoaded', () => {
      initAnimations();
      
      // Add some interactive elements
      const projectCards = document.querySelectorAll('.project-card');
      projectCards.forEach(card => {
        card.addEventListener('mouseenter', () => {
          card.style.transform = 'translateY(-10px) scale(1.02) rotateX(5deg)';
        });
        
        card.addEventListener('mouseleave', () => {
          card.style.transform = 'translateY(0) scale(1) rotateX(0deg)';
        });
      });

      // Add click effects to buttons
      const buttons = document.querySelectorAll('.btn');
      buttons.forEach(btn => {
        btn.addEventListener('click', function(e) {
          let ripple = document.createElement('span');
          ripple.classList.add('ripple');
          this.appendChild(ripple);

          let x = e.clientX - e.target.offsetLeft;
          let y = e.clientY - e.target.offsetTop;

          ripple.style.left = `${x}px`;
          ripple.style.top = `${y}px`;

          setTimeout(() => {
            ripple.remove();
          }, 600);
        });
      });
    });

    // Performance optimization: Reduce animations on low-end devices
    const prefersReducedMotion = window.matchMedia('(prefers-reduced-motion: reduce)');
    
    if (prefersReducedMotion.matches) {
      document.documentElement.style.setProperty('--animation-duration', '0.01ms');
    }

    // Add some easter eggs for fun
    let clickCount = 0;
    document.querySelector('.logo').addEventListener('click', () => {
      clickCount++;
      if (clickCount === 5) {
        document.body.style.filter = 'hue-rotate(180deg)';
        setTimeout(() => {
          document.body.style.filter = 'none';
          clickCount = 0;
        }, 2000);
      }
    });
  </script>
</body>
</html>
# mktbykem.github.io
