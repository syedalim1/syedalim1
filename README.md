
  <style>
    :root {
      --primary: #0abde3;
      --secondary: #00ADB5;
      --dark: #222831;
      --light: #EEEEEE;
      --accent: #FC5185;
    }
    
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #222831 0%, #393e46 100%);
      color: var(--light);
      line-height: 1.6;
      margin: 0;
      padding: 20px;
    }
    
    .container {
      max-width: 800px;
      margin: 0 auto;
      padding: 20px;
    }
    
    .header {
      text-align: center;
      position: relative;
      padding: 20px 0;
      margin-bottom: 40px;
      animation: fadeIn 1s ease-in-out;
    }
    
    .header::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 25%;
      width: 50%;
      height: 3px;
      background: linear-gradient(90deg, transparent, var(--primary), transparent);
    }
    
    h1 {
      font-size: 3rem;
      margin-bottom: 10px;
      position: relative;
      display: inline-block;
    }
    
    h1 span {
      color: var(--primary);
      position: relative;
      display: inline-block;
      animation: wave 2.5s ease-in-out infinite;
    }
    
    .badge {
      display: inline-block;
      background: rgba(10, 189, 227, 0.1);
      color: var(--primary);
      padding: 3px 10px;
      border-radius: 15px;
      font-size: 0.8rem;
      margin: 3px;
      border: 1px solid rgba(10, 189, 227, 0.3);
      transition: all 0.3s ease;
    }
    
    .badge:hover {
      transform: translateY(-2px);
      box-shadow: 0 5px 15px rgba(10, 189, 227, 0.2);
      background: rgba(10, 189, 227, 0.2);
    }
    
    .section {
      background: rgba(255, 255, 255, 0.05);
      border-radius: 10px;
      padding: 25px;
      margin-bottom: 30px;
      position: relative;
      overflow: hidden;
      transition: all 0.3s ease;
      border: 1px solid rgba(255, 255, 255, 0.1);
      animation: slideUp 0.8s ease-out forwards;
      opacity: 0;
    }
    
    .section:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
      background: rgba(255, 255, 255, 0.07);
    }
    
    .section:nth-child(1) { animation-delay: 0.1s; }
    .section:nth-child(2) { animation-delay: 0.3s; }
    .section:nth-child(3) { animation-delay: 0.5s; }
    .section:nth-child(4) { animation-delay: 0.7s; }
    .section:nth-child(5) { animation-delay: 0.9s; }
    
    .section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 3px;
      background: linear-gradient(90deg, var(--primary), var(--accent));
    }
    
    .section-title {
      display: flex;
      align-items: center;
      margin-bottom: 15px;
      color: var(--primary);
    }
    
    .section-icon {
      margin-right: 10px;
      font-size: 1.5rem;
    }
    
    .quote {
      font-style: italic;
      border-left: 3px solid var(--primary);
      padding-left: 15px;
      margin: 20px 0;
      position: relative;
      overflow: hidden;
    }
    
    .quote::after {
      content: '"';
      position: absolute;
      bottom: -20px;
      right: 10px;
      font-size: 4rem;
      opacity: 0.1;
      color: var(--primary);
    }
    
    .tech-stack {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      margin: 20px 0;
    }
    
    .tech-icon {
      width: 50px;
      height: 50px;
      margin: 10px;
      padding: 8px;
      background: rgba(255, 255, 255, 0.1);
      border-radius: 10px;
      transition: all 0.3s ease;
      animation: pulse 2s infinite;
      animation-delay: calc(var(--i) * 0.2s);
    }
    
    .tech-icon:hover {
      transform: translateY(-5px) rotate(5deg);
      background: rgba(255, 255, 255, 0.2);
    }
    
    .toolkit {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
    }
    
    .toolkit-item {
      background: rgba(10, 189, 227, 0.1);
      padding: 8px 15px;
      border-radius: 20px;
      font-size: 0.9rem;
      border: 1px solid rgba(10, 189, 227, 0.3);
      transition: all 0.3s ease;
    }
    
    .toolkit-item:hover {
      background: rgba(10, 189, 227, 0.2);
      transform: scale(1.05);
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    }
    
    .social-links {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 15px;
      margin-top: 30px;
    }
    
    .social-btn {
      display: inline-flex;
      align-items: center;
      padding: 10px 20px;
      background: var(--dark);
      color: var(--light);
      border-radius: 30px;
      text-decoration: none;
      font-weight: 500;
      transition: all 0.3s ease;
      border: 1px solid rgba(255, 255, 255, 0.1);
      position: relative;
      overflow: hidden;
      z-index: 1;
    }
    
    .social-btn::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(45deg, var(--primary), var(--accent));
      z-index: -1;
      transform: scaleX(0);
      transform-origin: left;
      transition: transform 0.5s ease;
    }
    
    .social-btn:hover::before {
      transform: scaleX(1);
    }
    
    .social-btn:hover {
      color: white;
      transform: translateY(-3px);
      box-shadow: 0 7px 15px rgba(0, 0, 0, 0.2);
    }
    
    .social-icon {
      margin-right: 8px;
      font-size: 1.2rem;
    }
    
    .waves {
      position: fixed;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 15vh;
      margin-bottom: -7px;
      min-height: 100px;
      max-height: 150px;
      z-index: -1;
    }
    
    .parallax > use {
      animation: wave-move 25s cubic-bezier(0.55, 0.5, 0.45, 0.5) infinite;
    }
    
    .parallax > use:nth-child(1) {
      animation-delay: -2s;
      animation-duration: 7s;
      fill: rgba(10, 189, 227, 0.1);
    }
    
    .parallax > use:nth-child(2) {
      animation-delay: -3s;
      animation-duration: 10s;
      fill: rgba(10, 189, 227, 0.2);
    }
    
    .parallax > use:nth-child(3) {
      animation-delay: -4s;
      animation-duration: 13s;
      fill: rgba(10, 189, 227, 0.3);
    }
    
    .parallax > use:nth-child(4) {
      animation-delay: -5s;
      animation-duration: 20s;
      fill: rgba(10, 189, 227, 0.4);
    }
    
    .typing-effect {
      overflow: hidden;
      white-space: nowrap;
      border-right: 3px solid var(--primary);
      width: 0;
      animation: typing 3s steps(40) forwards, blink-caret 0.75s step-end infinite;
    }
    
    .particles {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
    }
    
    .particle {
      position: absolute;
      width: 6px;
      height: 6px;
      background: var(--primary);
      border-radius: 50%;
      opacity: 0.5;
      animation: float 15s linear infinite;
    }
    
    @keyframes float {
      0% {
        transform: translateY(0) rotate(0deg);
        opacity: 0.5;
      }
      50% {
        opacity: 0.3;
      }
      100% {
        transform: translateY(-100vh) rotate(360deg);
        opacity: 0;
      }
    }
    
    @keyframes wave {
      0%, 100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-5px);
      }
    }
    
    @keyframes pulse {
      0%, 100% {
        transform: scale(1);
      }
      50% {
        transform: scale(1.1);
      }
    }
    
    @keyframes wave-move {
      0% {
        transform: translate3d(-90px, 0, 0);
      }
      100% {
        transform: translate3d(85px, 0, 0);
      }
    }
    
    @keyframes typing {
      from { width: 0 }
      to { width: 100% }
    }
    
    @keyframes blink-caret {
      from, to { border-color: transparent }
      50% { border-color: var(--primary) }
    }
    
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    
    @keyframes slideUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .rotating-border {
      position: relative;
      border-radius: 10px;
      padding: 3px;
      background: linear-gradient(90deg, var(--primary), var(--accent), var(--primary));
      background-size: 200% 200%;
      animation: rotatingGradient 3s linear infinite;
    }

    .rotating-content {
      background: var(--dark);
      border-radius: 8px;
      padding: 20px;
    }

    @keyframes rotatingGradient {
      0% {
        background-position: 0% 50%;
      }
      50% {
        background-position: 100% 50%;
      }
      100% {
        background-position: 0% 50%;
      }
    }

    .glow {
      text-shadow: 0 0 5px var(--primary), 0 0 10px var(--primary), 0 0 15px var(--primary);
    }
  </style>

