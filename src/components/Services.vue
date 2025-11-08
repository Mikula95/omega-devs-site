<template>
  <section id="services" class="section bg-darker">
    <div class="container">
      <h2 class="section-title">Our Services</h2>
      <div class="services-grid">
        <div class="service-card">
          <div class="service-icon">🌐</div>
          <h3>Web Development</h3>
          <p>
            Full-stack web applications using modern frameworks like Vue.js, React.js, 
            Django, and Laravel. Responsive, fast, and user-friendly solutions.
          </p>
          <ul class="service-features">
            <li>Custom Web Applications</li>
            <li>E-commerce Platforms</li>
            <li>REST API Development</li>
            <li>Progressive Web Apps</li>
          </ul>
        </div>

        <div class="service-card">
          <div class="service-icon">📱</div>
          <h3>Mobile Development</h3>
          <p>
            Native Android applications and cross-platform mobile solutions 
            that provide excellent user experience across all devices.
          </p>
          <ul class="service-features">
            <li>Android Native Apps</li>
            <li>React Native Apps</li>
            <li>Mobile UI/UX Design</li>
            <li>App Store Deployment</li>
          </ul>
        </div>

        <div class="service-card">
          <div class="service-icon">🛠️</div>
          <h3>Custom Software</h3>
          <p>
            Tailored software solutions designed specifically for your business needs, 
            from CRM systems to specialized industry applications.
          </p>
          <ul class="service-features">
            <li>Business Applications</li>
            <li>CRM Systems</li>
            <li>Data Management Tools</li>
            <li>Automation Solutions</li>
          </ul>
        </div>

        <div class="service-card">
          <div class="service-icon">🤖</div>
          <h3>AI & Machine Learning</h3>
          <p>
            Leverage the power of artificial intelligence and machine learning 
            to automate processes and gain insights from your data.
          </p>
          <ul class="service-features">
            <li>Data Analysis Tools</li>
            <li>Predictive Models</li>
            <li>Process Automation</li>
            <li>Bioinformatics Solutions</li>
          </ul>
        </div>

        <div class="service-card">
          <div class="service-icon">☁️</div>
          <h3>Cloud Solutions</h3>
          <p>
            Scalable cloud infrastructure and deployment solutions using AWS 
            and modern DevOps practices for reliable applications.
          </p>
          <ul class="service-features">
            <li>AWS Cloud Deployment</li>
            <li>Docker Containerization</li>
            <li>CI/CD Pipelines</li>
            <li>Database Management</li>
          </ul>
        </div>

        <div class="service-card">
          <div class="service-icon">🎯</div>
          <h3>Consulting & Support</h3>
          <p>
            Technical consulting, code reviews, and ongoing support to help 
            you make the right technology decisions for your business.
          </p>
          <ul class="service-features">
            <li>Technology Consulting</li>
            <li>Code Review & Optimization</li>
            <li>Technical Training</li>
            <li>Ongoing Maintenance</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.service-card {
  background: linear-gradient(135deg, #111, #1a1a1a);
  padding: 2.5rem 2rem;
  border-radius: 15px;
  border: 1px solid #333;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.service-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(135deg, #4A9EFF, #0066CC);
  transform: scaleX(0);
  transition: transform 0.3s ease;
}

.service-card:hover::before {
  transform: scaleX(1);
}

.service-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(74, 158, 255, 0.2);
  border-color: #4A9EFF;
}

.service-icon {
  font-size: 3rem;
  margin-bottom: 1.5rem;
  display: block;
}

.service-card h3 {
  color: #4A9EFF;
  font-size: 1.5rem;
  margin-bottom: 1rem;
  font-weight: 600;
}

.service-card p {
  color: #ccc;
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.service-features {
  list-style: none;
}

.service-features li {
  color: #aaa;
  padding: 0.5rem 0;
  position: relative;
  padding-left: 1.5rem;
  transition: color 0.3s ease;
}

.service-features li::before {
  content: '✓';
  color: #4A9EFF;
  position: absolute;
  left: 0;
  font-weight: bold;
}

.service-card:hover .service-features li {
  color: #ddd;
}

@media (max-width: 768px) {
  .services-grid {
    grid-template-columns: 1fr;
  }
  
  .service-card {
    padding: 2rem 1.5rem;
  }
}
</style>