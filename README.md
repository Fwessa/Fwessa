<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Luisa - Portfolio</title>
<style>
  * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
  }

  body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      line-height: 1.6;
      color: #333;
      background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
      min-height: 100vh;
  }

  .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 20px;
  }

  /* Hero Section */
  .hero {
      text-align: center;
      padding: 60px 20px;
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color: white;
      border-radius: 20px;
      margin-bottom: 40px;
      position: relative;
      overflow: hidden;
  }

  .hero::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
  }

  .hero h1 {
      font-size: 3.5rem;
      margin-bottom: 10px;
      font-weight: 800;
      letter-spacing: -1px;
  }

  .hero h2 {
      font-size: 1.8rem;
      margin-bottom: 5px;
      font-weight: 600;
      opacity: 0.9;
  }

  .hero h3 {
      font-size: 1.2rem;
      font-weight: 400;
      opacity: 0.8;
  }

  .social-links {
      display: flex;
      justify-content: center;
      gap: 15px;
      margin-top: 25px;
      flex-wrap: wrap;
  }

  .social-links a {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 12px 24px;
      background: rgba(255, 255, 255, 0.1);
      color: white;
      text-decoration: none;
      border-radius: 50px;
      transition: all 0.3s ease;
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.2);
  }

  .social-links a:hover {
      background: rgba(255, 255, 255, 0.2);
      transform: translateY(-3px);
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
  }

  /* About Section */
  .about-section {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 40px;
      margin-bottom: 50px;
      align-items: start;
  }

  .about-text {
      background: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
  }

  .about-text h2 {
      color: #667eea;
      margin-bottom: 20px;
      font-size: 2rem;
  }

  .stats-card {
      background: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
      text-align: center;
  }

  .stats-card img {
      max-width: 100%;
      border-radius: 10px;
  }

  /* Project Section */
  .project-section {
      margin-bottom: 50px;
  }

  .project-section h2 {
      text-align: center;
      color: #667eea;
      font-size: 2rem;
      margin-bottom: 40px;
  }

  .project-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 40px;
      align-items: start;
  }

  .project-preview {
      background: white;
      border-radius: 15px;
      overflow: hidden;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
  }

  .project-preview img {
      width: 100%;
      height: 300px;
      object-fit: cover;
  }

  .project-content {
      padding: 25px;
  }

  .project-content h3 {
      color: #667eea;
      margin-bottom: 15px;
      font-size: 1.5rem;
  }

  .tech-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin: 15px 0;
  }

  .tech-tag {
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color: white;
      padding: 5px 15px;
      border-radius: 20px;
      font-size: 0.9rem;
  }

  .project-button {
      display: inline-block;
      padding: 12px 30px;
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color: white;
      text-decoration: none;
      border-radius: 50px;
      font-weight: 600;
      transition: all 0.3s ease;
      border: none;
      cursor: pointer;
  }

  .project-button:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 20px rgba(102, 126, 234, 0.3);
  }

  /* Skills Section */
  .skills-section {
      margin-bottom: 50px;
  }

  .skills-section h2 {
      text-align: center;
      color: #667eea;
      font-size: 2rem;
      margin-bottom: 40px;
  }

  .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
  }

  .skill-category {
      background: white;
      padding: 25px;
      border-radius: 15px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
      transition: transform 0.3s ease;
  }

  .skill-category:hover {
      transform: translateY(-5px);
  }

  .skill-category h3 {
      color: #667eea;
      margin-bottom: 20px;
      text-align: center;
      font-size: 1.3rem;
  }

  .skill-item {
      display: flex;
      align-items: center;
      gap: 10px;
      margin: 12px 0;
      padding: 8px;
      border-radius: 8px;
      transition: background 0.3s ease;
  }

  .skill-item:hover {
      background: #f8f9fa;
  }

  .skill-item img {
      width: 24px;
      height: 24px;
  }

  /* Stats Section */
  .stats-section {
      margin-bottom: 50px;
  }

  .stats-section h2 {
      text-align: center;
      color: #667eea;
      font-size: 2rem;
      margin-bottom: 40px;
  }

  .stats-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 25px;
  }

  .stats-card-large {
      background: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
      text-align: center;
  }

  /* Footer */
  .footer {
      text-align: center;
      padding: 40px 20px;
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color: white;
      border-radius: 20px;
      margin-top: 50px;
  }

  .footer h3 {
      margin-bottom: 20px;
      font-size: 1.8rem;
  }

  .visitor-counter {
      display: inline-block;
      padding: 10px 20px;
      background: rgba(255, 255, 255, 0.1);
      border-radius: 50px;
      margin-top: 20px;
  }

  /* Responsive Design */
  @media (max-width: 768px) {
      .hero h1 {
          font-size: 2.5rem;
      }
      
      .about-section,
      .project-grid {
          grid-template-columns: 1fr;
      }
      
      .social-links {
          flex-direction: column;
          align-items: center;
      }
      
      .social-links a {
          width: 100%;
          max-width: 300px;
          justify-content: center;
      }
  }

  /* Animation */
  @keyframes fadeIn {
      from {
          opacity: 0;
          transform: translateY(20px);
      }
      to {
          opacity: 1;
          transform: translateY(0);
      }
  }

  .fade-in {
      animation: fadeIn 0.6s ease-out;
  }

  /* Typing Effect */
  .typing-container {
      margin: 20px 0;
      min-height: 60px;
  }

  .typing-text {
      font-size: 1.2rem;
      font-weight: 300;
      opacity: 0.9;
      border-right: 2px solid rgba(255, 255, 255, 0.7);
      padding-right: 5px;
      animation: blink 1s infinite;
  }

  @keyframes blink {
      0%, 100% { border-color: transparent; }
      50% { border-color: rgba(255, 255, 255, 0.7); }
  }
