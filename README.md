<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Anthony Espinosa | Portfolio</title>
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;500;700&display=swap" rel="stylesheet">

  <style>
    /* --- CSS DESIGN STACK --- */
    :root {
      --primary: #10b981; /* Emerald */
      --bg-dark: #0f172a;
      --card-bg: rgba(30, 41, 59, 0.7);
      --text-light: #f1f5f9;
      --transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: 'Space Grotesk', sans-serif;
      background-color: var(--bg-dark);
      color: var(--text-light);
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* Background Animation */
    .blob {
      position: fixed;
      width: 400px; height: 400px;
      background: radial-gradient(circle, rgba(16, 185, 129, 0.15) 0%, transparent 70%);
      z-index: -1; filter: blur(60px);
      animation: move 20s infinite alternate;
    }
    .blob-2 { right: -100px; bottom: -100px; opacity: 0.5; }
    @keyframes move { from { transform: translate(0,0); } to { transform: translate(50px, 50px); } }

    header { text-align: center; padding: 3rem 1rem; }
    header h1 { font-size: 2.5rem; color: var(--primary); letter-spacing: -1px; }

    /* Navigation */
    #main-nav {
      position: sticky; top: 0;
      display: flex; justify-content: center;
      background: rgba(15, 23, 42, 0.9);
      backdrop-filter: blur(12px);
      padding: 1rem; z-index: 100;
      border-bottom: 1px solid rgba(255,255,255,0.1);
    }
    .nav-link {
      color: var(--text-light); text-decoration: none;
      margin: 0 15px; font-weight: 500; opacity: 0.6;
      transition: var(--transition);
    }
    .nav-link:hover, .nav-link.active { opacity: 1; color: var(--primary); }

    /* Logic: Hiding/Showing Sections */
    .content-section {
      display: none;
      max-width: 900px; margin: 2rem auto;
      padding: 2rem; animation: fadeInUp 0.5s ease forwards;
    }
    .content-section.active { display: block; }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* Cards & Grids */
    .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1.5rem; }
    .item-card {
      background: var(--card-bg); border: 1px solid rgba(255,255,255,0.05);
      border-radius: 12px; padding: 1.5rem; backdrop-filter: blur(10px);
      transition: var(--transition);
    }
    .item-card:hover { border-color: var(--primary); transform: translateY(-5px); }
    
    .project-thumb { width: 100%; border-radius: 8px; margin-bottom: 1rem; }

    /* Buttons */
    .explore-button, .file-link {
      display: inline-block; background: var(--primary); color: white;
      padding: 0.6rem 1.2rem; border-radius: 6px; text-decoration: none;
      margin-top: 1rem; transition: 0.3s;
    }

    /* Chatbot */
    .chatbot {
      position: fixed; bottom: 20px; right: 20px; width: 280px;
      background: #1e293b; border: 1px solid var(--primary);
      border-radius: 12px; overflow: hidden; box-shadow: 0 10px 30px rgba(0,0,0,0.5);
    }
    .chat-header { background: var(--primary); padding: 8px 12px; font-weight: bold; font-size: 0.75rem; }
    .chat-body { height: 150px; padding: 10px; overflow-y: auto; font-size: 0.85rem; background: #0f172a; }
    #chatInput { width: 100%; border: none; padding: 10px; background: #334155; color: white; }

    footer { text-align: center; padding: 2rem; opacity: 0.5; font-size: 0.8rem; }
  </style>
</head>
<body>

  <div class="blob" aria-hidden="true"></div>
  <div class="blob blob-2" aria-hidden="true"></div>

  <header>
    <h1>Anthony Espinosa</h1>
    <p>IT Student & Digital Architect</p>
  </header>

  <nav id="main-nav">
    <a href="#home" class="nav-link active" onclick="showSection('home'); return false;">Home</a>
    <a href="#about" class="nav-link" onclick="showSection('about'); return false;">About</a>
    <a href="#projects" class="nav-link" onclick="showSection('projects'); return false;">Projects</a>
    <a href="#skills" class="nav-link" onclick="showSection('skills'); return false;">Skills</a>
    <a href="#contact" class="nav-link" onclick="showSection('contact'); return false;">Contact</a>
  </nav>

  <main>
    <section id="home" class="content-section active">
      <h2>Welcome</h2>
      <p>I build elegant solutions for the modern web. Aspiring IT specialist focused on bridging the gap between design and functionality.</p>
      <a href="#projects" class="explore-button" onclick="showSection('projects'); return false;">View My Work</a>
    </section>

    <section id="about" class="content-section">
      <h2>Biography</h2>
      <p>Passionate about technology and human experience. Currently pursuing my IT degree with a focus on full-stack development.</p>
    </section>

    <section id="projects" class="content-section">
      <h2>Featured Work</h2>
      <div class="grid">
        <article class="item-card">
          <img src="assets/A.jpg" alt="Jersey Design" class="project-thumb">
          <h3>Jersey Layout</h3>
          <p>Creative sports apparel design and layout configuration.</p>
        </article>
        <article class="item-card">
          <h3>Logic Engine</h3>
          <p>Custom JavaScript tools for complex data workflows.</p>
        </article>
      </div>
    </section>

    <section id="skills" class="content-section">
      <h2>Technical Stack</h2>
      <div class="grid">
        <div class="item-card"><h3>Languages</h3><p>HTML, Java, JavaScript</p></div>
        <div class="item-card"><h3>Design</h3><p>Figma, UI/UX Design</p></div>
      </div>
    </section>

    <section id="contact" class="content-section">
      <h2>Let's Connect</h2>
      <div class="item-card">
        <p>📧 <a href="mailto:espinosaanthony50@gmail.com" style="color:var(--primary)">Email Me</a></p>
        <p>🔗 <a href="https://www.facebook.com/share/1AyUQ6gKmh/" target="_blank" style="color:var(--primary)">Facebook</a></p>
      </div>
    </section>
  </main>

  <aside class="chatbot">
    <div class="chat-header">SYSTEM ASSISTANT</div>
    <div class="chat-body" id="chatBody">
      <p><span style="color:var(--primary)">[Bot]:</span> Online. How can I help?</p>
    </div>
    <input type="text" id="chatInput" placeholder="Ask a question..." onkeypress="handleChat(event)">
  </aside>

  <footer>
    <p>&copy; 2026 Anthony Espinosa // Emerald Web Architecture</p>
  </footer>

  <script>
    /* --- JAVASCRIPT LOGIC --- */
    function showSection(sectionId) {
      // Hide all sections
      document.querySelectorAll('.content-section').forEach(sec => sec.classList.remove('active'));
      // Show clicked section
      document.getElementById(sectionId).classList.add('active');
      
      // Update Nav active state
      document.querySelectorAll('.nav-link').forEach(link => {
        link.classList.remove('active');
        if(link.getAttribute('href') === '#' + sectionId) link.classList.add('active');
      });

      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    function handleChat(e) {
      if (e.key === 'Enter') {
        const input = document.getElementById('chatInput');
        const body = document.getElementById('chatBody');
        if (input.value.trim()) {
          body.innerHTML += `<p style="opacity:0.6">[You]: ${input.value}</p>`;
          
          // Simple Response Logic
          setTimeout(() => {
            let resp = "Command recognized. Redirecting to " + input.value + "...";
            if(input.value.toLowerCase().includes("help")) resp = "Try clicking the 'Skills' tab!";
            body.innerHTML += `<p><span style="color:#10b981">[Bot]:</span> ${resp}</p>`;
            body.scrollTop = body.scrollHeight;
          }, 600);
          
          input.value = "";
        }
      }
    }
  </script>
</body>
</html>
