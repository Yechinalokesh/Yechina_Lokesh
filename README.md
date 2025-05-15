<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Lokesh Yechina - Dynamic Portfolio README</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

  /* Reset */
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body {
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #1f1c2c, #928dab);
    color: #eee;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 40px 20px;
  }

  header {
    text-align: center;
    margin-bottom: 2rem;
  }
  header h1 {
    font-size: 3rem;
    color: #ff6f61;
    animation: neonGlow 2s ease-in-out infinite alternate;
  }
  @keyframes neonGlow {
    from {
      text-shadow:
        0 0 5px #ff6f61,
        0 0 10px #ff6f61,
        0 0 20px #ff6f61,
        0 0 40px #ff6f61,
        0 0 80px #ff6f61;
    }
    to {
      text-shadow: none;
    }
  }
  header p {
    font-size: 1.2rem;
    margin-top: 10px;
    color: #ccc;
    letter-spacing: 2px;
  }

  /* Typing effect container */
  .typing-container {
    font-size: 1.5rem;
    font-weight: 600;
    margin-top: 20px;
    min-height: 40px;
    color: #ffb997;
    border-right: 2px solid #ffb997;
    white-space: nowrap;
    overflow: hidden;
  }

  /* Main content grid */
  main {
    max-width: 900px;
    width: 100%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
    margin-bottom: 3rem;
  }
  @media (max-width: 700px) {
    main {
      grid-template-columns: 1fr;
    }
  }

  section {
    background: rgba(255,255,255,0.05);
    padding: 2rem;
    border-radius: 12px;
    box-shadow:
      0 0 10px rgba(255, 255, 255, 0.1),
      inset 0 0 20px rgba(255, 255, 255, 0.2);
  }

  h2 {
    color: #ff6f61;
    margin-bottom: 1rem;
    border-bottom: 2px solid #ff6f61;
    padding-bottom: 6px;
    letter-spacing: 1.5px;
  }

  ul {
    list-style-type: none;
  }
  ul li {
    margin: 10px 0;
    font-size: 1.1rem;
  }
  ul li::before {
    content: "▶";
    margin-right: 8px;
    color: #ffb997;
  }

  /* Animated skill bars */
  .skill {
    margin-bottom: 15px;
  }
  .skill-name {
    font-weight: 600;
    margin-bottom: 5px;
  }
  .skill-bar {
    width: 100%;
    background: #222;
    border-radius: 10px;
    overflow: hidden;
  }
  .skill-progress {
    height: 15px;
    background: #ff6f61;
    width: 0;
    border-radius: 10px;
    animation-fill-mode: forwards;
  }

  /* Animate progress bars with delay */
  .skill-progress.python { animation: fillBar 2s forwards 0.2s; }
  .skill-progress.js { animation: fillBar 2s forwards 0.4s; }
  .skill-progress.sql { animation: fillBar 2s forwards 0.6s; }
  .skill-progress.react { animation: fillBar 2s forwards 0.8s; }
  .skill-progress.ml { animation: fillBar 2s forwards 1.0s; }

  @keyframes fillBar {
    to { width: var(--progress); }
  }

  /* Contact Buttons */
  .contact-links {
    display: flex;
    gap: 20px;
    justify-content: center;
    flex-wrap: wrap;
  }
  .contact-links a {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: #ff6f61;
    color: white;
    text-decoration: none;
    padding: 12px 18px;
    border-radius: 8px;
    font-weight: 600;
    transition: background 0.3s ease;
  }
  .contact-links a:hover {
    background: #ff3b2f;
  }

  /* Footer */
  footer {
    margin-top: 3rem;
    font-size: 0.9rem;
    color: #aaa;
  }
</style>
</head>
<body>

<header>
  <h1>Lokesh Yechina</h1>
  <p>Data Scientist | AI Enthusiast | Web & VLSI Developer</p>
  <div class="typing-container" id="typing"></div>
</header>

<main>
  <section>
    <h2>About Me</h2>
    <p>Hi, I'm Lokesh! Passionate about Data Science, Artificial Intelligence, and building impactful solutions. Skilled in Python, Java, SQL, and React. Constantly learning and exploring new technologies. Let's build something amazing together!</p>
  </section>

  <section>
    <h2>Skills & Expertise</h2>
    <div class="skill">
      <div class="skill-name">Python</div>
      <div class="skill-bar"><div class="skill-progress python" style="--progress: 90%;"></div></div>
    </div>
    <div class="skill">
      <div class="skill-name">JavaScript</div>
      <div class="skill-bar"><div class="skill-progress js" style="--progress: 75%;"></div></div>
    </div>
    <div class="skill">
      <div class="skill-name">SQL</div>
      <div class="skill-bar"><div class="skill-progress sql" style="--progress: 80%;"></div></div>
    </div>
    <div class="skill">
      <div class="skill-name">React.js</div>
      <div class="skill-bar"><div class="skill-progress react" style="--progress: 70%;"></div></div>
    </div>
    <div class="skill">
      <div class="skill-name">Machine Learning</div>
      <div class="skill-bar"><div class="skill-progress ml" style="--progress: 65%;"></div></div>
    </div>
  </section>

  <section>
    <h2>Projects</h2>
    <ul>
      <li><strong>Blood Bank Management System</strong> - Responsive website for blood donation and requests.</li>
      <li><strong>Solar Tricycle Auto Braking System</strong> - Prototype for automatic braking on solar tricycles.</li>
      <li><strong>Movie Rating Prediction</strong> - Machine learning model predicting movie ratings.</li>
    </ul>
  </section>

  <section>
    <h2>Contact Me</h2>
    <div class="contact-links">
      <a href="mailto:lokeshyechina@gmail.com" target="_blank" rel="noopener noreferrer">📧 Email</a>
      <a href="https://linkedin.com/in/yechinalokesh" target="_blank" rel="noopener noreferrer">🔗 LinkedIn</a>
      <a href="https://github.com/YechinaLokesh" target="_blank" rel="noopener noreferrer">🐙 GitHub</a>
      <a href="https://twitter.com/yechinalokesh" target="_blank" rel="noopener noreferrer">🐦 Twitter</a>
    </div>
  </section>
</main>

<footer>
  &copy; 2025 Lokesh Yechina — Made with ❤️ and Code
</footer>

<script>
  // Typing animation script
  const typingEl = document.getElementById('typing');
  const phrases = [
    'Data Scientist.',
    'AI & ML Enthusiast.',
    'Open Source Contributor.',
    'Web & VLSI Developer.',
    'Lover of Code & Coffee ☕'
  ];

  let phraseIndex = 0;
  let letterIndex = 0;
  let currentText = '';
  let isDeleting = false;
  let typingSpeed = 120;

  function type() {
    const currentPhrase = phrases[phraseIndex];
    if (isDeleting) {
      currentText = currentPhrase.substring(0, letterIndex--);
    } else {
      currentText = currentPhrase.substring(0, letterIndex++);
    }

    typingEl.textContent = currentText;

    if (!isDeleting && letterIndex === currentPhrase.length + 1) {
      isDeleting = true;
      typingSpeed = 50;
      setTimeout(type, 1500);
    } else if (isDeleting && letterIndex === 0) {
      isDeleting = false;
      phraseIndex = (phraseIndex + 1) % phrases.length;
      typingSpeed = 120;
      setTimeout(type, 300);
      return;
    }

    setTimeout(type, typingSpeed);
  }

  type();
</script>

</body>
</html>
