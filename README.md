<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Anthony Espinosa | Portfolio</title>
  
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;500;700&display=swap" rel="stylesheet">

  <style>
    /* PASTE THE CSS CODE HERE */
    :root {
      --primary: #10b981;
      --bg: #0f172a;
      --card-bg: rgba(30, 41, 59, 0.7);
      --text: #f8fafc;
    }
    /* ... include the rest of the CSS from the previous message ... */
  </style>
</head>
<body>

  <script>
    // PASTE THE JAVASCRIPT CODE HERE
    function showSection(sectionId) {
      const sections = document.querySelectorAll('section');
      sections.forEach(sec => sec.classList.remove('active'));
      // ... include the rest of the JS logic ...
    }
  </script>
</body>
</html>
:root {
  --primary: #10b981; /* Emerald */
  --bg-dark: #0f172a;
  --card-bg: rgba(30, 41, 59, 0.7);
  --text-light: #f1f5f9;
  --transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Space Grotesk', sans-serif;
  background-color: var(--bg-dark);
  color: var(--text-light);
  line-height: 1.6;
  overflow-x: hidden;
}

/* --- Animated Background Blobs --- */
.blob {
  position: fixed;
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, rgba(16, 185, 129, 0.2) 0%, transparent 70%);
  z-index: -1;
  filter: blur(50px);
  animation: move 20s infinite alternate;
}

.blob-2 {
  right: -100px;
  bottom: -100px;
  background: radial-gradient(circle, rgba(56, 189, 248, 0.15) 0%, transparent 70%);
}

@keyframes move {
  from { transform: translate(0, 0); }
  to { transform: translate(100px, 100px); }
}

/* --- Navigation --- */
#main-nav {
  position: sticky;
  top: 0;
  display: flex;
  justify-content: center;
  background: rgba(15, 23, 42, 0.8);
  backdrop-filter: blur(10px);
  padding: 1rem;
  z-index: 100;
  border-bottom: 1px solid rgba(255,255,255,0.1);
}

#main-nav a {
  color: var(--text-light);
  text-decoration: none;
  margin: 0 15px;
  font-weight: 500;
  transition: var(--transition);
  opacity: 0.7;
}

#main-nav a:hover, #main-nav a.active {
  color: var(--primary);
  opacity: 1;
}

/* --- Sections Visibility --- */
section {
  display: none; /* Hidden by default for the JS logic */
  max-width: 1000px;
  margin: 4rem auto;
  padding: 2rem;
  animation: fadeIn 0.6s ease-out;
}

section.active {
  display: block;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* --- Grid & Cards --- */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.item-card {
  background: var(--card-bg);
  border: 1px solid rgba(255,255,255,0.1);
  border-radius: 16px;
  padding: 1.5rem;
  backdrop-filter: blur(5px);
  transition: var(--transition);
}

.item-card:hover {
  transform: translateY(-10px);
  border-color: var(--primary);
  box-shadow: 0 10px 30px rgba(16, 185, 129, 0.1);
}

.project-thumb {
  width: 100%;
  border-radius: 8px;
  margin-bottom: 1rem;
}

/* --- Buttons --- */
.explore-button, .file-link {
  display: inline-block;
  background: var(--primary);
  color: #fff;
  padding: 0.8rem 1.5rem;
  border-radius: 8px;
  text-decoration: none;
  margin-top: 1rem;
  font-weight: 700;
  transition: var(--transition);
}

.explore-button:hover {
  filter: brightness(1.1);
  box-shadow: 0 0 15px var(--primary);
}

/* --- Chatbot UI --- */
.chatbot {
  position: fixed;
  bottom: 20px;
  right: 20px;
  width: 300px;
  background: #1e293b;
  border: 1px solid var(--primary);
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 10px 25px rgba(0,0,0,0.5);
}

.chat-header {
  background: var(--primary);
  padding: 10px;
  font-size: 0.8rem;
  font-weight: bold;
}

.chat-body {
  height: 200px;
  padding: 10px;
  overflow-y: auto;
  font-size: 0.9rem;
}

#chatInput {
  width: 100%;
  padding: 10px;
  border: none;
  background: #334155;
  color: white;
  outline: none;
}

