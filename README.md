<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Iced Executor</title>
  <meta name="description" content="Iced Executor open source executor">
  <link rel="icon" type="image/png" href="ice.jpg">

  <style>
    html { scroll-behavior: smooth; }

    body {
      background-color: #0a0a0a;
      color: #e0f7fa;
      font-family: Verdana, sans-serif;
      margin: 0;
      overflow-x: hidden;
    }

    /* === Welcome message === */
    #welcome {
      position: fixed;
      top: 20%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: rgba(0, 207, 255, 0.2);
      color: #00f7ff;
      padding: 2rem 3rem;
      border-radius: 12px;
      font-size: 1.5rem;
      font-weight: bold;
      text-align: center;
      box-shadow: 0 0 30px #00f7ff;
      opacity: 0;
      animation: fadeInMove 1.5s forwards, fadeOut 1s 3s forwards;
      z-index: 999;
    }

    @keyframes fadeInMove {
      0% { opacity: 0; transform: translate(-50%, -70%) scale(0.8); }
      100% { opacity: 1; transform: translate(-50%, -50%) scale(1); }
    }

    @keyframes fadeOut {
      to { opacity: 0; transform: translate(-50%, -50%) scale(0.8); }
    }

    header {
      text-align: center;
      padding: 2.5rem;
      background: linear-gradient(120deg, #00cfff, #0055ff);
      color: white;
      animation: glow 3s infinite alternate;
    }

    @keyframes glow {
      from { box-shadow: 0 0 10px #00cfff; }
      to { box-shadow: 0 0 35px #00ffff; }
    }

    .header-logo {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 1rem;
    }

    .header-logo img {
      width: 52px;
      filter: drop-shadow(0 0 10px #00f7ff);
      animation: float 4s ease-in-out infinite;
    }

    @keyframes float {
      0%,100% { transform: translateY(0); }
      50% { transform: translateY(-6px); }
    }

    .tagline {
      font-style: italic;
      opacity: 0.85;
      margin-top: 0.5rem;
    }

    main {
      max-width: 900px;
      margin: 2rem auto;
      padding: 1rem;
    }

    section {
      margin-bottom: 2rem;
      padding: 1.4rem;
      background: rgba(255,255,255,0.05);
      border-radius: 14px;
      transition: transform .4s ease, box-shadow .4s ease;
    }

    section:hover {
      transform: translateY(-4px);
      box-shadow: 0 10px 25px rgba(0,247,255,.15);
    }

    p { line-height: 1.6; transition: color .3s, text-shadow .3s; }
    p:hover { color:#fff; text-shadow:0 0 8px #00f7ff; }

    a { text-decoration:none; }
    a:hover { text-decoration: underline; }

    ul { list-style:none; padding:0; }
    ul li::before { content:"❄️ "; padding-right:0.3rem; }

    /* Gallery 3D tilt */
    .gallery { perspective: 1000px; }
    .tilt { perspective: 1000px; }
    .gallery img {
      width:100%;
      margin-top:1.2rem;
      border-radius:14px;
      box-shadow:0 15px 40px rgba(0,247,255,.25);
      transform-style: preserve-3d;
      transition: box-shadow .3s ease;
      will-change: transform;
    }

    /* Download buttons */
    .download-btn {
      display:inline-block;
      margin-top:1rem;
      padding:.85rem 1.8rem;
      background: linear-gradient(120deg,#00cfff,#0077ff);
      color:#001122;
      font-weight:bold;
      border-radius:12px;
      box-shadow:0 0 15px #00f7ff;
      transition: transform .25s, box-shadow .25s;
    }
    .download-btn:hover {
      transform: translateY(-3px) scale(1.08);
      box-shadow:0 0 25px #00f7ff,0 0 45px #00ffff;
    }

    /* Bigger Link buttons */
    .link-buttons {
      display:flex;
      flex-wrap:wrap;
      justify-content:center;
      gap:1rem;
      margin-top:1rem;
    }

    .link-buttons a {
      display:inline-block;
      padding:1rem 2rem;
      background:linear-gradient(120deg,#00cfff,#0077ff);
      color:#001122;
      font-weight:bold;
      font-size:1.1rem;
      border-radius:12px;
      text-decoration:none;
      box-shadow:0 0 15px #00f7ff;
      transition: transform .25s, box-shadow .25s;
    }
    .link-buttons a:hover {
      transform: translateY(-3px) scale(1.08);
      box-shadow:0 0 25px #00f7ff,0 0 45px #00ffff;
    }

    footer {
      text-align:center;
      padding:1rem;
      font-size:.9rem;
      background:#001122;
      color:#a0e0ff;
    }

    @media(max-width:600px){
      header h1 { font-size:1.6rem; }
      .header-logo { flex-direction:column; }
    }
  </style>
</head>

<body>

<!-- Welcome Message -->
<div id="welcome">Welcome to Iced Executor ❄️</div>

<header>
  <div class="header-logo">
    <img src="ice.jpg" alt="Iced Executor logo">
    <h1>❄️ Iced Executor</h1>
  </div>
  <p class="tagline">Clean. Fast. Experimental.</p>
</header>

<main>

<section>
  <h2>What is Iced Executor?</h2>
  <p>Iced Executor is a <strong>roblox executor project</strong> focused on UI design.</p>
</section>

<section>
  <h2>Features</h2>
  <ul>
    <li>Minimal & icy UI</li>
    <li>Fast startup philosophy</li>
    <li>Custom script editor</li>
  </ul>
</section>

<section class="gallery">
  <h2>Gallery</h2>
  <p>Move mouse over images for real 3D tilt ❄️</p>
  <div class="tilt"><img src="preview.jpg" alt="Preview"></div>
  <div class="tilt"><img src="ice.jpg" alt="Logo"></div>
</section>

<section>
  <h2>Downloads</h2>
  <a class="download-btn" href="https://download.com" target="_blank">Download Mirror 1</a>
  <a class="download-btn" href="https://download.com" target="_blank">Download Mirror 2</a>
  <a class="download-btn" href="https://download.com" target="_blank">Download Mirror 3</a>
</section>

<section>
  <h2>Links</h2>
  <div class="link-buttons">
    <a href="https://discord.gg/E8XbUzUn" target="_blank">Discord</a>
    <a href="page2.html">Changelog</a>
    <a href="credits.html">Credits</a>
    <a href="https://github.com/coptfinxzi-dev">github</a>
  </div>
</section>

</main>

<footer>
  <p>© 2026 Iced Executor</p>
</footer>

<script src="script.js"></script>
<script>
  // Show welcome message on load
  window.addEventListener('load', () => {
    const welcome = document.getElementById('welcome');
    setTimeout(() => {
      welcome.style.display = 'none';
    }, 4000); // automaticky zmizí po 4.5s
  });
</script>

</body>
</html>
