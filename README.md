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
    margin: 3rem auto;
    padding: 2rem 3rem;
    background: rgba(20, 0, 40, 0.75);
    border-radius: 20px;
    box-shadow: 0 0 15px 5px #9400ff88, inset 0 0 25px #7a00ff88;
  }

  /* Title with neon glow */
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
      text-shadow:
        0 0 5px #ff00de,
        0 0 10px #ff00de,
        0 0 20px #ff00de,
        0 0 40px #ff00de;
      color: #ff00de;
    }
    100% {
      text-shadow:
        0 0 20px #ff6eff,
        0 0 30px #ff6eff,
        0 0 40px #ff6eff,
        0 0 60px #ff6eff;
      color: #ff6eff;
    }
  }

  /* Glitch effect for subtitle */
  .glitch {
    position: relative;
    color: #fff;
    font-weight: 900;
    font-size: 2rem;
    text-align: center;
    margin-bottom: 2rem;
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
    border-left: 2px solid #ff33cc;
    padding-left: 10px;
    white-space: pre-wrap;
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
    margin: 1rem 0;
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
    <h1>Lokesh Yechina</h1>
    <div class="glitch" data-text="About Me"></div>

    <div id="typed" class="typed-container"></div>

    <div class="skills">
      <h2>My Skills</h2>
      <div class="skill">
        <div class="skill-name">React.js</div>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-skill="90%"></div>
        </div>
      </div>
      <div class="skill">
        <div class="skill-name">JavaScript (ES6+)</div>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-skill="85%"></div>
        </div>
      </div>
      <div class="skill">
        <div class="skill-name">HTML5 &amp; CSS3</div>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-skill="95%"></div>
        </div>
      </div>
      <div class="skill">
        <div class="skill-name">Node.js &amp; Express</div>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-skill="75%"></div>
        </div>
      </div>
      <div class="skill">
        <div class="skill-name">Python &amp; Data Science</div>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-skill="80%"></div>
        </div>
      </div>
    </div>

    <div class="social">
      <a href="https://github.com/YechinaLokesh" target="_blank" title="GitHub" aria-label="GitHub">
        <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" height="32" width="32" viewBox="0 0 24 24"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.387.6.113.82-.258.82-.577v-2.234c-3.338.724-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.757-1.333-1.757-1.089-.744.083-.729.083-.729 1.205.085 1.84 1.236 1.84 1.236 1.07 1.834 2.809 1.304 3.495.997.107-.775.418-1.305.762-1.605-2.665-.305-5.466-1.333-5.466-5.93 0-1.312.47-2.382 1.235-3.222-.124-.303-.535-1.523.117-3.176 0 0 1.008-.322 3.301 1.23a11.52 11.52 0 013.003-.404c1.018.005 2.042.138 3.003.404 2.289-1.552 3.295-1.23 3.295-1.23.654 1.653.243 2.873.12 3.176.77.84 1.23 1.91 1.23 3.222 0 4.61-2.804 5.624-5.475 5.922.43.372.823 1.103.823 2.222v3.293c0 .321.218.694.825.576 4.765-1.59 8.198-6.086 8.198-11.387 0-6.627-5.373-12-12-12z"/></svg>
      </a>
      <a href="https://linkedin.com/in/yechina-lokesh" target="_blank" title="LinkedIn" aria-label="LinkedIn">
        <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" height="32" width="32" viewBox="0 0 24 24"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.761 0 5-2.239 5-5v-14c0-2.761-2.239-5-5-5zm-11.75 19h-3v-11h3v11zm-1.5-12.268c-.967 0-1.75-.783-1.75-1.75s.783-1.75 1.75-1.75c.967 0 1.75.783 1.75 1.75s-.783 1.75-1.75 1.75zm13.25 12.268h-3v-5.604c0-1.337-.025-3.06-1.865-3.06-1.867 0-2.154 1.46-2.154 2.963v5.701h-3v-11h2.88v1.507h.041c.401-.758 1.379-1.56 2.839-1.56 3.037 0 3.6 2 3.6 4.59v6.463z"/></svg>
      </a>
      <a href="mailto:lokeshyechina@gmail.com" target="_blank" title="Email" aria-label="Email">
        <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" height="32" width="32" viewBox="0 0 24 24"><path d="M12 13.5l-11-8.5h22l-11 8.5zm0 1.5l11-8.5v12h-22v-12l11 8.5z"/></svg>
      </a>
    </div>

    <footer>
      &copy; 2025 Lokesh Yechina | Built with ❤️ and a bit of neon magic
    </footer>
  </div>

  <script>
    // Typed text effect for About Me
    const typedText = `I'm Lokesh Yechina, a passionate Computer Science & Engineering student specializing in Data Science and Web Development. 
Skilled in React.js, JavaScript, Python, and designing sleek, user-friendly interfaces. 
Always eager to learn new technologies and solve complex problems with clean, efficient code. 
Currently exploring AI, machine learning, and modern front-end frameworks. 
Let's build something amazing together!`;

    const typedContainer = document.getElementById('typed');
    let idx = 0;
    let speed = 40; // typing speed in ms

    function typeWriter() {
      if (idx < typedText.length) {
        if (typedText[idx] === '\n') {
          typedContainer.innerHTML += '<br />';
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

    document.addEventListener('DOMContentLoaded', animateSkills);
  </script>

</body>
</html>
