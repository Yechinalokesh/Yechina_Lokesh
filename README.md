<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Lokesh Yechina | Portfolio</title>
  <style>
    /* Reset & Base */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Segoe UI', sans-serif;
      background: #0f172a;
      color: #e2e8f0;
      line-height: 1.6;
      scroll-behavior: smooth;
    }

    a { color: #38bdf8; text-decoration: none; transition: 0.3s; }
    a:hover { color: #0ea5e9; }

    header, footer, section {
      padding: 60px 10%;
    }

    header {
      background: linear-gradient(to right, #1e293b, #334155);
      text-align: center;
    }

    header h1 {
      font-size: 3.5rem;
      margin-bottom: 10px;
    }

    header p {
      font-size: 1.2rem;
      color: #94a3b8;
    }

    nav {
      display: flex;
      justify-content: center;
      background: #1e293b;
      padding: 10px;
      gap: 20px;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    nav a {
      font-weight: 500;
    }

    section h2 {
      font-size: 2rem;
      margin-bottom: 20px;
      border-left: 4px solid #38bdf8;
      padding-left: 12px;
    }

    .about, .contact {
      max-width: 800px;
      margin: auto;
    }

    .skills {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      justify-content: center;
    }

    .skills span {
      background: #1e293b;
      padding: 10px 16px;
      border-radius: 6px;
      font-weight: bold;
    }

    .projects {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 25px;
    }

    .project-card {
      background: #1e293b;
      padding: 20px;
      border-radius: 12px;
      transition: 0.3s;
      border: 1px solid transparent;
    }

    .project-card:hover {
      border-color: #38bdf8;
      transform: translateY(-5px);
    }

    .project-card h3 {
      color: #facc15;
      margin-bottom: 10px;
    }

    footer {
      text-align: center;
      color: #94a3b8;
      font-size: 0.9rem;
      background: #0f172a;
    }

    .wave {
      position: relative;
      height: 100px;
      background: url('https://i.ibb.co/VCqMptT/wave.png') repeat-x;
      animation: wave 8s linear infinite;
    }

    @keyframes wave {
      0% { background-position-x: 0; }
      100% { background-position-x: 1000px; }
    }

    /* Scroll Reveal */
    .reveal {
      opacity: 0;
      transform: translateY(30px);
      transition: all 1s ease;
    }

    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }

    /* Responsive Typography */
    @media (max-width: 600px) {
      header h1 { font-size: 2.4rem; }
      nav { flex-wrap: wrap; gap: 10px; }
    }
  </style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#projects">Projects</a>
    <a href="#contact">Contact</a>
  </nav>

  <!-- HEADER -->
  <header>
    <h1>Hi, I'm Lokesh Yechina 👋</h1>
    <p>CS Engineer | Data Science Intern | Web Developer | UI Designer</p>
  </header>

  <!-- ABOUT -->
  <section id="about" class="reveal about">
    <h2>💻 About Me</h2>
    <p>🎓 Final-year CSE undergrad at Vignan Institute of Technology and Science.<br/>
    💼 Currently a Data Science Intern @ Prodigy InfoTech.<br/>
    🔍 Passionate about Python, ML, Web Dev, and VLSI.<br/>
    🎮 Love anime, tech, and solving real-world problems with code.</p>
  </section>

  <!-- SKILLS -->
  <section id="skills" class="reveal">
    <h2>🚀 Skills</h2>
    <div class="skills">
      <span>Python</span>
      <span>Java</span>
      <span>JavaScript</span>
      <span>React.js</span>
      <span>HTML</span>
      <span>CSS</span>
      <span>SQL</span>
      <span>Tableau</span>
      <span>Node.js</span>
      <span>Embedded C</span>
    </div>
  </section>

  <!-- PROJECTS -->
  <section id="projects" class="reveal">
    <h2>🌟 Featured Projects</h2>
    <div class="projects">
      <div class="project-card">
        <h3>Blood Bank Website</h3>
        <p>A responsive platform for blood donations and requests.</p>
        <p><strong>Tech:</strong> HTML, CSS, JavaScript</p>
        <a href="#">GitHub Repo →</a>
      </div>
      <div class="project-card">
        <h3>Solar Tricycle Brake System</h3>
        <p>Prototype for automatic braking in tricycles using sensors.</p>
        <p><strong>Tech:</strong> Embedded C, Sensors</p>
        <a href="#">GitHub Repo →</a>
      </div>
      <div class="project-card">
        <h3>Movie Dashboard</h3>
        <p>Insights on Nani's films and ratings using Power BI.</p>
        <p><strong>Tech:</strong> Power BI</p>
        <a href="#">GitHub Repo →</a>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" class="reveal contact">
    <h2>🔗 Contact Me</h2>
    <p>📧 Email: <a href="mailto:lokeshyechina@gmail.com">lokeshyechina@gmail.com</a></p>
    <p>💻 GitHub: <a href="https://github.com/YechinaLokesh" target="_blank">@YechinaLokesh</a></p>
  </section>

  <!-- WAVE & FOOTER -->
  <div class="wave"></div>
  <footer>
    <p>Made with ❤️ by Lokesh Yechina</p>
  </footer>

  <!-- JavaScript -->
  <script>
    // Reveal on Scroll
    const reveals = document.querySelectorAll('.reveal');
    window.addEventListener('scroll', () => {
      for (let i = 0; i < reveals.length; i++) {
        const windowHeight = window.innerHeight;
        const elementTop = reveals[i].getBoundingClientRect().top;
        if (elementTop < windowHeight - 50) {
          reveals[i].classList.add('active');
        }
      }
    });
  </script>
</body>
</html>
