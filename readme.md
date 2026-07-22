<!-- README.md -->
<!-- This is a fully graphical, animated, website-style profile README for Saumil Prajapati. -->

<div align="center">

<!-- ====== ANIMATED BACKGROUND ====== -->
<style>
  /* Reset and base */
  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: #0f0c29;  /* fallback for old browsers */
    background: -webkit-linear-gradient(to right, #24243e, #302b63, #0f0c29);
    background: linear-gradient(to right, #24243e, #302b63, #0f0c29);
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    min-height: 100vh;
    padding: 20px;
  }

  /* Floating particles (CSS only) */
  .particles {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: 0;
    overflow: hidden;
  }

  .particle {
    position: absolute;
    background: rgba(255, 255, 255, 0.08);
    border-radius: 50%;
    animation: float linear infinite;
  }

  @keyframes float {
    0% { transform: translateY(100vh) scale(0); opacity: 0; }
    10% { opacity: 1; }
    90% { opacity: 1; }
    100% { transform: translateY(-10vh) scale(1); opacity: 0; }
  }

  /* Generate 30 particles with random sizes, positions, and durations */
  .particle:nth-child(1) { width: 10px; height: 10px; left: 5%; animation-duration: 12s; animation-delay: 0s; }
  .particle:nth-child(2) { width: 20px; height: 20px; left: 15%; animation-duration: 18s; animation-delay: 2s; }
  .particle:nth-child(3) { width: 8px; height: 8px; left: 25%; animation-duration: 14s; animation-delay: 4s; }
  .particle:nth-child(4) { width: 25px; height: 25px; left: 35%; animation-duration: 20s; animation-delay: 1s; }
  .particle:nth-child(5) { width: 12px; height: 12px; left: 45%; animation-duration: 16s; animation-delay: 3s; }
  .particle:nth-child(6) { width: 18px; height: 18px; left: 55%; animation-duration: 22s; animation-delay: 5s; }
  .particle:nth-child(7) { width: 6px; height: 6px; left: 65%; animation-duration: 13s; animation-delay: 2.5s; }
  .particle:nth-child(8) { width: 30px; height: 30px; left: 75%; animation-duration: 19s; animation-delay: 0.5s; }
  .particle:nth-child(9) { width: 15px; height: 15px; left: 85%; animation-duration: 17s; animation-delay: 4.5s; }
  .particle:nth-child(10) { width: 22px; height: 22px; left: 95%; animation-duration: 21s; animation-delay: 3.5s; }
  .particle:nth-child(11) { width: 9px; height: 9px; left: 10%; animation-duration: 15s; animation-delay: 6s; }
  .particle:nth-child(12) { width: 17px; height: 17px; left: 20%; animation-duration: 23s; animation-delay: 1.5s; }
  .particle:nth-child(13) { width: 11px; height: 11px; left: 30%; animation-duration: 14s; animation-delay: 7s; }
  .particle:nth-child(14) { width: 24px; height: 24px; left: 40%; animation-duration: 19s; animation-delay: 0.2s; }
  .particle:nth-child(15) { width: 7px; height: 7px; left: 50%; animation-duration: 16s; animation-delay: 5.5s; }
  .particle:nth-child(16) { width: 19px; height: 19px; left: 60%; animation-duration: 20s; animation-delay: 2.8s; }
  .particle:nth-child(17) { width: 13px; height: 13px; left: 70%; animation-duration: 18s; animation-delay: 4.2s; }
  .particle:nth-child(18) { width: 28px; height: 28px; left: 80%; animation-duration: 22s; animation-delay: 1.8s; }
  .particle:nth-child(19) { width: 16px; height: 16px; left: 90%; animation-duration: 15s; animation-delay: 6.5s; }
  .particle:nth-child(20) { width: 21px; height: 21px; left: 98%; animation-duration: 17s; animation-delay: 3.2s; }

  /* Main container - glassmorphism */
  .profile-container {
    position: relative;
    z-index: 1;
    max-width: 1100px;
    margin: 0 auto;
    padding: 20px;
  }

  /* Glass card */
  .glass {
    background: rgba(255, 255, 255, 0.07);
    backdrop-filter: blur(12px);
    -webkit-backdrop-filter: blur(12px);
    border-radius: 30px;
    border: 1px solid rgba(255, 255, 255, 0.12);
    box-shadow: 0 20px 50px rgba(0, 0, 0, 0.4);
    padding: 30px;
    margin-bottom: 30px;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    color: #fff;
  }

  .glass:hover {
    transform: translateY(-5px);
    box-shadow: 0 30px 60px rgba(0, 0, 0, 0.6);
  }

  /* Headings */
  h1, h2, h3 {
    font-weight: 600;
    letter-spacing: 0.5px;
  }

  h1 {
    font-size: 3rem;
    background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    display: inline-block;
  }

  h2 {
    font-size: 2rem;
    margin-bottom: 20px;
    color: #fff;
    border-bottom: 2px solid rgba(255,255,255,0.1);
    padding-bottom: 10px;
  }

  .typing-wrapper {
    margin: 20px 0;
  }

  /* Skill progress bars */
  .skill-bar {
    margin: 12px 0;
  }

  .skill-bar .label {
    display: flex;
    justify-content: space-between;
    font-size: 0.95rem;
    margin-bottom: 4px;
  }

  .skill-bar .bar {
    height: 10px;
    background: rgba(255,255,255,0.15);
    border-radius: 20px;
    overflow: hidden;
  }

  .skill-bar .bar .fill {
    height: 100%;
    width: 0%;
    background: linear-gradient(90deg, #f093fb, #f5576c);
    border-radius: 20px;
    transition: width 1.5s ease;
  }

  .skill-bar .bar .fill.animate {
    width: var(--width);
  }

  /* Badges inline */
  .badge-group {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
  }

  .badge-group img {
    transition: transform 0.2s;
  }

  .badge-group img:hover {
    transform: scale(1.1);
  }

  /* Project cards */
  .project-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    margin-top: 20px;
  }

  .project-card {
    background: rgba(255,255,255,0.05);
    border-radius: 20px;
    padding: 20px;
    border: 1px solid rgba(255,255,255,0.08);
    transition: 0.3s;
  }

  .project-card:hover {
    background: rgba(255,255,255,0.12);
    transform: scale(1.02);
  }

  /* Stats */
  .stats-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
  }

  .stats-grid img {
    max-width: 100%;
    border-radius: 15px;
  }

  /* Connect icons */
  .social-icons {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 15px;
    margin-top: 10px;
  }

  .social-icons a {
    display: inline-block;
    transition: 0.3s;
  }

  .social-icons a:hover {
    transform: translateY(-5px) scale(1.1);
  }

  /* Responsive */
  @media (max-width: 600px) {
    h1 { font-size: 2rem; }
    .glass { padding: 20px; }
  }

  /* custom scrollbar */
  ::-webkit-scrollbar { width: 8px; }
  ::-webkit-scrollbar-track { background: rgba(255,255,255,0.05); }
  ::-webkit-scrollbar-thumb { background: linear-gradient(#f093fb, #f5576c); border-radius: 10px; }

  /* Remove default body margin from GitHub's rendered view */
  body { margin: 0; padding: 0; background: transparent; }
</style>

<!-- ====== PARTICLES ====== -->
<div class="particles">
  <div class="particle"></div><div class="particle"></div><div class="particle"></div>
  <div class="particle"></div><div class="particle"></div><div class="particle"></div>
  <div class="particle"></div><div class="particle"></div><div class="particle"></div>
  <div class="particle"></div><div class="particle"></div><div class="particle"></div>
  <div class="particle"></div><div class="particle"></div><div class="particle"></div>
  <div class="particle"></div><div class="particle"></div><div class="particle"></div>
  <div class="particle"></div><div class="particle"></div>
</div>

<!-- ====== MAIN CONTENT ====== -->
<div class="profile-container">

  <!-- HERO -->
  <div class="glass" style="text-align: center;">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=32&pause=1000&color=00BFFF&center=true&vCenter=true&random=false&width=700&height=100&lines=Hi+%F0%9F%91%8B%2C+I'm+Saumil+Prajapati;Graphic+Designer+%7C+Web+Developer;AI+Enthusiast+%7C+System+Admin;Startup+Co-founder+%40+BusPro" alt="Typing SVG" style="max-width:100%; height:auto; background: transparent;" />

    <div style="margin: 20px 0 10px 0;">
      <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
      <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
      <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram" />
      <img src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter" />
      <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail" />
    </div>

    <div>
      <img src="https://komarev.com/ghpvc/?username=saumilprajapati&label=Profile%20Views&color=0e75b6&style=flat" alt="Profile Views" />
    </div>

    <div style="margin-top: 20px; font-size: 1.1rem; color: rgba(255,255,255,0.85);">
      Student at Parul University · Vadodara, Gujarat, India
    </div>
  </div>

  <!-- ABOUT -->
  <div class="glass">
    <h2>👨‍🎓 About Me</h2>
    <p style="font-size: 1.1rem; line-height: 1.7;">
      I'm a passionate student at <strong>Parul University</strong> with a deep interest in technology and design. 
      I'm actively seeking roles as a <strong>Graphic Designer, AI Engineer, Web Developer, System Administrator, 
      and AI Integration Manager</strong>. I love building impactful solutions and currently co-founding a startup 
      called <strong>BusPro</strong> to revolutionize university transport.
    </p>
    <ul style="list-style: none; padding: 0; margin-top: 15px;">
      <li>🔭 <strong>Working on:</strong> BusPro – a smart transport management platform.</li>
      <li>🌱 <strong>Learning:</strong> Advanced AI, Full-Stack Development, Cybersecurity.</li>
      <li>👯 <strong>Looking to collaborate:</strong> on innovative tech projects with real-world impact.</li>
      <li>💬 <strong>Ask me about:</strong> Web Dev, AI, Graphic Design, or Startup journeys.</li>
      <li>⚡ <strong>Fun fact:</strong> I blend creativity with code to build beautiful and functional solutions.</li>
    </ul>
  </div>

  <!-- SKILLS -->
  <div class="glass">
    <h2>🛠️ Tech Stack & Skills</h2>

    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px,1fr)); gap: 15px;">
      <!-- Programming -->
      <div>
        <h3 style="font-size: 1.2rem; color: #f093fb;">Programming</h3>
        <div class="skill-bar"><div class="label"><span>C</span><span>85%</span></div><div class="bar"><div class="fill animate" style="--width:85%;"></div></div></div>
        <div class="skill-bar"><div class="label"><span>Python</span><span>80%</span></div><div class="bar"><div class="fill animate" style="--width:80%;"></div></div></div>
        <div class="skill-bar"><div class="label"><span>Java</span><span>70%</span></div><div class="bar"><div class="fill animate" style="--width:70%;"></div></div></div>
        <div class="skill-bar"><div class="label"><span>SQL</span><span>75%</span></div><div class="bar"><div class="fill animate" style="--width:75%;"></div></div></div>
      </div>
      <!-- Web -->
      <div>
        <h3 style="font-size: 1.2rem; color: #f093fb;">Web Development</h3>
        <div class="skill-bar"><div class="label"><span>HTML5/CSS3</span><span>90%</span></div><div class="bar"><div class="fill animate" style="--width:90%;"></div></div></div>
        <div class="skill-bar"><div class="label"><span>JavaScript</span><span>80%</span></div><div class="bar"><div class="fill animate" style="--width:80%;"></div></div></div>
        <div class="skill-bar"><div class="label"><span>React</span><span>70%</span></div><div class="bar"><div class="fill animate" style="--width:70%;"></div></div></div>
        <div class="skill-bar"><div class="label"><span>Next.js</span><span>65%</span></div><div class="bar"><div class="fill animate" style="--width:65%;"></div></div></div>
      </div>
      <!-- AI & Design -->
      <div>
        <h3 style="font-size: 1.2rem; color: #f093fb;">AI & Design</h3>
        <div class="skill-bar"><div class="label"><span>Machine Learning</span><span>70%</span></div><div class="bar"><div class="fill animate" style="--width:70%;"></div></div></div>
        <div class="skill-bar"><div class="label"><span>Generative AI</span><span>65%</span></div><div class="bar"><div class="fill animate" style="--width:65%;"></div></div></div>
        <div class="skill-bar"><div class="label"><span>Graphic Design</span><span>85%</span></div><div class="bar"><div class="fill animate" style="--width:85%;"></div></div></div>
        <div class="skill-bar"><div class="label"><span>SEO / Project Mgmt</span><span>75%</span></div><div class="bar"><div class="fill animate" style="--width:75%;"></div></div></div>
      </div>
    </div>

    <div style="margin-top: 25px; text-align: center;">
      <span class="badge-group">
        <img src="https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white" alt="C" />
        <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
        <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML" />
        <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS" />
        <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JS" />
        <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
        <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next" />
        <img src="https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white" alt="Bootstrap" />
        <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind" />
        <img src="https://img.shields.io/badge/Machine_Learning-FF6F00?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="ML" />
        <img src="https://img.shields.io/badge/Generative_AI-412991?style=for-the-badge&logo=openai&logoColor=white" alt="GenAI" />
        <img src="https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white" alt="Databricks" />
        <img src="https://img.shields.io/badge/Graphic_Design-FF5722?style=for-the-badge&logo=adobe&logoColor=white" alt="Design" />
      </span>
    </div>
  </div>

  <!-- EXPERIENCE & PROJECTS -->
  <div class="glass">
    <h2>💼 Experience & Projects</h2>
    <div class="project-grid">
      <div class="project-card">
        <h3 style="color:#f093fb;">🚀 BusPro (Co-founder)</h3>
        <p><strong>Parul University</strong> · Current</p>
        <p>Smart university transport solution. Selected for Pre-Incubation Program under PIERC – VSF 6.0.</p>
        <span style="display:inline-block; margin-top:8px; background:rgba(255,255,255,0.1); padding:4px 12px; border-radius:20px; font-size:0.8rem;">🏆 Incubation Letter Received</span>
      </div>
      <div class="project-card">
        <h3 style="color:#f093fb;">🎨 Freelance Graphic Designer & Web Dev</h3>
        <p><strong>Self-Employed</strong></p>
        <p>Created logos, branding, and responsive websites for diverse clients. Focus on modern aesthetics and usability.</p>
      </div>
      <div class="project-card">
        <h3 style="color:#f093fb;">📊 Python for Data Science Workshop</h3>
        <p><strong>BIT at Parul University</strong></p>
        <p>Hands-on workshop covering career opportunities, logic building, ML, AI, and data-driven decision making.</p>
      </div>
    </div>
  </div>

  <!-- CERTIFICATIONS -->
  <div class="glass">
    <h2>📜 Certifications</h2>
    <ul style="list-style: none; padding: 0; display: flex; flex-wrap: wrap; gap: 15px; justify-content: center;">
      <li style="background:rgba(255,255,255,0.05); padding:10px 20px; border-radius:30px;">✅ Get Started with Databricks for Generative AI – Simplilearn</li>
      <li style="background:rgba(255,255,255,0.05); padding:10px 20px; border-radius:30px;">✅ Getting Started with Microsoft Copilot – Simplilearn</li>
      <li style="background:rgba(255,255,255,0.05); padding:10px 20px; border-radius:30px;">✅ C Programming For Beginners – Udemy</li>
      <li style="background:rgba(255,255,255,0.05); padding:10px 20px; border-radius:30px;">✅ Starting a New Business – HP LIFE</li>
      <li style="background:rgba(255,255,255,0.05); padding:10px 20px; border-radius:30px;">✅ Introduction to Cybersecurity Awareness – HP LIFE</li>
    </ul>
  </div>

  <!-- GITHUB STATS -->
  <div class="glass">
    <h2>📊 GitHub Stats</h2>
    <div class="stats-grid">
      <img src="https://github-readme-stats.vercel.app/api?username=saumilprajapati&show_icons=true&theme=radical&bg_color=00000000&border_color=rgba(255,255,255,0.1)" alt="Stats" />
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=saumilprajapati&layout=compact&theme=radical&bg_color=00000000&border_color=rgba(255,255,255,0.1)" alt="Top Langs" />
    </div>
  </div>

  <!-- CONNECT -->
  <div class="glass" style="text-align: center;">
    <h2>💡 Let's Connect</h2>
    <p style="font-size: 1.1rem; margin-bottom: 15px;">I'm always open to interesting conversations and collaboration.</p>
    <div class="social-icons">
      <a href="https://www.linkedin.com/in/saumil-prajapati-b55643416/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
      <a href="https://github.com/saumilprajapati"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
      <a href="https://www.instagram.com/your-instagram/"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram" /></a>
      <a href="https://twitter.com/your-twitter"><img src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter" /></a>
      <a href="mailto:your-email@example.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail" /></a>
    </div>
  </div>

  <!-- FOOTER WAVE -->
  <div style="margin-top: 30px; text-align: center;">
    <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=120&section=footer" style="width:100%; max-width:1100px; border-radius:0;" />
  </div>

</div> <!-- end container -->
</div>
