<!DOCTYPE html>
<html lang="en">
<head></head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Anthony Espinosa | IT Professional Portfolio</title>
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

  <style>
    /* --- MODERN UI SYSTEM --- */
    :root {
      --bg: #ffffff;
      --text: #111827;
      --secondary-text: #4b5563;
      --accent: #000000;
      --gray-light: #f3f4f6;
      --gray-mid: #e5e7eb;
      --border: #d1d5db;
      --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
      --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: 'Inter', sans-serif;
      background-color: var(--bg);
      color: var(--text);
      line-height: 1.5;
    }

    /* Navigation */
    nav {
      position: fixed; top: 0; width: 100%;
      background: rgba(255, 255, 255, 0.9);
      backdrop-filter: blur(8px);
      border-bottom: 1px solid var(--gray-mid);
      z-index: 1000;
      display: flex; justify-content: center; padding: 1.2rem;
    }
    .nav-link {
      color: var(--secondary-text); text-decoration: none;
      margin: 0 1rem; font-weight: 500; font-size: 0.9rem;
      transition: var(--transition); cursor: pointer;
    }
    .nav-link:hover, .nav-link.active { color: var(--accent); font-weight: 700; }

    /* Layout Components */
    main { max-width: 800px; margin: 100px auto 60px; padding: 0 20px; }

    .content-section {
      display: none; animation: fadeIn 0.4s ease-out;
    }
    .content-section.active { display: block; }

    @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

    /* UI Elements */
    h1 { font-size: 3rem; font-weight: 700; letter-spacing: -2px; margin-bottom: 0.5rem; }
    h2 { font-size: 1.5rem; border-bottom: 2px solid var(--accent); display: inline-block; margin-bottom: 1.5rem; }
    p { color: var(--secondary-text); margin-bottom: 1.5rem; font-size: 1.1rem; }

    .button-group { display: flex; gap: 10px; flex-wrap: wrap; }
    
    .btn {
      padding: 12px 24px; border-radius: 6px; font-weight: 600; 
      cursor: pointer; transition: var(--transition); text-decoration: none;
      display: inline-flex; align-items: center; justify-content: center;
    }
    .btn-primary { background: var(--accent); color: white; border: none; }
    .btn-primary:hover { background: #333; transform: translateY(-2px); }
    
    .btn-outline { background: transparent; color: var(--accent); border: 2px solid var(--accent); }
    .btn-outline:hover { background: var(--gray-light); }

    .btn-download { background: var(--gray-light); color: var(--accent); border: 1px solid var(--border); }

    /* Cards */
    .card-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 20px; }
    @media (max-width: 600px) { .card-grid { grid-template-columns: 1fr; } }
    
    .card {
      background: var(--gray-light); padding: 20px; border-radius: 8px;
      border: 1px solid var(--gray-mid);
    }
    .card h3 { margin-bottom: 8px; font-size: 1rem; }

    /* Chatbot Interface */
    .chatbot-container {
      position: fixed; bottom: 25px; right: 25px; width: 320px;
      background: white; border-radius: 12px; border: 1px solid var(--border);
      box-shadow: 0 10px 25px rgba(0,0,0,0.1); overflow: hidden; z-index: 2000;
    }
    .chat-header { background: var(--accent); color: white; padding: 12px; font-weight: 600; font-size: 0.8rem; }
    .chat-box { height: 250px; padding: 15px; overflow-y: auto; background: white; font-size: 0.85rem; }
    .chat-input-area { display: flex; border-top: 1px solid var(--gray-mid); }
    #chatInput { flex: 1; padding: 12px; border: none; outline: none; }
    #sendBtn { padding: 12px; background: white; border: none; cursor: pointer; font-weight: bold; }

    .msg { margin-bottom: 10px; border-radius: 4px; padding: 8px; max-width: 85%; }
    .bot-msg { background: var(--gray-light); color: var(--text); align-self: flex-start; }
    .user-msg { background: #333; color: white; margin-left: auto; }

    footer { text-align: center; padding: 40px; border-top: 1px solid var(--gray-mid); color: var(--secondary-text); font-size: 0.8rem; }
  </style>
</head>
<body>

  <nav>
    <div class="nav-link active" onclick="showSection('home')">Home</div>
    <div class="nav-link" onclick="showSection('about')">About</div>
    <div class="nav-link" onclick="showSection('skills')">Skills</div>
    <div class="nav-link" onclick="showSection('certificates')">Certificates</div>
    <div class="nav-link" onclick="showSection('contact')">Contact</div>
  </nav>

  <main>
    <section id="home" class="content-section active">
      <h1>Anthony Espinosa</h1>
      <p>IT Student & Digital Architect based in the Philippines. I specialize in bridging technical logic with elegant user interfaces.</p>
      <div class="button-group">
        <button class="btn btn-primary" onclick="showSection('about')">About Me</button>
        <button class="btn btn-outline" onclick="showSection('projects')">View Projects</button>
        <a href="path-to-your-cv.pdf" download="Anthony_Espinosa_CV" class="btn btn-download">
          📄 Download CV
        </a>
      </div>
    </section>

    <section id="about" class="content-section">
      <h2>About Me</h2>
      <p>I am a passionate IT professional dedicated to full-stack development and UI/UX design. I believe technology should be as beautiful as it is functional.</p>
      <p>Currently pursuing advanced studies in Information Technology, focusing on modern web frameworks and data systems.</p>
      <button class="btn btn-primary" onclick="showSection('skills')">Check My Skills</button>
    </section>

    <section id="skills" class="content-section">
      <h2>Technical Stack</h2>
      <div class="card-grid">
        <div class="card">
          <h3>Languages</h3>
          <p>HTML5, CSS3, JavaScript (ES6+), Java</p>
        </div>
        <div class="card">
          <h3>Design</h3>
          <p>Figma, Adobe XD, UI/UX Principles</p>
        </div>
        <div class="card">
          <h3>Development</h3>
          <p>Responsive Design, Git, Logic Engine Design</p>
        </div>
        <div class="card">
          <h3>Frameworks</h3>
          <p>Learning React, Node.js</p>
        </div>
      </div>
      <br>
      <button class="btn btn-primary" onclick="showSection('certificates')">View Certificates</button>
    </section>

    <section id="certificates" class="content-section">
      <h2>Professional Training</h2>
      <div class="card">
        <h3>Verified IT Specialist Certification</h3>
        <p>Issued by Professional Training Institute</p>
        <small>Date: 2025</small>
      </div>
      <br>
      <button class="btn btn-primary" onclick="showSection('contact')">Get In Touch</button>
    </section>

    <section id="contact" class="content-section">
      <h2>Let's Connect</h2>
      <p>I am always open to discussing new projects, creative ideas, or opportunities to be part of your vision.</p>
      <div class="card">
        <p><strong>Email:</strong> espinosaanthony50@gmail.com</p>
        <p><strong>Location:</strong> Philippines</p>
        <div class="button-group" style="margin-top:20px;">
          <a href="https://www.facebook.com/share/1AyUQ6gKmh/" target="_blank" class="btn btn-outline">Facebook</a>
          <a href="https://www.instagram.com/toni_2high?igsh=MXFxcXVwc2Y5bXRpeQ==" target="_blank" class="btn btn-outline">Instagram</a>
        </div>
      </div>
    </section>
  </main>

  <div class="chatbot-container">
    <div class="chat-header">ASSISTANT // ONLINE</div>
    <div class="chat-box" id="chatBox">
      <div class="msg bot-msg">Hello! I'm Anthony's assistant. Ask me about his skills, background, or how to contact him.</div>
    </div>
    <div class="chat-input-area">
      <input type="text" id="chatInput" placeholder="Ask a question...">
      <button id="sendBtn">➤</button>
    </div>
  </div>

  <footer>
    &copy; 2026 Anthony Espinosa. Built with Precision.
  </footer>

  <script>
    // 1. SECTION NAVIGATION LOGIC
    function showSection(id) {
      // Hide all
      document.querySelectorAll('.content-section').forEach(section => {
        section.classList.remove('active');
      });
      // Show Target
      document.getElementById(id).classList.add('active');
      
      // Update Nav active state
      document.querySelectorAll('.nav-link').forEach(link => {
        link.classList.remove('active');
        if(link.innerText.toLowerCase() === id.toLowerCase()) {
          link.classList.add('active');
        }
      });

      // Scroll to top of section
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    // 2. CONTEXT-AWARE AI CHATBOT LOGIC
    const chatInput = document.getElementById('chatInput');
    const sendBtn = document.getElementById('sendBtn');
    const chatBox = document.getElementById('chatBox');

    const portfolioData = {
      skills: "Anthony knows HTML, CSS, JavaScript, and Java. He also uses Figma for UI/UX design.",
      contact: "You can email him at espinosaanthony50@gmail.com or find him on Instagram (@toni_2high).",
      about: "Anthony is an IT Student and Digital Architect who focuses on full-stack development and elegant web solutions.",
      certificates: "He holds a Verified IT Specialist Certification from 2025.",
      location: "He is based in the Philippines."
    };

    function handleChat() {
      const query = chatInput.value.toLowerCase().trim();
      if (!query) return;

      // Display User Message
      appendMessage(chatInput.value, 'user-msg');
      chatInput.value = '';

      // Determine Bot Response
      setTimeout(() => {
        let response = "I'm sorry, I don't have that specific information. Try asking about his skills, contact info, or background.";

        if (query.includes("skill") || query.includes("language") || query.includes("stack")) {
          response = portfolioData.skills;
        } else if (query.includes("contact") || query.includes("email") || query.includes("facebook")) {
          response = portfolioData.contact;
        } else if (query.includes("who") || query.includes("about") || query.includes("background")) {
          response = portfolioData.about;
        } else if (query.includes("cert") || query.includes("training")) {
          response = portfolioData.certificates;
        } else if (query.includes("hi") || query.includes("hello")) {
          response = "Hello! How can I help you learn more about Anthony today?";
        }

        appendMessage(response, 'bot-msg');
      }, 500);
    }

    function appendMessage(text, className) {
      const msgDiv = document.createElement('div');
      msgDiv.className = `msg ${className}`;
      msgDiv.innerText = text;
      chatBox.appendChild(msgDiv);
      chatBox.scrollTop = chatBox.scrollHeight;
    }

    sendBtn.addEventListener('click', handleChat);
    chatInput.addEventListener('keypress', (e) => { if(e.key === 'Enter') handleChat(); });
  </script>
</body>
</html>
