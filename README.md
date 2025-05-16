import React, { useEffect, useState } from "react";

const typingText = "Hey there, I’m Lokesh Yechina 👨‍💻";

export default function Profile() {
  const [displayedText, setDisplayedText] = useState("");
  const [index, setIndex] = useState(0);

  useEffect(() => {
    if (index < typingText.length) {
      const timeout = setTimeout(() => {
        setDisplayedText((prev) => prev + typingText[index]);
        setIndex(index + 1);
      }, 100);
      return () => clearTimeout(timeout);
    }
  }, [index]);

  return (
    <div className="min-h-screen bg-gradient-to-br from-gray-900 via-gray-800 to-gray-900 text-gray-200 p-8 font-sans max-w-4xl mx-auto">
      {/* Typing Animation Header */}
      <h1 className="text-4xl md:text-5xl font-bold mb-6 tracking-wide">
        <span className="border-r-4 border-cyan-400 pr-2 animate-blink-caret">
          {displayedText}
        </span>
      </h1>
      <p className="italic text-lg mb-10">— Turning code into impact, one line at a time.</p>

      {/* About Me Section */}
      <section className="mb-12">
        <h2 className="text-3xl font-semibold mb-4 text-cyan-400">🧠 About Me</h2>
        <ul className="space-y-2 text-lg">
          <li><strong>🎓</strong> CSE (Data Science) @ <span className="text-cyan-300 font-semibold">VITS</span></li>
          <li><strong>💼</strong> Data Science Intern @ <span className="text-cyan-300 font-semibold">Prodigy InfoTech</span></li>
          <li><strong>🧑‍💻</strong> Web Developer | Python Enthusiast | Problem Solver</li>
          <li><strong>⚡</strong> Passionate about building innovative solutions and vibing to anime tunes</li>
          <li><strong>🎯</strong> Mission: Harnessing tech to solve real-world challenges and create value</li>
          <li><strong>☕</strong> Code. Create. Iterate. Repeat.</li>
        </ul>
      </section>

      {/* Tech Stack */}
      <section className="mb-12">
        <h2 className="text-3xl font-semibold mb-4 text-cyan-400">🧰 Tech Stack</h2>
        <p className="text-lg">Python | JavaScript | HTML & CSS | Power BI | Machine Learning | Data Analysis | React.js</p>
      </section>

      {/* GitHub Analytics & Contribution */}
      <section className="mb-12">
        <h2 className="text-3xl font-semibold mb-4 text-cyan-400">📈 GitHub Analytics</h2>
        <p className="mb-6">Visualize my coding journey — growing commit by commit.</p>
        <div className="bg-gray-800 rounded-lg p-6 flex justify-center items-center h-40">
          {/* Placeholder for GitHub contribution graph or animated SVG */}
          <p className="text-gray-400 italic">[GitHub contribution graph animation here]</p>
        </div>
      </section>

      {/* Projects Snapshot */}
      <section className="mb-12">
        <h2 className="text-3xl font-semibold mb-6 text-cyan-400">🔥 Projects Snapshot</h2>
        <table className="w-full table-auto border-collapse border border-gray-700 text-left">
          <thead>
            <tr className="bg-cyan-700">
              <th className="border border-gray-600 p-3">💼 Project</th>
              <th className="border border-gray-600 p-3">⚙️ Tech Stack</th>
              <th className="border border-gray-600 p-3">📌 Status</th>
            </tr>
          </thead>
          <tbody>
            <tr className="hover:bg-gray-700">
              <td className="border border-gray-600 p-3">🩸 Blood Bank System</td>
              <td className="border border-gray-600 p-3">HTML, CSS, JavaScript</td>
              <td className="border border-gray-600 p-3 text-yellow-300 font-semibold">Coming Soon</td>
            </tr>
            <tr className="hover:bg-gray-700">
              <td className="border border-gray-600 p-3">🎥 Movie Dashboard (Nani)</td>
              <td className="border border-gray-600 p-3">Power BI</td>
              <td className="border border-gray-600 p-3 text-blue-400 font-semibold">In Progress</td>
            </tr>
            <tr className="hover:bg-gray-700">
              <td className="border border-gray-600 p-3">🎬 Movie Rating Prediction</td>
              <td className="border border-gray-600 p-3">Python, Machine Learning</td>
              <td className="border border-gray-600 p-3 text-green-400 font-semibold">Building...</td>
            </tr>
            <tr className="hover:bg-gray-700">
              <td className="border border-gray-600 p-3">🎮 Just Vibes</td>
              <td className="border border-gray-600 p-3 italic">Details Coming Soon</td>
              <td className="border border-gray-600 p-3 text-gray-400 italic">Planning</td>
            </tr>
          </tbody>
        </table>
      </section>

      {/* Connect With Me */}
      <section className="mb-12">
        <h2 className="text-3xl font-semibold mb-4 text-cyan-400">📡 Connect With Me</h2>
        <p className="mb-4 text-lg">
          Let’s collaborate, share ideas, and create something amazing!
        </p>
        <div className="flex space-x-6 text-2xl">
          <a href="https://github.com/YechinaLokesh" target="_blank" rel="noopener noreferrer" aria-label="GitHub" className="hover:text-cyan-400 transition">
            <svg
              fill="currentColor"
              viewBox="0 0 24 24"
              className="w-8 h-8"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path d="M12 0C5.37 0 0 5.37 0 12c0 5.3 3.438 9.8 8.205 11.387.6.113.82-.26.82-.577v-2.234c-3.338.726-4.033-1.61-4.033-1.61-.546-1.387-1.333-1.756-1.333-1.756-1.09-.746.082-.73.082-.73 1.205.085 1.838 1.238 1.838 1.238 1.07 1.835 2.807 1.305 3.492.997.107-.775.418-1.305.762-1.605-2.665-.3-5.466-1.334-5.466-5.93 0-1.31.47-2.38 1.235-3.22-.125-.303-.535-1.523.115-3.176 0 0 1.005-.322 3.3 1.23a11.5 11.5 0 013.003-.404c1.02.005 2.045.138 3.003.404 2.28-1.552 3.285-1.23 3.285-1.23.655 1.653.245 2.873.12 3.176.77.84 1.235 1.91 1.235 3.22 0 4.61-2.8 5.625-5.475 5.92.43.37.82 1.1.82 2.22v3.293c0 .32.215.694.825.576C20.565 21.795 24 17.297 24 12c0-6.63-5.37-12-12-12z" />
            </svg>
          </a>
          <a href="https://linkedin.com/in/yechinalokesh" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn" className="hover:text-cyan-400 transition">
            <svg
              fill="currentColor"
              viewBox="0 0 24 24"
              className="w-8 h-8"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path d="M19 0h-14c-2.762 0-5 2.238-5 5v14c0 2.763 2.238 5 5 5h14c2.763 0 5-2.237 5-5v-14c0-2.762-2.237-5-5-5zm-11 19h-3v-10h3v10zm-1.5-11.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764c.967 0 1.75.79 1.75 1.764s-.783 1.764-1.75 1.764zm13.5 11.268h-3v-5.6c0-3.4-4-3.15-4 0v5.6h-3v-10h3v1.43c1.396-2.586 7-2.777 7 2.476v6.094z" />
            </svg>
          </a>
          <a href="mailto:lokeshyechina@gmail.com" aria-label="Email" className="hover:text-cyan-400 transition text-3xl">
            📧
          </a>
        </div>
      </section>

      <footer className="text-center text-gray-500 text-sm pt-10 border-t border-gray-700">
        Thanks for stopping by — <span className="font-semibold">Keep building, keep dreaming 🚀</span>
      </footer>

      {/* Typing caret animation styles */}
      <style jsx>{`
        @keyframes blink-caret {
          0%, 100% { border-color: transparent; }
          50% { border-color: #22d3ee; }
        }
        .animate-blink-caret {
          border-right: 4px solid #22d3ee;
          animation: blink-caret 1s step-end infinite;
        }
      `}</style>
    </div>
  );
}
