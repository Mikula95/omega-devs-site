<template>

</template>

<style scoped>
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.project-card {
  background: linear-gradient(135deg, #111, #1a1a1a);
  padding: 2rem;
  border-radius: 15px;
  border: 1px solid #333;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.project-card::before {
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

.project-card:hover::before {
  transform: scaleX(1);
}

.project-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 15px 35px rgba(74, 158, 255, 0.25);
  border-color: #4A9EFF;
}

.project-header h3 {
  color: #4A9EFF;
  font-size: 1.4rem;
  margin-bottom: 0.5rem;
  font-weight: 600;
}

.project-tech {
  color: #888;
  font-size: 0.9rem;
  margin-bottom: 1rem;
  font-family: 'Courier New', monospace;
}

.project-description {
  color: #ccc;
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.project-features {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.feature-tag {
  background: rgba(74, 158, 255, 0.1);
  color: #4A9EFF;
  padding: 0.3rem 0.8rem;
  border-radius: 20px;
  font-size: 0.8rem;
  border: 1px solid rgba(74, 158, 255, 0.3);
  transition: all 0.3s ease;
}

.project-card:hover .feature-tag {
  background: rgba(74, 158, 255, 0.2);
  border-color: rgba(74, 158, 255, 0.5);
}

@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }
  
  .project-card {
    padding: 1.5rem;
  }
}
</style>