# myportfolio
my project Amazon clone
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Dilkesh | Developer Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background-color: #0f172a;
      color: #f8fafc;
      scroll-behavior: smooth;
    }

    nav {
      background-color: #1e293b;
      display: flex;
      justify-content: space-between;
      padding: 20px 60px;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 999;
    }

    nav .left {
      font-size: 1.8rem;
      font-weight: bold;
      color: #38bdf8;
      padding-left: 40px;
    }

    nav ul {
      display: flex;
      gap: 30px;
      list-style: none;
    }

    nav ul li a {
      text-decoration: none;
      color: white;
      font-weight: 500;
      transition: color 0.3s;
    }

    nav ul li a:hover {
      color: #38bdf8;
    }

    .firstSection {
      display: flex;
      justify-content: space-around;
      align-items: center;
      padding: 100px 40px;
      flex-wrap: wrap;
      background: linear-gradient(to bottom, #0f172a, #1e293b);
    }

    .leftSection {
      max-width: 500px;
      font-size: 2.5rem;
    }

    .leftSection span.purple {
      color: #a78bfa;
    }

    .leftSection .buttons {
      margin-top: 40px;
    }

    .leftSection .btn {
      padding: 12px 24px;
      background-color: #38bdf8;
      color: #0f172a;
      border: none;
      font-size: 1rem;
      font-weight: bold;
      border-radius: 8px;
      margin-right: 20px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .leftSection .btn:hover {
      background-color: #0ea5e9;
    }

    .rightSection img {
      width: 350px;
      border-radius: 16px;
      animation: float 3s ease-in-out infinite;
    }

    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-15px); }
      100% { transform: translateY(0px); }
    }

    .secondSection {
      max-width: 90%;
      margin: auto;
      padding: 60px 20px;
    }

    .secondSection h1 {
      font-size: 2rem;
      text-align: center;
      margin-bottom: 40px;
      color: #38bdf8;
    }

    .box {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 40px;
      justify-items: center;
    }

    .vertical {
      background: #1e293b;
      padding: 20px;
      border-radius: 12px;
      text-align: center;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
      transition: transform 0.3s;
    }

    .vertical:hover {
      transform: translateY(-10px);
    }

    .image-top {
      width: 50px;
      margin-bottom: 15px;
    }

    .vertical-title {
      font-size: 1.1rem;
      font-weight: bold;
      margin-bottom: 8px;
    }

    .vertical-desc {
      font-size: 0.85rem;
      color: #cbd5e1;
    }

    footer {
      background-color: #0f172a;
      padding: 60px 20px 20px;
      color: #cbd5e1;
    }

    .footer {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 30px;
      max-width: 1100px;
      margin: auto;
    }

    .footer div ul {
      list-style: none;
    }

    .footer div h3 {
      margin-bottom: 10px;
      color: #38bdf8;
    }

    .footer ul li {
      margin-bottom: 8px;
      cursor: pointer;
    }

    .text-right {
      text-align: center;
      margin-top: 40px;
      font-size: 0.85rem;
      color: #94a3b8;
    }

    @media(max-width: 768px) {
      .leftSection {
        text-align: center;
      }

      nav {
        flex-direction: column;
        gap: 10px;
      }

      nav ul {
        flex-direction: column;
        gap: 10px;
      }
    }

    /* Sidebar */
    .sidebar {
      position: fixed;
      top: 0;
      left: -250px;
      height: 100vh;
      width: 250px;
      background-color: #1e293b;
      padding: 60px 20px;
      box-shadow: 2px 0 8px rgba(0,0,0,0.2);
      transition: left 0.3s ease;
      z-index: 999;
    }

    .sidebar h2 {
      color: #38bdf8;
      margin-bottom: 30px;
      font-size: 2.5rem;
    }

    .sidebar ul {
      list-style: none;
      padding: 0;
    }

    .sidebar ul li {
      margin: 20px 0;
    }

    .sidebar ul li a {
      color: #f8fafc;
      text-decoration: none;
      font-size: 1rem;
      font-weight: 500;
      transition: color 0.2s;
    }

    .sidebar ul li a:hover {
      color: #38bdf8;
    }

    .sidebar.active {
      left: 0;
    }

  </style>
