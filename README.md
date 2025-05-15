<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Lokesh Yechina - Portfolio</title>
  <style>
    /* ====== BASE & RESET ====== */
    * {
      box-sizing: border-box;
      margin: 0; padding: 0;
      scroll-behavior: smooth;
    }
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #0f111a 0%, #1a1c2a 100%);
      color: #cbd5e1;
      line-height: 1.6;
      padding: 20px;
      max-width: 900px;
      margin: 0 auto 50px auto;
      user-select: none;
    }
    a {
      color: #00f7ff;
      text-decoration: none;
      transition: color 0.3s ease;
    }
    a:hover, a:focus {
      color: #00c6ff;
      outline: none;
    }
    h1, h2, h3 {
      color: #00f7ff;
      text-align: center;
      text-shadow: 0 0 10px #00f7ff88;
    }
    h3 {
      color: #81a1c1;
      font-weight: 400;
      margin-bottom: 1.5em;
    }
    hr {
      border: none;
      border-top: 1.5px solid #2e3440;
      margin: 3em 0;
      box-shadow: 0 0 10px #00f7ff33;
    }

    /* ====== HEADER ====== */
    header {
      margin-bottom: 40px;
    }
    header h1 {
      font-size: 3rem;
      margin-bottom: 0.1em;
    }
    header h3 {
      font-size: 1.4rem;
      letter-spacing: 1.5px;
    }

    /* ====== TYPING ANIMATION ====== */
    .typing-container {
      margin: 0 auto 60px auto;
      font-size: 28px;
      font-weight: 700;
      font-family: 'Courier New', Courier, monospace;
      color: #00f7ff;
      width: 600px;
      max-width: 90vw;
      white-space: nowrap;
      overflow: hidden;
      border-right: 4px solid #00f7ff;
      animation: blinkCursor 1s steps(2, start) infinite;
      text-align: center;
      user-select: none;
    }
    @keyframes blinkCursor {
      0%, 100% { border-color: #00f7ff; }
      50% { border-color: transparent; }
    }

    /* ====== SECTIONS ====== */
    section {
      margin-bottom: 50px;
    }
    section h2 {
      font-size: 2.2rem;
      margin-bottom: 1rem;
      position: relative;
    }
    section h2::after {
      content: '';
      display: block;
      width: 60px;
      height: 3px;
      background: #00f7ff;
      margin: 0.5em auto 0 auto;
      border-radius: 2px;
      box-shadow: 0 0 10px #00f7ff66;
    }

    /* ====== ABOUT ME ====== */
    #about ul {
      list-style: none;
      padding-left: 0;
      max-width: 650px;
      margin: 0 auto;
    }
    #about ul li {
      background: #1c1e2a;
      margin-bottom: 15px;
      padding: 14px 20px;
      border-radius: 12px;
      box-shadow: 0 0 10px #00f7ff33;
      font-size: 1.15rem;
      position: relative;
      cursor: default;
      transition: transform 0.3s ease;
    }
    #about ul li:hover {
      transform: translateX(12px);
      box-shadow: 0 0 25px #00f7ffaa;
    }
    #about ul li::before {
      content: '🌟';
      position: absolute;
      left: 15px;
      top: 50%;
      transform: translateY(-50%);
      font-size: 1.3rem;
    }

    /* ====== TECH STACK ====== */
    #tech-stack {
      text-align: center;
    }
    .tech-stack {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
      margin-top: 20px;
    }
    .tech-stack img {
      height: 50px;
      border-radius: 10px;
      box-shadow: 0 0 15px #00f7ff88;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      cursor: pointer;
    }
    .tech-stack img:hover {
      transform: scale(1.15) rotate(10deg);
      box-shadow: 0 0 30px #00f7ffcc;
    }

    /* ====== PROJECTS ====== */
    #projects ul {
      list-style: none;
      padding-left: 0;
      max-width: 700px;
      margin: 0 auto;
    }
    #projects ul li {
      background: #1c1e2a;
      margin-bottom: 20px;
      padding: 18px 22px;
      border-radius: 15px;
      box-shadow: 0 0 10px #00f7ff33;
      cursor: default;
      font-size: 1.1rem;
      transition: box-shadow 0.3s ease, transform 0.3s ease;
      position: relative;
    }
    #projects ul li:hover {
      box-shadow: 0 0 25px #00f7ffbb;
      transform: translateY(-6px);
    }
    #projects ul li::before {
      content: '🔹';
      position: absolute;
      left: 18px;
      top: 50%;
      transform: translateY(-50%);
      font-size: 1.3rem;
    }
    #projects p {
      text-align: center;
      font-style: italic;
      margin-top: 10px;
      color: #81a1c1;
    }

    /* ====== GITHUB STATS ====== */
    #stats {
      text-align: center;
    }
    #stats img {
      max-width: 350px;
      width: 45vw;
      margin: 15px 15px 30px 15px;
      border-radius: 15px;
      box-shadow: 0 0 20px #00f7ffbb;
      transition: transform 0.3s ease;
      cursor: pointer;
    }
    #stats img:hover {
      transform: scale(1.1);
      box-shadow: 0 0 40px #00f7ffee;
    }

    /* ====== CONTACT ====== */
    #contact {
      text-align: center;
    }
    #contact p {
      margin-top: 10px;
    }
    #contact a {
      display: inline-block;
      margin: 0 12px;
      transition: transform 0.3s ease;
      border-radius: 12px;
      box-shadow: 0 0 12px #00f7ff70;
    }
    #contact a:hover {
      transform: scale(1.2);
      box-shadow: 0 0 25px #00f7ffcc;
    }
    #contact a img {
      height: 48px;
      width: auto;
      display: block;
      border-radius: 12px;
    }

    /* ====== SKILLS PROGRESS BARS ====== */
    #skills {
      max-width: 650px;
      margin: 0 auto;
    }
    .skill {
      margin-bottom: 18px;
    }
    .skill-name {
      font-size: 1.1rem;
      margin-bottom: 6px;
      letter-spacing: 0.05em;
      color: #81a1c1;
    }
    .progress-bar {
      background: #1c1e2a;
      border-radius: 20px;
      box-shadow: inset 0 0 8px #000;
      height: 22px;
      overflow: hidden;
    }
    .progress {
      height: 100%;
      background: linear-gradient(90deg, #00f7ff, #00c6ff);
      width: 0%;
      border-radius: 20px;
      transition: width 2s ease-in-out;
      box-shadow: 0 0 10px #00f7ffcc;
    }

    /* ====== RESPONSIVE ====== */
    @media (max-width: 700px) {
      body {
        padding: 10px;
        max-width: 100vw;
      }
      .typing-container {
        width: 90vw;
        font-size: 22px;
      }
      #tech-stack img {
        height: 40px;
      }
      #stats img {
        max-width: 90vw;
        width: 90vw;
      }
    }
    @media (max-width: 400px) {
      header h1 {
        font-size: 2.2rem;
      }
      header h3 {
        font-size: 1rem;
      }
      section h2 {
        font-size: 1.7rem;
      }
      .skill-name {
        font-size: 1rem;
      }
    }
  </style>
</head>
<body>

<header>
  <h1>Hi 👋, I'm Lokesh Yechina</h1>
  <h3>CSE Student | Data Science Intern | Web Developer</h3>
</header>

<div class="typing-container" id="typing"></div>

<section id="about" aria-label="About Me Section">
  <h2>🌟 About Me</h2>
  <ul>
    <li>🎓 Final Year Computer Science Student (Data Science Specialization)</li>
    <li>💼 Currently interning as a <strong>Data Science Intern at Prodigy InfoTech</strong></li>
    <li>💻 Passionate about building websites, machine learning models, and data visualizations</li>
    <li>✍️ Consistency, growth, and self-learning are my core values</li>
    <li>🌱 Exploring Deep Learning, Backend Development & Cloud (AWS)</li>
  </ul>
</section>

<hr />

<section id="tech-stack" aria-label="Technology Stack Section">
  <h2>🔧 Tech Stack</h2>
  <div class="tech-stack" aria-live="polite">
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" title="Python" />
    <img src="https://img.shields.io/badge/HTML5-e34c26?style=for-the-badge&logo=html5&logoColor=white" alt
