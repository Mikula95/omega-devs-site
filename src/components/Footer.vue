<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-section">
          <div class="footer-logo">
            <h3><span class="text-blue">Omega</span>-Devs SP</h3>
            <p>Innovative software solutions for modern businesses.</p>
          </div>
          <div class="social-links">
            <a href="#" class="social-link" title="LinkedIn">💼</a>
            <a href="#" class="social-link" title="GitHub">👨‍💻</a>
            <a href="#" class="social-link" title="Email">📧</a>
          </div>
        </div>
        
        <div class="footer-section">
          <h4>Services</h4>
          <ul class="footer-links">
            <li><a href="#services">Web Development</a></li>
            <li><a href="#services">Mobile Apps</a></li>
            <li><a href="#services">Custom Software</a></li>
            <li><a href="#services">AI & ML</a></li>
            <li><a href="#services">Cloud Solutions</a></li>
          </ul>
        </div>
        
        <div class="footer-section">
          <h4>Technologies</h4>
          <ul class="footer-links">
            <li><a href="#">Python & Django</a></li>
            <li><a href="#">Vue.js & React</a></li>
            <li><a href="#">Java & Android</a></li>
            <li><a href="#">Go & PHP</a></li>
            <li><a href="#">AWS & Docker</a></li>
          </ul>
        </div>
        
        <div class="footer-section">
          <h4>Contact Info</h4>
          <div class="contact-info">
            <p>📍 Banja Luka, Bosnia and Herzegovina</p>
            <p>📧 contact@omega-devs.com</p>
            <p>📱 +387 XX XXX XXX</p>
            <p>🕒 Mon-Fri: 9:00 AM - 6:00 PM</p>
          </div>
        </div>
      </div>
      
      <div class="footer-bottom">
        <div class="footer-divider"></div>
        <div class="footer-bottom-content">
          <p>&copy; {{ currentYear }} Omega-Devs. All rights reserved.</p>
          <div class="footer-bottom-links">
            <a href="#">Privacy Policy</a>
            <a href="#">Terms of Service</a>
            <a href="#">Cookie Policy</a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { computed } from 'vue'

const currentYear = computed(() => new Date().getFullYear())
</script>

<style scoped>
.footer {
  background: linear-gradient(135deg, #000, #111);
  padding: 3rem 0 1rem;
  border-top: 1px solid #333;
}

.footer-content {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr 1.5fr;
  gap: 3rem;
  margin-bottom: 2rem;
}

.footer-section h3 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
  font-weight: 700;
}

.footer-section h4 {
  color: #4A9EFF;
  font-size: 1.1rem;
  margin-bottom: 1rem;
  font-weight: 600;
}

.footer-logo p {
  color: #ccc;
  margin-bottom: 1.5rem;
  line-height: 1.6;
}

.social-links {
  display: flex;
  gap: 1rem;
}

.social-link {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  background: rgba(74, 158, 255, 0.1);
  border: 1px solid rgba(74, 158, 255, 0.3);
  border-radius: 50%;
  color: #4A9EFF;
  text-decoration: none;
  font-size: 1.2rem;
  transition: all 0.3s ease;
}

.social-link:hover {
  background: rgba(74, 158, 255, 0.2);
  border-color: #4A9EFF;
  transform: translateY(-2px);
}

.footer-links {
  list-style: none;
}

.footer-links li {
  margin-bottom: 0.5rem;
}

.footer-links a {
  color: #ccc;
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-links a:hover {
  color: #4A9EFF;
}

.contact-info p {
  color: #ccc;
  margin-bottom: 0.5rem;
  font-size: 0.9rem;
}

.footer-divider {
  height: 1px;
  background: linear-gradient(90deg, transparent, #333, transparent);
  margin: 2rem 0;
}

.footer-bottom-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 1rem;
}

.footer-bottom-content p {
  color: #888;
  font-size: 0.9rem;
}

.footer-bottom-links {
  display: flex;
  gap: 2rem;
}

.footer-bottom-links a {
  color: #888;
  text-decoration: none;
  font-size: 0.9rem;
  transition: color 0.3s ease;
}

.footer-bottom-links a:hover {
  color: #4A9EFF;
}

@media (max-width: 968px) {
  .footer-content {
    grid-template-columns: repeat(2, 1fr);
    gap: 2rem;
  }
}

@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: 1fr;
    text-align: center;
  }
  
  .footer-bottom-content {
    flex-direction: column;
    text-align: center;
  }
  
  .footer-bottom-links {
    justify-content: center;
  }
}
</style>