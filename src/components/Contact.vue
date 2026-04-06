<template>
  <section id="contact" class="section bg-darker">
    <div class="container">
      <h2 class="section-title">Get In Touch</h2>
      <div class="contact-content">
        <div class="contact-info">
          <h3>Let's Build Something Amazing Together</h3>
          <p>
            Ready to turn your ideas into reality? We're here to help you create 
            innovative software solutions that drive your business forward.
          </p>
          
          <div class="contact-methods">
            <div class="contact-method">
              <div class="contact-icon">📧</div>
              <div class="contact-details">
                <h4>Email</h4>
                <p>info@omegadevs.tech</p>
              </div>
            </div>
            
            <div class="contact-method">
              <div class="contact-icon">📱</div>
              <div class="contact-details">
                <h4>Phone</h4>
                <p>+387 65 389 414</p>
              </div>
            </div>
            
            <div class="contact-method">
              <div class="contact-icon">📍</div>
              <div class="contact-details">
                <h4>Location</h4>
                <p>Banja Luka, Bosnia and Herzegovina</p>
              </div>
            </div>
          </div>
          
          <div class="business-hours">
            <h4>Business Hours</h4>
            <div class="hours-grid">
              <div>Monday - Friday:</div>
              <div>8:00 AM - 8:00 PM</div>
              <div>Weekend:</div>
              <div>Available for urgent projects</div>
            </div>
          </div>
        </div>
<!--         
        <div class="contact-form">
          <form @submit.prevent="handleSubmit">
            <div class="form-group">
              <label for="name">Name *</label>
              <input 
                type="text" 
                id="name" 
                v-model="form.name" 
                required 
                placeholder="Your Name"
              />
            </div>
            
            <div class="form-group">
              <label for="email">Email *</label>
              <input 
                type="email" 
                id="email" 
                v-model="form.email" 
                required 
                placeholder="your@email.com"
              />
            </div>
            
            <div class="form-group">
              <label for="company">Company</label>
              <input 
                type="text" 
                id="company" 
                v-model="form.company" 
                placeholder="Your Company"
              />
            </div>
            
            <div class="form-group">
              <label for="project">Project Type</label>
              <select id="project" v-model="form.projectType">
                <option value="">Select Project Type</option>
                <option value="web">Web Development</option>
                <option value="mobile">Mobile App</option>
                <option value="custom">Custom Software</option>
                <option value="ai">AI/ML Solution</option>
                <option value="cloud">Cloud Migration</option>
                <option value="consulting">Consulting</option>
                <option value="other">Other</option>
              </select>
            </div>
            
            <div class="form-group">
              <label for="budget">Budget Range</label>
              <select id="budget" v-model="form.budget">
                <option value="">Select Budget Range</option>
                <option value="small">€1,000 - €5,000</option>
                <option value="medium">€5,000 - €15,000</option>
                <option value="large">€15,000 - €50,000</option>
                <option value="enterprise">€50,000+</option>
                <option value="discuss">Let's Discuss</option>
              </select>
            </div>
            
            <div class="form-group">
              <label for="message">Message *</label>
              <textarea 
                id="message" 
                v-model="form.message" 
                required 
                rows="5" 
                placeholder="Tell us about your project..."
              ></textarea>
            </div>
            
            <button type="submit" class="btn btn-full">
              Send Message
            </button>
          </form>
        </div> -->
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const form = ref({
  name: '',
  email: '',
  company: '',
  projectType: '',
  budget: '',
  message: ''
})

const handleSubmit = () => {
  // Here you would typically send the form data to a server
  alert('Thank you for your message! We will get back to you soon.')
  
  // Reset form
  form.value = {
    name: '',
    email: '',
    company: '',
    projectType: '',
    budget: '',
    message: ''
  }
}
</script>

<style scoped>
.contact-content {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 500px;
  gap: 4rem;
  margin-top: 2rem;
}

.contact-info h3 {
  color: #4A9EFF;
  font-size: 1.8rem;
  margin-bottom: 1rem;
}

.contact-info p {
  color: #ccc;
  line-height: 1.6;
  margin-bottom: 2rem;
}

.contact-methods {
  margin-bottom: 3rem;
}

.contact-method {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1.5rem;
  padding: 1rem;
  background: rgba(74, 158, 255, 0.05);
  border-radius: 10px;
  border: 1px solid rgba(74, 158, 255, 0.1);
}

.contact-icon {
  font-size: 1.5rem;
  width: 50px;
  text-align: center;
}

.contact-details h4 {
  color: #4A9EFF;
  margin-bottom: 0.3rem;
}

.contact-details p {
  color: #ccc;
  margin: 0;
}

.business-hours h4 {
  color: #4A9EFF;
  margin-bottom: 1rem;
}

.hours-grid {
  display: grid;
  grid-template-columns: auto auto;
  gap: 0.5rem 2rem;
  color: #ccc;
}

.contact-form {
  background: linear-gradient(135deg, #111, #1a1a1a);
  padding: 2.5rem;
  border-radius: 15px;
  border: 1px solid #333;
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group label {
  display: block;
  color: #4A9EFF;
  margin-bottom: 0.5rem;
  font-weight: 500;
}

.form-group input,
.form-group select,
.form-group textarea {
  width: 100%;
  padding: 0.8rem 1rem;
  background: #222;
  border: 1px solid #444;
  border-radius: 5px;
  color: #fff;
  font-size: 1rem;
  transition: all 0.3s ease;
}

.form-group input:focus,
.form-group select:focus,
.form-group textarea:focus {
  outline: none;
  border-color: #4A9EFF;
  box-shadow: 0 0 0 2px rgba(74, 158, 255, 0.2);
}

.form-group input::placeholder,
.form-group textarea::placeholder {
  color: #888;
}

.btn-full {
  width: 100%;
  padding: 1rem;
  font-size: 1.1rem;
  margin-top: 1rem;
}

@media (max-width: 968px) {
  .contact-content {
    grid-template-columns: 1fr;
    gap: 3rem;
  }
}

@media (max-width: 768px) {
  .contact-form {
    padding: 2rem 1.5rem;
  }
  
  .hours-grid {
    grid-template-columns: 1fr;
    gap: 0.3rem;
  }
}
</style>