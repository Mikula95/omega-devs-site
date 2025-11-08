<template>
  <header class="header">
    <div class="container">
      <div class="nav-wrapper">
        <div class="logo">
          <h2><span class="text-blue">Omega</span>-Devs</h2>
        </div>
        <nav class="nav">
          <a href="#home" class="nav-link">Home</a>
          <a href="#about" class="nav-link">About</a>
          <a href="#services" class="nav-link">Services</a>
          <a href="#projects" class="nav-link">Projects</a>
          <a href="#contact" class="nav-link">Contact</a>
        </nav>
        <div class="mobile-menu-toggle" @click="toggleMenu">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const mobileMenuOpen = ref(false)

const toggleMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}
</script>

<style scoped>
.header {
  background-color: rgba(0, 0, 0, 0.95);
  backdrop-filter: blur(10px);
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  border-bottom: 1px solid #222;
}

.nav-wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 0;
}

.logo h2 {
  font-size: 1.8rem;
  font-weight: 700;
}

.nav {
  display: flex;
  gap: 2rem;
}

.nav-link {
  color: #fff;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
  position: relative;
}

.nav-link:hover {
  color: #4A9EFF;
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background: linear-gradient(135deg, #4A9EFF, #0066CC);
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}

.mobile-menu-toggle {
  display: none;
  flex-direction: column;
  cursor: pointer;
  gap: 4px;
}

.mobile-menu-toggle span {
  width: 25px;
  height: 3px;
  background-color: #fff;
  transition: all 0.3s ease;
}

@media (max-width: 768px) {
  .nav {
    display: none;
  }
  
  .mobile-menu-toggle {
    display: flex;
  }
}
</style>