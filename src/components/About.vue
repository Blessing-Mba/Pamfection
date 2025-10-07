<template>
  <div class="about-container" id="about">
    <div class="about-content">
      <h2>About Us</h2>
      <div class="about-text">
        <p>
          At Pamfection, we believe beauty is more than skin deep — it's confidence, empowerment, and self-expression. 
          Located in the heart of Birmingham, we specialize in professional makeup artistry, hair installation, and 
          braiding services designed to help you look and feel your absolute best.
        </p>
        <p>
          Whether you're getting ready for a special occasion or just treating yourself to a new look, our team of 
          skilled beauty professionals are here to transform your vision into reality.
        </p>
      </div>
      <div class="about-values">
        <div class="value-item">
          <div class="value-icon">✨</div>
          <h3>Quality</h3>
          <p>We never compromise on the products we use or the techniques we employ.</p>
        </div>
        <div class="value-item">
          <div class="value-icon">🤝</div>
          <h3>Personalization</h3>
          <p>Every service is tailored to match your unique style and preferences.</p>
        </div>
        <div class="value-item">
          <div class="value-icon">🌟</div>
          <h3>Satisfaction</h3>
          <p>Your happiness is our priority - we're not satisfied until you are.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style scoped>
.about-container {
  padding: 5rem 2rem;
  background: linear-gradient(rgba(255, 255, 255, 0.9), rgba(255, 200, 221, 0.2));
}

.about-content {
  max-width: 1200px;
  margin: 0 auto;
  text-align: center;
}

.about-content h2 {
  font-size: 2.8rem;
  color: #333;
  margin-bottom: 2rem;
  font-family: 'Playfair Display', serif;
  font-weight: 600;
  position: relative;
  display: inline-block;
}

.about-content h2::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 80px;
  height: 3px;
  background: linear-gradient(90deg, #ffc8dd, #ffafcc);
  border-radius: 2px;
}

.about-text {
  max-width: 800px;
  margin: 0 auto 3rem;
}

.about-text p {
  margin-bottom: 1.5rem;
  font-size: 1.1rem;
  line-height: 1.8;
  color: #555;
}

.about-values {
  display: flex;
  justify-content: space-between;
  margin-top: 2rem;
  position: relative;
  overflow: hidden;
  height: 280px;
}

.value-item {
  background: white;
  padding: 1.5rem;
  border-radius: 20px;
  box-shadow: 0 4px 16px rgba(0,0,0,0.06);
  transition: transform 0.3s ease;
  animation: slideAcross 15s linear infinite;
  width: 28%;
  position: absolute;
  height: 250px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.value-item p {
  color: #666;
  line-height: 1.6;
  flex-grow: 1;
  display: flex;
  align-items: center;
  max-width: 90%; /* Control text width */
}

.value-item:nth-child(1) {
  animation-delay: 0s;
  left: 0;
}

.value-item:nth-child(2) {
  animation-delay: -5s; /* Increased delay to add more space between boxes */
  left: 0;
}

.value-item:nth-child(3) {
  animation-delay: -10s; /* Increased delay to add more space between boxes */
  left: 0;
}

@keyframes slideAcross {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(calc(100vw - 28%));
  }
}

.value-item:hover {
  animation-play-state: paused;
  transform: scale(1.05);
  z-index: 10;
}

.value-icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.value-item h3 {
  font-size: 1.5rem;
  color: #333;
  margin-bottom: 1rem;
  font-family: 'Playfair Display', serif;
  font-weight: 600;
}

.value-item p {
  color: #666;
  line-height: 1.6;
}

@media (max-width: 768px) {
  .about-container {
    padding: 3rem 1rem;
  }
  
  .about-content h2 {
    font-size: 2rem;
  }
  
  .about-text p {
    font-size: 0.95rem;
    line-height: 1.6;
  }
  
  .about-values {
    display: grid;
    grid-template-columns: 1fr;
    gap: 1.5rem;
    height: auto;
    overflow: visible;
  }
  
  .value-item {
    position: static;
    width: 100%;
    height: auto;
    min-height: 180px;
    padding: 1.2rem;
    animation: none;
    margin-bottom: 1rem;
  }
  
  .value-item h3 {
    font-size: 1.3rem;
    margin-bottom: 0.5rem;
  }
  
  .value-item p {
    font-size: 0.9rem;
    line-height: 1.5;
  }
  
  .value-icon {
    font-size: 2rem;
    margin-bottom: 0.5rem;
  }
}
</style>