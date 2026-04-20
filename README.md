<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Anthony Espinosa | Portfolio</title>
  
  <meta property="og:title" content="Anthony Espinosa | Portfolio">
  <meta property="og:description" content="IT Student & Digital Architect - View my featured work and technical stack.">
  <meta property="og:image" content="assets/A.jpg"> 
  <meta name="theme-color" content="#10b981">

  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;500;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <div class="blob"></div>
  <div class="blob blob-2"></div>

  <header>
    <h1>Anthony Espinosa</h1>
    <p>IT Student & Digital Architect</p>
  </header>

  <nav id="main-nav">
    <a href="#home" class="active" onclick="showSection('home')">Home</a>
    <a href="#about" onclick="showSection('about')">About</a>
    <a href="#projects" onclick="showSection('projects')">Projects</a>
    <a href="#skills" onclick="showSection('skills')">Skills</a>
    <a href="#contact" onclick="showSection('contact')">Contact</a>
  </nav>

  <section id="home" class="active">
    <h2>Welcome</h2>
    <p>I build elegant solutions for the modern web. Aspiring IT specialist focused on bridging the gap between design and functionality.</p>
    <a href="#projects" class="explore-button" onclick="showSection('projects')">View My Work</a>
  </section>

  <section id="about">
    <h2>Biography</h2>
    <p>Passionate about the intersection of technology and human experience. Currently pursuing my IT degree with a focus on full-stack development.</p>
    <div class="img-container">
        <img src="https://via.placeholder.com/600x300/0f172a/10b981?text=Future+Tech+Vision" alt="Tech Vision">
    </div>
  </section>

  <section id="projects">
    <h2>Featured Work</h2>
    <div class="grid">
      <div class="item-card">
        <img src="assets/A.jpg" alt="Jersey Layout" class="project-thumb">
        <h3>Jersey Layout</h3>
        <p>Creative sports apparel design and layout configuration.</p>
        <a href="assets/A.jpg" target="_blank" class="file-link">View Design</a>
      </div>
      <div class="item-card">
        <img src="assets/project2.png" alt="Logic Engine" class="project-thumb">
        <h3>Logic Engine</h3>
        <p>Custom JavaScript tools to handle complex data workflows.</p>
        <a href="assets/logic-engine.zip" download class="file-link">Get Files</a>
      </div>
    </div>
  </section>

  <section id="skills">
    <h2>Technical Stack</h2>
    <div class="grid">
      <div class="item-card">
        <h3>Languages</h3>
        <p>HTML, Java, JavaScript</p>
      </div>
      <div class="item-card">
        <h3>Design</h3>
        <p>Figma, UI/UX Design</p>
      </div>
      <div class="item-card">
        <img src="assets/B.jpg" alt="Certification" class="project-thumb" style="height:120px;">
        <p>Verified Professional Training</p>
      </div>
    </div>
  </section>

  <section id="contact">
    <h2>Let's Connect</h2>
    <div class="contact-links">
      <a href="mailto:espinosaanthony50@gmail.com">📧 Email Me</a>
      <a href="https://www.facebook.com/share/1AyUQ6gKmh/" target="_blank">👤 Facebook Profile</a>
      <a href="https://www.instagram.com/toni_2high?igsh=MXFxcXVwc2Y5bXRpeQ==" target="_blank">📸 Instagram</a>
    </div>
  </section>

  <div class="chatbot">
    <div class="chat-header">SYSTEM ASSISTANT</div>
    <div class="chat-body" id="chatBody">
      <p><span class="bot-label">[Bot]:</span> Online. How can I help?</p>
    </div>
    <input type="text" id="chatInput" placeholder="Enter query..." onkeypress="handleChat(event)">
  </div>

  <footer>
    <p>&copy; 2026 Anthony Espinosa // Built for the Emerald Web.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
