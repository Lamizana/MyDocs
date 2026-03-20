---
hide:
  - navigation
  - footer
  - toc
---

<style>
.hero-container {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
  border-radius: 20px;
  padding: 3rem 2rem;
  margin-bottom: 2rem;
  text-align: center;
  color: white;
  box-shadow: 0 10px 40px rgba(102, 126, 234, 0.4);
}

.hero-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.5rem;
}

.hero-photo {
  width: 140px;
  height: 140px;
  border-radius: 50%;
  border: 5px solid white;
  box-shadow: 0 8px 30px rgba(0,0,0,0.3);
  object-fit: cover;
}

.hero-title {
  font-size: 2.5rem;
  font-weight: 800;
  margin: 0;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
}

.hero-subtitle {
  font-size: 1.2rem;
  opacity: 0.95;
  margin: 0;
  font-style: italic;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 0.5rem;
}

.hero-btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  border-radius: 50px;
  text-decoration: none;
  font-weight: 600;
  transition: transform 0.2s, box-shadow 0.2s;
}

.hero-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 5px 20px rgba(0,0,0,0.3);
}

.hero-btn-primary {
  background: white;
  color: #667eea;
}

.hero-btn-secondary {
  background: rgba(255,255,255,0.2);
  color: white;
  border: 2px solid white;
}
</style>

<div class="hero-container">
  <div class="hero-content">
    <img src="../images/zehd.png" alt="Alex Lamizana" class="hero-photo">
    <h1 class="hero-title">Alex Lamizana</h1>
    <p class="hero-subtitle">Le pouvoir du savoir...</p>
    <div class="hero-buttons">
      <a href="https://github.com/Lamizana" class="hero-btn hero-btn-primary" target="_blank">
        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
        GitHub
      </a>
      <a href="mailto:alex.lamizana@42angouleme.fr" class="hero-btn hero-btn-secondary">
        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        Contact
      </a>
    </div>
  </div>
</div>

<style>
.projects-section {
  margin: 2rem 0;
}

.section-title {
  font-size: 1.8rem;
  font-weight: 700;
  margin-bottom: 1.5rem;
  text-align: center;
  background: linear-gradient(90deg, #667eea, #764ba2, #f093fb);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
}

.project-card {
  background: linear-gradient(145deg, #ffffff, #f5f7fa);
  border-radius: 16px;
  padding: 1.5rem;
  text-decoration: none;
  color: inherit;
  transition: transform 0.3s, box-shadow 0.3s;
  border: 2px solid transparent;
  position: relative;
  overflow: hidden;
}

.project-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
}

[data-md-color-scheme="default"] .project-card {
  box-shadow: 0 4px 15px rgba(0,0,0,0.1);
}

[data-md-color-scheme="default"] .project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 30px rgba(102, 126, 234, 0.3);
}

[data-md-color-scheme="slate"] .project-card {
  background: linear-gradient(145deg, #1e1e2e, #2d2d44);
  box-shadow: 0 4px 15px rgba(0,0,0,0.3);
}

[data-md-color-scheme="slate"] .project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 30px rgba(102, 126, 234, 0.4);
}