</style>
</head>
<body>
    <div class="container">
        <!-- Hero Section -->
        <section class="hero fade-in">
            <h1>👋 Hi, I'm Luisa</h1>
            <h2>🎓 BSIT Student • 🖥️ Full-Stack Developer • 🎨 Multimedia Artist</h2>
            <h3>📍 Philippines</h3>
            
<div class="typing-container">
  <div class="typing-text" id="typing-text"></div>
</div>

<div class="social-links">
  <a href="https://linkedin.com/in/www.linkedin.com/in/luisa-dala-b53341132" target="_blank">
      <span>LinkedIn</span>
  </a>
  <a href="https://github.com/Fwessa" target="_blank">
      <span>GitHub</span>
  </a>
  <a href="#" target="_blank">
      <span>Portfolio</span>
  </a>
  <a href="mailto:your-email@example.com">
      <span>Email</span>
  </a>
</div>
</section>

<!-- About Section -->
<section class="about-section fade-in">
<div class="about-text">
  <h2>🌟 About Me</h2>
  <p>I'm a BSIT student specializing in <strong>Multimedia Arts and Animation</strong> with a passion for <strong>full-stack web development</strong>. I build practical applications using Vue 3 and Django REST Framework, focusing on clean UI, RESTful APIs, and JWT authentication.</p>
  <p>I love creating visually appealing and functional applications that solve real-world problems, blending my technical skills with artistic creativity.</p>
  
  <div style="margin-top: 20px;">
      <p><strong>🎯 Currently Learning:</strong></p>
      <ul>
          <li>Advanced Vue 3 Composition API</li>
          <li>Django REST Framework optimization</li>
          <li>Docker containerization</li>
          <li>Real-time applications with WebSockets</li>
          <li>UI/UX design principles</li>
      </ul>
  </div>
</div>

<div class="stats-card">
  <h3>GitHub Stats</h3>
  <img src="https://github-readme-stats.vercel.app/api?username=Fwessa&show_icons=true&theme=radical&hide_border=true" alt="GitHub Stats">
</div>
</section>

<!-- Project Section -->
<section class="project-section fade-in">
<h2>🚀 Featured Project</h2>
<div class="project-grid">
  <div class="project-preview">
      <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExZTR6eXZ6enU1bXN2NDBqd3E5anA0cXExdTlyZDNxOW1hOTU1ZDM1MSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/xT9IgzoKnwFNmISR8I/giphy.gif" alt="Kanban Board Demo">
  </div>
  
  <div class="project-content">
      <h3>🗂️ Kanban Task Board</h3>
      <p>A drag-and-drop task management system built with Vue 3 + Django REST Framework. Includes JWT authentication, responsive UI, and smooth UX for organizing tasks.</p>
      
      <p><strong>Highlights:</strong></p>
      <ul>
          <li>Drag & drop Kanban columns</li>
          <li>JWT login + protected routes</li>
          <li>RESTful API integration</li>
          <li>Clean, responsive layout</li>
      </ul>
      
      <div class="tech-tags">
          <span class="tech-tag">Vue 3</span>
          <span class="tech-tag">Django</span>
          <span class="tech-tag">PostgreSQL</span>
          <span class="tech-tag">JWT Auth</span>
          <span class="tech-tag">PrimeVue</span>
      </div>
      
      <a href="https://github.com/Fwessa/DjangoREST-API-Vue_KabanDraggable_TaskBoard" target="_blank" class="project-button">
          View Project on GitHub
      </a>
  </div>
</div>
</section>

