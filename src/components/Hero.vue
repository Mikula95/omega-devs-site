<template>
  <section id="home" class="hero">
    <div class="container">
      <div class="hero-content">
        <h1 class="hero-title">
          <span class="text-blue">Omega-Devs</span><br>
          Software Development Solutions
        </h1>
        <p class="hero-subtitle">
          We create innovative software solutions that drive your business forward. 
          Specializing in web applications, mobile development, and custom software.
        </p>
        <div class="hero-buttons">
          <a href="#projects" class="btn">View Our Work</a>
          <a href="#contact" class="btn btn-outline">Get In Touch</a>
        </div>
      </div>
      <div class="hero-visual">
        <div class="code-block">
          <div class="code-header">
            <div class="code-dots">
              <span></span>
              <span></span>
              <span></span>
            </div>
            <div class="code-title">main.py</div>
          </div>
          <div class="code-content">
            <div class="code-line"><span class="keyword">def</span> <span class="function">create_solution</span>():</div>
            <div class="code-line">&nbsp;&nbsp;&nbsp;&nbsp;<span class="keyword">return</span> <span class="string">"innovative_software"</span></div>
            <div class="code-line"></div>
            <div class="code-line"><span class="comment"># Omega-Devs</span></div>
            <div class="code-line"><span class="variable">result</span> = <span class="function">create_solution</span>()</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  background: linear-gradient(135deg, #000 0%, #111 100%);
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 20% 50%, rgba(74, 158, 255, 0.1) 0%, transparent 50%),
    radial-gradient(circle at 80% 20%, rgba(74, 158, 255, 0.05) 0%, transparent 50%);
}

.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
  position: relative;
  z-index: 1;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 700;
  line-height: 1.2;
  margin-bottom: 1.5rem;
}

.hero-subtitle {
  font-size: 1.2rem;
  color: #ccc;
  margin-bottom: 2.5rem;
  line-height: 1.6;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.btn-outline {
  background: transparent;
  border: 2px solid #4A9EFF;
  color: #4A9EFF;
}

.btn-outline:hover {
  background: #4A9EFF;
  color: white;
}

.code-block {
  background: #111;
  border-radius: 10px;
  border: 1px solid #333;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
}

.code-header {
  background: #1e1e1e;
  padding: 10px 15px;
  display: flex;
  align-items: center;
  gap: 10px;
  border-bottom: 1px solid #333;
}

.code-dots {
  display: flex;
  gap: 6px;
}

.code-dots span {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: #666;
}

.code-dots span:first-child {
  background: #ff5f57;
}

.code-dots span:nth-child(2) {
  background: #ffbd2e;
}

.code-dots span:nth-child(3) {
  background: #28ca42;
}

.code-title {
  color: #ccc;
  font-size: 0.9rem;
}

.code-content {
  padding: 20px;
  font-family: 'Courier New', monospace;
  font-size: 0.9rem;
  line-height: 1.5;
}

.code-line {
  margin-bottom: 5px;
}

.keyword {
  color: #4A9EFF;
}

.function {
  color: #50c878;
}

.string {
  color: #ffd700;
}

.comment {
  color: #666;
}

.variable {
  color: #ff6b6b;
}

@media (max-width: 768px) {
  .container {
    grid-template-columns: 1fr;
    gap: 2rem;
    text-align: center;
  }
  
  .hero-title {
    font-size: 2.5rem;
  }
  
  .hero-buttons {
    justify-content: center;
  }
}
</style>