.project-card.ft_transcendence::before { background: linear-gradient(90deg, #ff6b6b, #feca57); }
.project-card.minishell::before { background: linear-gradient(90deg, #48dbfb, #0abde3); }
.project-card.ft_irc::before { background: linear-gradient(90deg, #5f27cd, #341f97); }
.project-card.push_swap::before { background: linear-gradient(90deg, #00d2d3, #01a3a4); }
.project-card.so_long::before { background: linear-gradient(90deg, #ff9ff3, #f368e0); }

.project-icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.project-title {
  font-size: 1.2rem;
  font-weight: 700;
  margin: 0 0 0.5rem 0;
  color: var(--md-primary-fg-color);
}

.project-desc {
  font-size: 0.9rem;
  color: var(--md-default-fg-color--light);
  margin: 0;
  line-height: 1.5;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-top: 1rem;
}

.project-tag {
  font-size: 0.75rem;
  padding: 0.25rem 0.75rem;
  border-radius: 20px;
  background: var(--md-primary-fg-color--lightest);
  color: var(--md-primary-fg-color);
}
</style>

## :rocket: Projets

<div class="projects-section">
  <div class="projects-grid">
    
    <a href="projets/ft_transcendence/" class="project-card ft_transcendence">
      <div class="project-icon">🏓</div>
      <h3 class="project-title">ft_transcendence</h3>
      <p class="project-desc">Application web Pong multiplayer en temps réel avec matchmaking et chat intégré.</p>
      <div class="project-tags">
        <span class="project-tag">Node.js</span>
        <span class="project-tag">React</span>
        <span class="project-tag">WebSocket</span>
      </div>
    </a>
    
    <a href="projets/minishell/" class="project-card minishell">
      <div class="project-icon">💻</div>
      <h3 class="project-title">Minishell</h3>
      <p class="project-desc">Interpréteur de commandes en C simulant le comportement de bash.</p>
      <div class="project-tags">
        <span class="project-tag">C</span>
        <span class="project-tag">Unix</span>
      </div>
    </a>
    
    <a href="projets/ft_irc/" class="project-card ft_irc">
      <div class="project-icon">💬</div>
      <h3 class="project-title">ft_irc</h3>
      <p class="project-desc">Serveur IRC en C++ supportant les channels, DMs et commandes standard.</p>
      <div class="project-tags">
        <span class="project-tag">C++</span>
        <span class="project-tag">Network</span>
      </div>
    </a>
    
    <a href="projets/push_swap/" class="project-card push_swap">
      <div class="project-icon">📊</div>
      <h3 class="project-title">Push Swap</h3>
      <p class="project-desc">Algorithme de tri optimisé nécessitant un minimum d'opérations.</p>
      <div class="project-tags">
        <span class="project-tag">C</span>
        <span class="project-tag">Algorithmie</span>
      </div>
    </a>
    
    <a href="projets/so_long/" class="project-card so_long">
      <div class="project-icon">🎮</div>
      <h3 class="project-title">So Long</h3>
      <p class="project-desc">Jeu 2D en C avec graphismes MiniLibX et collecte de collectibles.</p>
      <div class="project-tags">
        <span class="project-tag">C</span>
        <span class="project-tag">Game Dev</span>
      </div>
    </a>
    
  </div>
</div>

---

<style>
.skills-section {
  margin: 2rem 0;
}

.skills-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  justify-content: center;
}

.skill-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.25rem;
  border-radius: 50px;
  font-weight: 600;
  font-size: 0.95rem;
  transition: transform 0.2s;
}

.skill-badge:hover {
  transform: scale(1.05);
}

.skill-python { background: linear-gradient(135deg, #306998, #FFD43B); color: white; }
.skill-c { background: linear-gradient(135deg, #A8B9CC, #555555); color: white; }
.skill-cpp { background: linear-gradient(135deg, #00599C, #004482); color: white; }
.skill-javascript { background: linear-gradient(135deg, #F7DF1E, #333333); color: #333; }
.skill-react { background: linear-gradient(135deg, #61DAFB, #20232A); color: white; }
.skill-git { background: linear-gradient(135deg, #F05032, #333333); color: white; }
.skill-docker { background: linear-gradient(135deg, #2496ED, #384D54); color: white; }
.skill-sql { background: linear-gradient(135deg, #4479A1, #336791); color: white; }
</style>

## :wrench: Compétences

<div class="skills-section">
  <div class="skills-grid">
    <span class="skill-badge skill-python">🐍 Python</span>
    <span class="skill-badge skill-c">🔧 C</span>
    <span class="skill-badge skill-cpp">⚡ C++</span>
    <span class="skill-badge skill-javascript">💛 JavaScript</span>
    <span class="skill-badge skill-react">⚛️ React</span>
    <span class="skill-badge skill-git">📦 Git</span>
    <span class="skill-badge skill-docker">🐳 Docker</span>
    <span class="skill-badge skill-sql">🗃️ SQL</span>
  </div>
</div>

---

<style>
.cta-section {
  background: linear-gradient(135deg, #11998e 0%, #38ef7d 100%);
  border-radius: 16px;
  padding: 2rem;
  text-align: center;
  color: white;
  margin: 2rem 0;
}

[data-md-color-scheme="slate"] .cta-section {
  background: linear-gradient(135deg, #0f4c3a 0%, #1e6f50 100%);
}

.cta-title {
  font-size: 1.5rem;
  margin: 0 0 1rem 0;
}

.cta-buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
}

.cta-btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  border-radius: 50px;
  text-decoration: none;
  font-weight: 600;
  transition: transform 0.2s;
}

.cta-btn:hover {
  transform: translateY(-2px);
}

.cta-btn-light {
  background: white;
  color: #11998e;
}

.cta-btn-outline {
  background: transparent;
  color: white;
  border: 2px solid white;
}
</style>

<div class="cta-section">
  <h2 class="cta-title">📚 Envie d'en savoir plus ?</h2>
  <div class="cta-buttons">
    <a href="about/" class="cta-btn cta-btn-light">À propos de moi</a>
    <a href="cours/" class="cta-btn cta-btn-outline">Voir les cours</a>
    <a href="blog/" class="cta-btn cta-btn-outline">Lire le blog</a>
  </div>
</div>

<style>
@media (max-width: 768px) {
  .hero-title {
    font-size: 1.8rem;
  }
  
  .hero-photo {
    width: 100px;
    height: 100px;
  }
  
  .projects-grid {
    grid-template-columns: 1fr;
  }
}
</style>