</head>
<body>

<!-- Sidebar Toggle Button -->
<button id="sidebarToggle" title="Toggle Sidebar" aria-label="Toggle Sidebar" style="position: fixed; top: 20px; left: 20px; z-index: 1000; background: #38bdf8; border: none; padding: 10px 15px; border-radius: 8px; cursor: pointer;">
  ☰
</button>

<!-- Sidebar -->
<div id="sidebar" class="sidebar">
  <h2>Menu</h2>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Account Sign In</a></li>
    <li><a href="#">Settings</a></li>
    <li><a href="#">Help</a></li>
    <li><a href="#">Feedback</a></li>
  </ul>
</div>

<!-- Navigation -->
<nav>
  <div class="left">Dilkesh</div>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Services</a></li>
    <li><a href="#">Projects</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>

<!-- Hero Section -->
<section class="firstSection">
  <div class="leftSection">
    Hi, My name is <span class="purple">Dilkesh</span>  
    <div>and I am a passionate</div>
    <span id="element"></span>
    <div class="buttons">
      <button class="btn">My Amazon Clone</button>
      <button class="btn">Contact Me</button>
    </div>
  </div>
  <div class="rightSection">
    <img src="pg2.png" alt="Dilkesh Image">
  </div>
</section>

<!-- Work Experience Section -->
<section class="secondSection">
  <h1>My Work Experience</h1>
  <div class="box">
    <div class="vertical">
      <img class="image-top" src="videogame.jpg" alt="icon">
      <div class="vertical-title">HTML Developer</div>
      <div class="vertical-desc">Built responsive layouts and animated interfaces for web games and static sites.</div>
    </div>
    <div class="vertical">
      <img class="image-top" src="facebooklogo.png" alt="icon">
      <div class="vertical-title">Node.js Dev - Facebook</div>
      <div class="vertical-desc">Worked with Node.js backend microservices and GraphQL APIs.</div>
    </div>
    <div class="vertical">
      <img class="image-top" src="twiterlogo.png" alt="icon">
      <div class="vertical-title">Frontend Dev - Twitter</div>
      <div class="vertical-desc">Optimized Twitter widgets and timeline performance.</div>
    </div>
    <div class="vertical">
      <img class="image-top" src="githublogo.png" alt="icon">
      <div class="vertical-title">Open Source - GitHub</div>
      <div class="vertical-desc">Maintained and contributed to open-source React components.</div>
    </div>
  </div>
</section>

<!-- Footer -->
<footer>
  <div class="footer">
    <div>
      <h3>Quick Links</h3>
      <ul><li>Home</li><li>About</li><li>Projects</li></ul>
    </div>
    <div>
      <h3>Connect</h3>
      <ul><li>LinkedIn</li><li>GitHub</li><li>Twitter</li></ul>
    </div>
    <div>
      <h3>Resources</h3>
      <ul><li>Resume</li><li>Skills</li><li>Certificates</li></ul>
    </div>
  </div>
  <div class="text-right">© 2025 Dilkesh's Portfolio. All rights reserved.</div>
</footer>

<!-- Scripts -->
<script src="https://unpkg.com/typed.js@2.1.0/dist/typed.umd.js"></script>
<script>
  var typed = new Typed('#element', {
    strings: ['Web Developer.', 'Video Designer.', 'Creative Coder.', 'UI/UX Enthusiast.'],
    typeSpeed: 60,
    backSpeed: 40,
    loop: true
  });

  const toggleBtn = document.getElementById('sidebarToggle');
  const sidebar = document.getElementById('sidebar');

  toggleBtn.addEventListener('click', () => {
    sidebar.classList.toggle('active');
  });
</script>

</body>
</html>
