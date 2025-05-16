<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Lokesh Yechina - Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;500;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Roboto', sans-serif;
    }

    body {
      background: linear-gradient(to right, #0f2027, #203a43, #2c5364);
      color: #fff;
      padding: 20px;
    }

    header {
      text-align: center;
      padding: 40px 0 20px;
    }

    header h1 {
      font-size: 3rem;
    }

    header p {
      font-size: 1.2rem;
      color: #a8dadc;
    }

    section {
      margin: 40px 0;
      background: rgba(255, 255, 255, 0.05);
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
    }

    h2 {
      border-bottom: 2px solid #00b4d8;
      padding-bottom: 10px;
      margin-bottom: 20px;
    }

    .about, .skills, .projects, .contact {
      padding: 10px 0;
    }

    .skills-icons {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .skills-icons span {
      background: #1d3557;
      padding: 8px 14px;
      border-radius: 5px;
      font-size: 1rem;
    }

    .project-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }

    .project-card {
      background: #1a1a2e;
      border-radius: 10px;
      padding: 20px;
      transition: transform 0.3s ease;
    }

    .project-card:hover {
      transform: scale(1.05);
    }

    .project-card h3 {
      margin-bottom: 10px;
      color: #ffd166;
    }

    .project-card p {
      font-size: 0.9rem;
      color: #ccc;
    }

    .project-card a {
      display: inline-block;
      margin-top: 10px;
      color: #06d6a0;
      text-decoration: none;
    }

    .contact p, .contact a {
      font-size: 1.1rem;
      color: #f1faee;
    }

    footer {
      text-align: center;
      margin-top: 60px;
      font-size: 0.9rem;
      color: #b0bec5;
    }

    .wave {
      position: absolute;
      bottom: 0;
      width: 100%;
      height: 120px;
      background: url('https://i.ibb.co/VCqMptT/wave.png') repeat-x;
      animation: wave 6s linear infinite;
    }

    @keyframes wave {
      0% {
        background-position-x: 0;
      }
      100% {
        background-position-x: 1000px;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Hi, I'm Lokesh Yechina 👋</h1>
    <p>Computer Science & Engineering Student | Data Science Intern | Web Developer</p>
  </header>

  <section class="about">
    <h2>💻 About Me</h2>
    <p>🎓 CSE Undergrad at Vignan Institute of Technology and Science</p>
    <p>💼 Data Science Intern at Prodigy InfoTech</p>
    <p>🔍 Python | Machine Learning | Web Development | VLSI</p>
    <p>🎮 Anime Fan | Tech Tinkerer | Curious Learner</p>
  </section>

  <section class="skills">
    <h2>🚀 Skills</h2>
    <div class="skills-icons">
      <span>Python</span>
      <span>Java</span>
      <span>JavaScript</span>
      <span>React</span>
      <span>HTML</span>
      <span>CSS</span>
      <span>SQL</span>
      <span>Tableau</span>
      <span>Node.js</span>
      <span>Embedded C</span>
    </div>
  </section>

  <section class="projects">
    <h2>🌟 Featured Projects</h2>
    <div class="project-grid">
      <div class="project-card">
        <h3>Blood Bank Website</h3>
        <p>A responsive platform for blood donations and requests.</p>
        <p><strong>Tech Stack:</strong> HTML, CSS, JavaScript</p>
        <a href="#">GitHub Repo</a>
      </div>
      <div class="project-card">
        <h3>Solar Tricycle Brake System</h3>
        <p>A prototype for automatic braking in tricycles using sensors.</p>
        <p><strong>Tech Stack:</strong> Embedded C, Sensors</p>
        <a href="#">GitHub Repo</a>
      </div>
      <div class="project-card">
        <h3>Movie Dashboard</h3>
        <p>Dashboard providing insights on Nani's filmography and ratings.</p>
        <p><strong>Tech Stack:</strong> Power BI</p>
        <a href="#">GitHub Repo</a>
      </div>
    </div>
  </section>

  <section class="contact">
    <h2>🔗 Contact</h2>
    <p>Email: <a href="mailto:lokeshyechina@gmail.com">lokeshyechina@gmail.com</a></p>
    <p>GitHub: <a href="https://github.com/YechinaLokesh" target="_blank">@YechinaLokesh</a></p>
  </section>

  <footer>
    <p>Made with ❤️ by Lokesh Yechina</p>
  </footer>

  <div class="wave"></div>
</body>
</html>