<!-- Skills Section -->
<section class="skills-section fade-in">
<h2>💻 Tech Stack</h2>
<div class="skills-grid">
  <div class="skill-category">
      <h3>🎨 Frontend</h3>
      <div class="skill-item">Vue.js</div>
      <div class="skill-item">React</div>
      <div class="skill-item">JavaScript</div>
      <div class="skill-item">HTML5/CSS3</div>
      <div class="skill-item">Bootstrap</div>
      <div class="skill-item">SASS</div>
  </div>
  
  <div class="skill-category">
      <h3>⚙️ Backend</h3>
      <div class="skill-item">Django & DRF</div>
      <div class="skill-item">Python</div>
      <div class="skill-item">Node.js</div>
      <div class="skill-item">Express.js</div>
      <div class="skill-item">REST APIs</div>
      <div class="skill-item">JWT Auth</div>
  </div>
  
  <div class="skill-category">
      <h3>🗄️ Databases</h3>
      <div class="skill-item">PostgreSQL</div>
      <div class="skill-item">MySQL</div>
      <div class="skill-item">MongoDB</div>
  </div>
  
  <div class="skill-category">
      <h3>🎨 Design Tools</h3>
      <div class="skill-item">Figma</div>
      <div class="skill-item">Adobe Illustrator</div>
      <div class="skill-item">Adobe Photoshop</div>
      <div class="skill-item">Blender</div>
      <div class="skill-item">Unity</div>
  </div>
</div>
</section>

<!-- Stats Section -->
<section class="stats-section fade-in">
<h2>📊 GitHub Activity</h2>
<div class="stats-grid">
  <div class="stats-card-large">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Fwessa&layout=compact&theme=radical&hide_border=true" alt="Top Languages">
  </div>
  <div class="stats-card-large">
      <img src="https://streak-stats.demolab.com?user=Fwessa&theme=radical&hide_border=true" alt="GitHub Streak">
  </div>
</div>
</section>

<!-- Fun Facts -->
<section class="about-text fade-in">
<h2>💡 Fun Facts</h2>
<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; margin-top: 20px;">
  <div style="text-align: center; padding: 20px; background: #f8f9fa; border-radius: 10px;">
      <div style="font-size: 2rem; margin-bottom: 10px;">🎨</div>
      <p>Can create digital illustrations and 3D models</p>
  </div>
  <div style="text-align: center; padding: 20px; background: #f8f9fa; border-radius: 10px;">
      <div style="font-size: 2rem; margin-bottom: 10px;">🌱</div>
      <p>Passionate about clean code and user experience</p>
  </div>
  <div style="text-align: center; padding: 20px; background: #f8f9fa; border-radius: 10px;">
      <div style="font-size: 2rem; margin-bottom: 10px;">🎯</div>
      <p>Love solving complex problems with elegant solutions</p>
  </div>
  <div style="text-align: center; padding: 20px; background: #f8f9fa; border-radius: 10px;">
      <div style="font-size: 2rem; margin-bottom: 10px;">☕</div>
      <p>Coffee fuels my coding sessions</p>
  </div>
</div>
</section>

<!-- Footer -->
<footer class="footer fade-in">
<h3>✨ "Code is poetry, design is art, and applications are experiences."</h3>
<div class="visitor-counter">
  <span>👁️ Views: <span id="view-count">1,234</span></span>
</div>
<p style="margin-top: 20px; opacity: 0.8;">© 2024 Luisa • BSIT Student & Developer</p>
</footer>
</div>

<script>
// Typing effect
const texts = [
"Vue 3 + Django REST Framework Developer",
"Clean UI | RESTful APIs | JWT Auth",
"Multimedia Arts & Animation | UI/UX Design",
"Hands-on Projects | Always Learning"
];
let textIndex = 0;
let charIndex = 0;
const typingText = document.getElementById('typing-text');

function typeText() {
if (charIndex < texts[textIndex].length) {
  typingText.textContent += texts[textIndex].charAt(charIndex);
  charIndex++;
  setTimeout(typeText, 50);
} else {
  setTimeout(eraseText, 2000);
}
}

function eraseText() {
if (charIndex > 0) {
  typingText.textContent = texts[textIndex].substring(0, charIndex - 1);
  charIndex--;
  setTimeout(eraseText, 30);
} else {
  textIndex = (textIndex + 1) % texts.length;
  setTimeout(typeText, 500);
}
}

// Start typing effect
setTimeout(typeText, 1000);

// Animate elements on scroll
const observerOptions = {
threshold: 0.1,
rootMargin: '0px 0px -50px 0px'
};

const observer = new IntersectionObserver((entries) => {
entries.forEach(entry => {
  if (entry.isIntersecting) {
      entry.target.style.opacity = '1';
      entry.target.style.transform = 'translateY(0)';
  }
});
}, observerOptions);

// Observe all fade-in elements
document.querySelectorAll('.fade-in').forEach(el => {
el.style.opacity = '0';
el.style.transform = 'translateY(20px)';
el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
observer.observe(el);
});

// Simple view counter (local storage based)
let views = localStorage.getItem('portfolioViews') || 1234;
views = parseInt(views) + 1;
localStorage.setItem('portfolioViews', views);
document.getElementById('view-count').textContent = views.toLocaleString();
</script>
</body>
</html>
