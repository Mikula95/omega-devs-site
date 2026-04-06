<template>
  <div class="clients-section bg-dark">
    <div class="clients-header">
      <p>TRUSTED BY</p>
    </div>
    <div class="marquee-wrapper">
      <div class="marquee" aria-hidden="true">
        <span v-for="(client, index) in clients" :key="'first-' + index" class="client-item">
          <a :href="client.url" target="_blank" rel="noopener noreferrer" class="client-link">
            {{ client.name }}
          </a>
          <span class="separator">•</span>
        </span>
      </div>
      <div class="marquee" aria-hidden="true">
        <span v-for="(client, index) in clients" :key="'second-' + index" class="client-item">
          <a :href="client.url" target="_blank" rel="noopener noreferrer" class="client-link">
            {{ client.name }}
          </a>
          <span class="separator">•</span>
        </span>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const clients = ref([
  { name: 'Brrm', url: 'http://brrm.eu/' },
  { name: 'ZenDev', url: 'https://www.zendev.se/' },
  { name: 'Metisox', url: 'https://www.metisox.com/' },
  { name: 'xrhuman', url: 'https://xrhuman.eu/' },
  { name: 'Grammarus', url: 'https://grammarsaurus.co.uk/' },
  { name: 'Nine alfa ltd', url: 'https://www.ninealfa.co.uk/' },
  { name: 'ccnet', url: 'https://www.ccnet.de/' },
  { name: 'Png systems', url: 'https://png.systems/' },
  { name: 'aiandit', url: 'https://aiandit.com/' },
  { name: '3Dmarch', url: 'https://3dmarch.org/' },
  
]);
</script>

<style scoped>
.clients-section {
  padding: 15px 0 10px 0;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
  overflow: hidden;
  position: relative;
  display: flex;
  flex-direction: column;
}

.clients-header {
  text-align: center;
  margin-bottom: 10px;
  z-index: 3;
}

.clients-header p {
  color: #555;
  font-size: 0.85rem;
  letter-spacing: 4px;
  text-transform: uppercase;
  font-weight: 600;
  margin: 0;
}

.marquee-wrapper {
  display: flex;
  overflow: hidden;
  user-select: none;
  width: 100%;
  position: relative;
}

.marquee-wrapper::before,
.marquee-wrapper::after {
  content: '';
  position: absolute;
  top: 0;
  bottom: 0;
  width: 15vw;
  z-index: 2;
  pointer-events: none;
}

.marquee-wrapper::before {
  left: 0;
  background: linear-gradient(to right, #111 0%, transparent 100%);
}

.marquee-wrapper::after {
  right: 0;
  background: linear-gradient(to left, #111 0%, transparent 100%);
}

.marquee {
  display: flex;
  flex-shrink: 0;
  align-items: center;
  justify-content: space-around;
  min-width: 100%;
  animation: scroll 40s linear infinite;
}

.marquee-wrapper:hover .marquee {
  animation-play-state: paused;
}

.client-item {
  display: flex;
  align-items: center;
  padding: 0 25px;
}

.client-link {
  color: #666;
  text-decoration: none;
  font-size: 1.05rem;
  font-weight: 700;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  text-transform: uppercase;
  letter-spacing: 1px;
  transition: all 0.3s ease;
  position: relative;
}

.client-link::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -4px;
  left: 0;
  background-color: #4A9EFF;
  transition: width 0.3s ease;
}

.client-link:hover {
  color: #fff;
  text-shadow: 0 0 15px rgba(74, 158, 255, 0.4);
}

.client-link:hover::after {
  width: 100%;
}

.separator {
  color: #333;
  margin-left: 50px;
  font-size: 1.2rem;
}

@keyframes scroll {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-100%);
  }
}

@media (max-width: 768px) {
  .client-link {
    font-size: 0.9rem;
    letter-spacing: 1px;
  }
  .client-item {
    padding: 0 15px;
  }
  .separator {
    margin-left: 30px;
  }
  .clients-section::before,
  .clients-section::after {
    width: 30px;
  }
}
</style>
