<template>
  <section id="about" class="section bg-dark">
    <div class="container">
      <h2 class="section-title">About Omega-Devs</h2>
      <div class="about-content">
        <div class="about-text">
          <h3>Who We Are</h3>
          <p>
            Omega-Devs is a dynamic software development company specializing in creating 
            innovative solutions for businesses of all sizes. Our team combines technical expertise 
            with creative problem-solving to deliver high-quality software that meets your unique needs.
          </p>
          <p>
            With experience across multiple technologies and industries, we pride ourselves on 
            staying at the forefront of technology trends while maintaining a focus on practical, 
            scalable solutions.
          </p>
          
          <h3>Our Expertise</h3>
          <div class="skills-grid">
            <div class="skill-category">
              <h4>Backend Development</h4>
              <ul>
                <li>Python (Django, Flask)</li>
                <li>Java (Spring)</li>
                <li>Go/Golang</li>
                <li>PHP (Laravel)</li>
              </ul>
            </div>
            <div class="skill-category">
              <h4>Frontend Development</h4>
              <ul>
                <li>Vue.js / React.js</li>
                <li>JavaScript (ES6+)</li>
                <li>HTML5 / CSS3</li>
                <li>React Native</li>
              </ul>
            </div>
            <div class="skill-category">
              <h4>Databases & Tools</h4>
              <ul>
                <li>PostgreSQL, MySQL</li>
                <li>MongoDB</li>
                <li>Docker</li>
                <li>AWS Cloud Services</li>
              </ul>
            </div>
            <div class="skill-category">
              <h4>Specialized</h4>
              <ul>
                <li>Android Development</li>
                <li>3D Development (Blender)</li>
                <li>Machine Learning</li>
                <li>Bioinformatics</li>
              </ul>
            </div>
          </div>
        </div>
        
        <div class="about-stats">
          <div class="stat-card">
            <div class="stat-number">5+</div>
            <div class="stat-label">Years Experience</div>
          </div>
          <div class="stat-card">
            <div class="stat-number">20+</div>
            <div class="stat-label">Projects Completed</div>
          </div>
          <div class="stat-card">
            <div class="stat-number">15+</div>
            <div class="stat-label">Technologies</div>
          </div>
          <div class="stat-card">
            <div class="stat-number">100%</div>
            <div class="stat-label">Client Satisfaction</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-content {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 4rem;
  align-items: start;
}

.about-text h3 {
  color: #4A9EFF;
  font-size: 1.5rem;
  margin-bottom: 1rem;
  margin-top: 2rem;
}

.about-text h3:first-child {
  margin-top: 0;
}

.about-text p {
  color: #ccc;
  margin-bottom: 1.5rem;
  line-height: 1.8;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2rem;
  margin-top: 2rem;
}

.skill-category h4 {
  color: #4A9EFF;
  font-size: 1.1rem;
  margin-bottom: 0.5rem;
  border-bottom: 1px solid #333;
  padding-bottom: 0.5rem;
}

.skill-category ul {
  list-style: none;
}

.skill-category li {
  color: #ccc;
  padding: 0.3rem 0;
  position: relative;
  padding-left: 1rem;
}

.skill-category li::before {
  content: '▶';
  color: #4A9EFF;
  position: absolute;
  left: 0;
  font-size: 0.8rem;
}

.about-stats {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
}

.stat-card {
  background: linear-gradient(135deg, #111, #222);
  padding: 2rem 1.5rem;
  border-radius: 10px;
  text-align: center;
  border: 1px solid #333;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.stat-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(74, 158, 255, 0.2);
}

.stat-number {
  font-size: 2.5rem;
  font-weight: 700;
  color: #4A9EFF;
  margin-bottom: 0.5rem;
}

.stat-label {
  color: #ccc;
  font-size: 0.9rem;
}

@media (max-width: 968px) {
  .about-content {
    grid-template-columns: 1fr;
    gap: 3rem;
  }
  
  .skills-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 768px) {
  .about-stats {
    grid-template-columns: 1fr;
  }
}
</style>