<body>
  <div class="particles" id="particles">
    <!-- Particles will be added with JS -->
  </div>

  <svg class="waves" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 24 150 28" preserveAspectRatio="none" shape-rendering="auto">
    <defs>
      <path id="gentle-wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z" />
    </defs>
    <g class="parallax">
      <use xlink:href="#gentle-wave" x="48" y="0" />
      <use xlink:href="#gentle-wave" x="48" y="3" />
      <use xlink:href="#gentle-wave" x="48" y="5" />
      <use xlink:href="#gentle-wave" x="48" y="7" />
    </g>
  </svg>

  <div class="container">
    <div class="header">
      <h1>👋 Hi there, I'm <span>Syed Ali M</span></h1>
      <div id="typing-container" style="height: 30px; margin: 15px 0;">
        <div class="typing-effect" id="typing-text">Founder & CEO of CodeNovaTech</div>
      </div>
      <div style="margin-top: 15px;">
        <span class="badge">AI Automation Strategist</span>
        <span class="badge">Full-Stack Developer</span>
        <span class="badge">Tech with Purpose</span>
        <span class="badge">Impact with Code</span>
      </div>
    </div>

    <div class="section">
      <div class="section-title">
        <div class="section-icon">🚀</div>
        <h2>Who Am I?</h2>
      </div>
      <div class="rotating-border">
        <div class="rotating-content">
          <p><span class="glow">🌟</span> Founder & CEO of <strong>CodeNovaTech</strong> — revolutionizing web & app development with <strong>AI-powered solutions</strong>.</p>
          <p><span class="glow">🎓</span> Final-year Computer Science student with a deep passion for automation & innovation.</p>
          <p><span class="glow">💼</span> I specialize in creating scalable full-stack systems and tools that <strong>code, design & deploy themselves</strong>.</p>
          <p><span class="glow">🎯</span> My goal: To bridge the gap between vision and execution using tech.</p>
        </div>
      </div>
    </div>

    <div class="section">
      <div class="section-title">
        <div class="section-icon">🔭</div>
        <h2>What Drives Me?</h2>
      </div>
      <div class="quote">
        "I don't just build code. I build companies, ecosystems, and intelligent workflows."
      </div>
      <p><span class="glow">⚡</span> Currently focused on:</p>
      <ul>
        <li>AI-first development platforms</li>
        <li>Auto-generation of UI, backend & APIs</li>
        <li>Smart developer workflows using machine intelligence</li>
      </ul>
    </div>

    <div class="section">
      <div class="section-title">
        <div class="section-icon">🧠</div>
        <h2>Tech Arsenal</h2>
      </div>
      <div class="tech-stack">
        <div class="tech-icon" style="--i:0;">
          <img src="/api/placeholder/40/40" alt="HTML" />
        </div>
        <div class="tech-icon" style="--i:1;">
          <img src="/api/placeholder/40/40" alt="CSS" />
        </div>
        <div class="tech-icon" style="--i:2;">
          <img src="/api/placeholder/40/40" alt="JavaScript" />
        </div>
        <div class="tech-icon" style="--i:3;">
          <img src="/api/placeholder/40/40" alt="React" />
        </div>
        <div class="tech-icon" style="--i:4;">
          <img src="/api/placeholder/40/40" alt="Node.js" />
        </div>
        <div class="tech-icon" style="--i:5;">
          <img src="/api/placeholder/40/40" alt="Python" />
        </div>
        <div class="tech-icon" style="--i:6;">
          <img src="/api/placeholder/40/40" alt="MongoDB" />
        </div>
        <div class="tech-icon" style="--i:7;">
          <img src="/api/placeholder/40/40" alt="Docker" />
        </div>
        <div class="tech-icon" style="--i:8;">
          <img src="/api/placeholder/40/40" alt="Git" />
        </div>
        <div class="tech-icon" style="--i:9;">
          <img src="/api/placeholder/40/40" alt="VS Code" />
        </div>
        <div class="tech-icon" style="--i:10;">
          <img src="/api/placeholder/40/40" alt="Figma" />
        </div>
      </div>
    </div>

    <div class="section">
      <div class="section-title">
        <div class="section-icon">🛠️</div>
        <h2>Toolkits & Frameworks</h2>
      </div>
      <div class="toolkit">
        <div class="toolkit-item">MERN Stack</div>
        <div class="toolkit-item">REST & GraphQL</div>
        <div class="toolkit-item">AI Models Integration</div>
        <div class="toolkit-item">CI/CD</div>
        <div class="toolkit-item">Clean Architecture</div>
        <div class="toolkit-item">Scalable Cloud Systems</div>
      </div>
    </div>

    <div class="section">
      <div class="section-title">
        <div class="section-icon">🌐</div>
        <h2>Connect With Me</h2>
      </div>
      <div class="social-links">
        <a href="https://linkedin.com/in/syedalim" target="_blank" class="social-btn">
          <span class="social-icon">in</span> LinkedIn
        </a>
        <a href="mailto:syedsyed3777@gmail.com" target="_blank" class="social-btn">
          <span class="social-icon">✉️</span> Gmail
        </a>
        <a href="https://github.com/syedalim1" target="_blank" class="social-btn">
          <span class="social-icon">⌨️</span> GitHub
        </a>
      </div>
    </div>
  </div>

  <script>
    // Create particles
    const particles = document.getElementById('particles');
    for (let i = 0; i < 30; i++) {
      const particle = document.createElement('div');
      particle.classList.add('particle');
      particle.style.left = `${Math.random() * 100}%`;
      particle.style.top = `${Math.random() * 100}%`;
      particle.style.animationDuration = `${15 + Math.random() * 30}s`;
      particle.style.animationDelay = `${Math.random() * 5}s`;
      particles.appendChild(particle);
    }

    // Typing effect
    const texts = [
      "Founder & CEO of CodeNovaTech",
      "AI Automation Strategist",
      "Full-Stack Developer",
      "Tech with Purpose | Impact with Code"
    ];
    let textIndex = 0;
    const typingText = document.getElementById('typing-text');
    
    function typeNextText() {
      typingText.textContent = '';
      typingText.style.width = '0';
      typingText.style.animation = 'none';
      
      setTimeout(() => {
        typingText.textContent = texts[textIndex];
        typingText.style.animation = 'typing 3s steps(40) forwards, blink-caret 0.75s step-end infinite';
        
        textIndex = (textIndex + 1) % texts.length;
        
        setTimeout(typeNextText, 4000);
      }, 500);
    }
    
    typeNextText();
  </script>
</body>
</html>
