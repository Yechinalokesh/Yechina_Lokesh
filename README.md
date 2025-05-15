<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Lokesh Yechina | About Me</title>
<style>
  /* Basic Reset */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  html, body {
    height: 100%;
    font-family: 'Poppins', sans-serif;
    background: #0f0f18;
    color: #eee;
    overflow-x: hidden;
  }
  /* Neon glowing gradient background with subtle animation */
  body {
    background: linear-gradient(270deg, #0f0f18, #150024, #0f0f18);
    background-size: 600% 600%;
    animation: gradientBG 15s ease infinite;
  }
  @keyframes gradientBG {
    0% {background-position: 0% 50%;}
    50% {background-position: 100% 50%;}
    100% {background-position: 0% 50%;}
  }
  /* Container */
  .container {
    max-width: 900px;
    margin: 2rem auto;
    padding: 2rem;
    background: rgba(20, 0, 40, 0.75);
    border-radius: 20px;
    box-shadow: 0 0 15px 5px #9400ff88, inset 0 0 25px #7a00ff88;
  }
  /* Title with glitch effect */
  h1 {
    font-size: 3rem;
    font-weight: 900;
    text-align: center;
    margin-bottom: 1rem;
    position: relative;
    color: #e600ff;
    animation: neonGlow 2s ease-in-out infinite alternate;
  }
  @keyframes neonGlow {
    0% {
      text-shadow: 0 0 5px #ff00de, 0 0 10px #ff00de, 0 0 20px #ff00de, 0 0 40px #ff00de;
      color: #ff00de;
    }
    100% {
      text-shadow: 0 0 20px #ff6eff, 0 0 30px #ff6eff, 0 0 40px #ff6eff, 0 0 60px #ff6eff;
      color: #ff6eff;
    }
  }
  /* Glitch Effect */
  .glitch {
    position: relative;
    color: #fff;
    font-weight: 900;
    font-size: 2rem;
  }
  .glitch::before, .glitch::after {
    content: attr(data-text);
    position: absolute;
    left: 0;
    width: 100%;
    overflow: hidden;
    clip: rect(0, 900px, 0, 0);
  }
  .glitch::before {
    animation: glitchTop 2s infinite linear alternate-reverse;
    color: #ff00c8;
    z-index: -1;
  }
  .glitch::after {
    animation: glitchBottom 2s infinite linear alternate-reverse;
    color: #00fff7;
    z-index: -2;
  }
  @keyframes glitchTop {
    0% {
      clip: rect(0, 900px, 5px, 0);
      transform: translate(-2px, -2px);
    }
    50% {
      clip: rect(2px, 900px, 8px, 0);
      transform: translate(2px, 2px);
    }
    100% {
      clip: rect(0, 900px, 5px, 0);
      transform: translate(-2px, -2px);
    }
  }
  @keyframes glitchBottom {
    0% {
      clip: rect(10px, 900px, 15px, 0);
      transform: translate(2px, 2px);
    }
    50% {
      clip: rect(12px, 900px, 18px, 0);
      transform: translate(-2px, -2px);
    }
    100% {
      clip: rect(10px, 900px, 15px, 0);
      transform: translate(2px, 2px);
    }
  }
  /* Typed text container */
  .typed-container {
    font-size: 1.2rem;
    margin: 1rem auto 2rem;
    max-width: 600px;
    text-align: center;
    line-height: 1.5;
    color: #ddd;
    min-height: 80px;
    font-family: 'Courier New', Courier, monospace;
  }
  /* Animated Skill bars */
  .skills {
    margin-top: 2rem;
  }
  .skills h2 {
    color: #ff4dff;
    text-align: center;
    margin-bottom: 1rem;
    font-weight: 700;
    text-shadow: 0 0 10px #ff00ffaa;
  }
  .skill {
    margin: 0.8rem 0;
  }
  .skill-name {
    font-weight: 700;
    margin-bottom: 0.3rem;
  }
  .skill-bar {
    background: #2e004f;
    border-radius: 15px;
    overflow: hidden;
  }
  .skill-bar-fill {
    height: 20px;
    width: 0;
    background: linear-gradient(90deg, #ff00cc, #6600ff);
    box-shadow: 0 0 15px #ff00ccaa;
    border-radius: 15px;
    transition: width 1.5s ease-in-out;
  }
  /* Social icons */
  .social {
    text-align: center;
    margin-top: 3rem;
  }
  .social a {
    display: inline-block;
    margin: 0 15px;
    text-decoration: none;
    color: #ff33cc;
    font-size: 2rem;
    transition: transform 0.3s ease, color 0.3s ease;
    filter: drop-shadow(0 0 5px #ff33cc);
  }
  .social a:hover {
    color: #ffffff;
    transform: scale(1.3) rotate(10deg);
    filter: drop-shadow(0 0 20px #ff33cc);
  }
  /* Footer */
  footer {
    margin-top: 3rem;
    text-align: center;
    color: #880088aa;
    font-style: italic;
    font-size: 0.9rem;
  }
  /* Responsive */
  @media (max-width: 600px) {
    h1 {
      font-size: 2.2rem;
    }
    .skills {
      max-width: 100%;
      padding: 0 1rem;
    }
    .typed-container {
      font-size: 1rem;
      padding: 0 1rem;
    }
  }
</style>
</head>
<body>

<div class="container">
  <h1 class="glitch" data-text="Lokesh Yechina">Lokesh Yechina</h1>

  <div class="typed-container" id="typed"></div>

  <div class="skills">
    <h2>My Skills</h2>
    <div class="skill">
      <div class="skill-name">React.js</div>
      <div class="skill-bar"><div class="skill-bar-fill" data-skill="90%"></div></div>
    </div>
    <div class="skill">
      <div class="skill-name">JavaScript (ES6+)</div>
      <div class="skill-bar"><div class="skill-bar-fill" data-skill="85%"></div></div>
    </div>
    <div class="skill">
      <div class="skill-name">HTML5 & CSS3</div>
      <div class="skill-bar"><div class="skill-bar-fill" data-skill="95%"></div></div>
    </div>
    <div class="skill">
      <div class="skill-name">Node.js & Express</div>
      <div class="skill-bar"><div class="skill-bar-fill" data-skill="80%"></div></div>
    </div>
    <div class="skill">
      <div class="skill-name">Python & Data Science</div>
      <div class="skill-bar"><div class="skill-bar-fill" data-skill="75%"></div></div>
    </div>
  </div>

  <div class="social">
    <!-- Add your social links here -->
    <a href="#" aria-label="GitHub" title="GitHub" target="_blank" rel="noopener noreferrer">🐙</a>
    <a href="#" aria-label="LinkedIn" title="LinkedIn" target="_blank" rel="noopener noreferrer">🔗</a>
    <a href="#" aria-label="Twitter" title="Twitter" target="_blank" rel="noopener noreferrer">🐦</a>
  </div>

  <footer>© 2025 Lokesh Yechina | Built with ❤️ and a bit of neon magic</footer>
</div>

<script>
  // Typed text effect for About Me
  const typedText = `I'm Lokesh Yechina, a passionate Computer Science & Engineering student specializing in Data Science and Web Development. Skilled in React.js, JavaScript, Python, and designing sleek, user-friendly interfaces. Always eager to learn new technologies and solve complex problems with clean, efficient code. Currently exploring AI, machine learning, and modern front-end frameworks. Let's build something amazing together!`;
  const typedContainer = document.getElementById('typed');
  let idx = 0;
  let speed = 40; // typing speed in ms

  function typeWriter() {
    if (idx < typedText.length) {
      if (typedText[idx] === '\n') {
        typedContainer.innerHTML += '<br>';
      } else {
        typedContainer.innerHTML += typedText.charAt(idx);
      }
      idx++;
      setTimeout(typeWriter, speed);
    }
  }
  typeWriter();

  // Animate skill bars on scroll into view
  function animateSkills() {
    const skillFills = document.querySelectorAll('.skill-bar-fill');
    skillFills.forEach(bar => {
      const skillPercent = bar.getAttribute('data-skill');
      bar.style.width = skillPercent;
    });
  }
  // Trigger animation once DOM content loaded
  document.addEventListener('DOMContentLoaded', animateSkills);
</script>

</body>
</html>
