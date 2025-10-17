<script setup>
import NavBar from './components/NavBar.vue';
import About from './components/About.vue';
import MenuPart from './components/MenuPart.vue';
import Reviews from './components/Reviews.vue';
import Contact from './components/Contact.vue';
import Booking from './components/Booking.vue';
import Footer from './components/Footer.vue';
import headerImage from './assets/pam-header1.jpg';
import { onMounted, ref } from 'vue';

const openCalendly = () => {
  window.open('https://calendly.com/pamfection1', '_blank');
};

const titleText = ref('');
const subtitleText = ref('');
const fullTitle = 'Welcome to Pamfection';
const fullSubtitle = 'Where Beauty Begins';

onMounted(() => {
  animateText(fullTitle, titleText, 100);
  setTimeout(() => {
    animateText(fullSubtitle, subtitleText, 100);
  }, fullTitle.length * 100 + 300); // Start subtitle after title finishes
});

const animateText = (fullText, targetRef, speed) => {
  let index = 0;
  const interval = setInterval(() => {
    targetRef.value = fullText.substring(0, index + 1);
    index++;
    if (index >= fullText.length) {
      clearInterval(interval);
    }
  }, speed);
};
</script>

<template>
  <div class="app-container">
    <NavBar />
    <header class="hero-section" id="home">
      <div class="hero-content">
        <div class="text-content">
          <h1><span class="animated-text">{{ titleText }}</span><span class="cursor" :class="{ 'blinking': titleText === fullTitle }"></span></h1>
          <p><span class="animated-text">{{ subtitleText }}</span><span class="cursor" :class="{ 'blinking': subtitleText === fullSubtitle }"></span></p>
          <button class="order-btn" @click="openCalendly">
            <span>Book Now</span>
            <svg class="whatsapp-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24">
              <path fill="currentColor" d="M12 2C6.48 2 2 6.48 2 12c0 1.82.49 3.53 1.35 5L2 22l5-.35C8.47 22.51 10.18 23 12 23c5.52 0 10-4.48 10-10S17.52 2 12 2zm5.46 14.06c-.24.66-1.2 1.26-1.96 1.42-.52.11-1.21.08-1.95-.03-.61-.09-1.29-.27-2.27-.61-1.33-.46-2.5-1.17-3.42-2.09-.92-.92-1.63-2.1-2.09-3.42-.34-.98-.52-1.66-.61-2.27-.11-.74-.14-1.43-.03-1.95.16-.76.76-1.72 1.42-1.96.37-.13.83-.1 1.24.1.03.01.06.02.08.03.22.09.46.35.6.67l.95 2.05c.06.13.08.25.08.37 0 .14-.03.28-.09.41-.1.23-.17.46-.25.71-.11.35-.17.6.01.87l.27.35c.31.39.78.86 1.31 1.39.53.53 1 1 1.39 1.31l.35.27c.27.18.52.12.87.01.25-.08.48-.15.71-.25.13-.06.27-.09.41-.09.12 0 .24.02.37.08l2.05.95c.32.14.58.38.67.6.01.02.02.05.03.08.2.41.23.87.1 1.24z"/>
            </svg>
          </button>
        </div>
        <div class="image-content">
          <div class="cake-display">
            <img :src="headerImage" alt="Beautiful Birthday Cakes" class="hero-image" />
          </div>
        </div>
      </div>
    </header>
     <div class="About-section">
         <About />
     </div>
    <section class="menu-intro">
      <div class="intro-content">
        <h2>Explore Our Catalog</h2>
        <div class="offerings">
          <div class="offering-card">
            <div class="offering-icon">💄</div>
            <h3>Makeup Services</h3>
            <p>From soft glam to bold editorial looks, our makeup services are customized to suit your style and event needs, using high-quality products for flawless results.</p>
            <div class="service-list">
              <div class="service-item">
                <span class="service-dot"></span>
                <span class="service-name">Full face glam</span>
              </div>
              <div class="service-item">
                <span class="service-dot"></span>
                <span class="service-name">Bridal Makeup</span>
              </div>
              <div class="service-item">
                <span class="service-dot"></span>
                <span class="service-name">Natural/soft glam</span>
              </div>
              <div class="service-item">
                <span class="service-dot"></span>
                <span class="service-name">Editorial looks</span>
              </div>
            </div>
          </div>
          <div class="offering-card">
            <div class="offering-icon">🪮</div>
            <h3>Hair Installation</h3>
            <p>Looking to switch things up or add volume and length? Our hair installation services are tailored to your head shape and desired look, ensuring a flawless and natural appearance.</p>
            <div class="service-list">
              <div class="service-item">
                <span class="service-dot"></span>
                <span class="service-name">Sew-in installations</span>
              </div>
              <div class="service-item">
                <span class="service-dot"></span>
                <span class="service-name">Wig customization and installation</span>
              </div>
              <div class="service-item">
                <span class="service-dot"></span>
                <span class="service-name">Closure and frontal installs</span>
              </div>
              <div class="service-item">
                <span class="service-dot"></span>
                <span class="service-name">Tape-ins and Micro-links</span>
              </div>
            </div>
          </div>
          <div class="offering-card">
            <div class="offering-icon">💇‍♀️</div>
            <h3>Braiding Services</h3>
            <p>Protective styles that are both stylish and functional. Our braiding services are done with care, creativity, and precision for all hair types and lengths.</p>
            <div class="service-list">
              <div class="service-item">
                <span class="service-dot"></span>
                <span class="service-name">Knotless box braids</span>
              </div>
              <div class="service-item">
                <span class="service-dot"></span>
                <span class="service-name">Feed-in cornrows</span>
              </div>
              <div class="service-item">
                <span class="service-dot"></span>
                <span class="service-name">Tribal and Lemonande braids</span>
              </div>
              <div class="service-item">
                <span class="service-dot"></span>
                <span class="service-name">Passion twists and more</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <div class="content-container">
     
      <MenuPart />
      <Reviews />
      <Contact />
    </div>
    <Booking />
    <Footer />
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&family=Poppins:wght@300;400;500;600&family=Great+Vibes&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html, body {
  width: 100%;
  max-width: 100vw;
  overflow-x: hidden;
  font-family: 'Poppins', sans-serif;
}

#app {
  width: 100%;
  max-width: 100vw;
  overflow-x: hidden;
  position: relative;
}

.app-container {
  width: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.content-container {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.hero-section {
  margin-top: 100px;
  min-height: 70vh;
  width: 100%;
  background: linear-gradient(rgba(255, 255, 255, 0.95), rgba(255, 200, 221, 0.3));
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2rem;
  box-sizing: border-box;
  position: relative;
}

.hero-content {
  max-width: 1200px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 2.5rem;
  
}

.text-content {
  flex: 1;
  text-align: left;
  padding-right: 2rem;
  margin-bottom: 12rem;
}

.image-content {
  flex: 1.2;
  display: flex;
  justify-content: flex-end;
}

.cake-display {
  position: relative;
  width: 100%;
  max-width: 550px;
  padding: 1rem;
  background: white;
  border-radius: 20px;
  box-shadow: 0 8px 24px rgba(0,0,0,0.12);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
  cursor: pointer;
  overflow: hidden;
}

.cake-display::before {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: rgba(255, 255, 255, 0.9);
  padding: 0.8rem 1.5rem;
  border-radius: 25px;
  font-family: 'Poppins', sans-serif;
  font-size: 1rem;
  color: #333;
  opacity: 0;
  transition: opacity 0.3s ease;
  z-index: 2;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.cake-display:hover::before {
  opacity: 1;
}

.cake-display:hover {
  transform: translateY(-5px) scale(1.02);
  box-shadow: 0 12px 32px rgba(0,0,0,0.15);
}

.hero-image {
  width: 75%;
  height: auto;
  border-radius: 15px;
  transition: all 0.5s ease;
  display: block;
  transform-origin: center;
  position: relative;
  z-index: 1;
}

.cake-display:hover .hero-image {
  transform: scale(1.1);
}

.logo-overlay {
  position: absolute;
  bottom: -20px;
  right: 20px;
  background: white;
  padding: 0.5rem;
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  transition: all 0.3s ease;
  z-index: 3;
}

.cake-display:hover .logo-overlay {
  transform: translateY(-5px);
  box-shadow: 0 6px 16px rgba(0,0,0,0.15);
}

.brand-logo {
  height: 60px;
  width: auto;
  transition: transform 0.3s ease;
}

.logo-overlay:hover .brand-logo {
  transform: scale(1.1);
}

.cake-display.zoomed {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 90vw;
  height: 90vh;
  max-width: none;
  z-index: 1000;
  background: rgba(255, 255, 255, 0.98);
  padding: 2rem;
}

.cake-display.zoomed .hero-image {
  width: auto;
  height: 100%;
  object-fit: contain;
}

.cake-display.zoomed::before {
  content: '✨ Click to close';
  background: rgba(255, 255, 255, 0.95);
}

.hero-content h1 {
  font-size: 3.8rem;
  color: #333;
  margin-bottom: 1.5rem;
  font-family: 'Playfair Display', serif;
  font-weight: 700;
  line-height: 1.2;
  text-align: left;
  letter-spacing: -0.5px;
}
.text-content h1{
  font-size: 48px;
  color: #000;
  margin-top: 7rem;
}
.hero-content p {
  font-size: 1.5rem;
  color: #000;
  margin-bottom: 2rem;
  font-family: 'Poppins', sans-serif;
  font-weight: 300;
  line-height: 1.6;
  text-align: left;
}

.order-btn {
  padding: 1.2rem 2.5rem;
  font-size: 1.2rem;
  background-color: #ffb3d1;
  border: none;
  border-radius: 50px;
  color: #333;
  cursor: pointer;
  transition: all 0.3s ease;
  font-weight: 500;
  font-family: 'Poppins', sans-serif;
  letter-spacing: 0.5px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.8rem;
}

.whatsapp-icon {
  width: 24px;
  height: 24px;
  transition: transform 0.3s ease;
}

.order-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
  background-color: #ffb3d1;
}

.order-btn:hover .whatsapp-icon {
  transform: scale(1.1);
}

@media (max-width: 768px) {
  .hero-content {
    flex-direction: column-reverse;
    padding: 1rem;
    gap: 2rem;
  }

  .text-content {
    padding-right: 0;
    text-align: center;
    margin-bottom: 2rem;
  }

  .text-content h1 {
    text-align: center;
    font-size: 1.8rem;
    white-space: nowrap;
    line-height: 1.1;
  }

  .text-content p {
    text-align: center;
    font-size: 1rem;
    margin-bottom: 1.5rem;
  }

  .hero-content h1 {
    font-size: 1.8rem;
  }

  .hero-content p {
    font-size: 1rem;
  }

  .order-btn {
    padding: 0.8rem 1.8rem;
    font-size: 0.9rem;
  }

  .hero-section {
    margin-top: 90px;
    min-height: auto;
    padding: 2rem 1rem;
  }

  .cake-display {
    max-width: 100%;
    margin-bottom: 2rem;
    padding: 0.5rem;
  }

  .cake-display::before {
    font-size: 0.9rem;
    padding: 0.6rem 1.2rem;
  }

  .cake-display:hover {
    transform: translateY(-3px) scale(1.01);
  }

  .cake-display.zoomed {
    padding: 1rem;
  }

  .logo-overlay {
    bottom: -15px;
    right: 15px;
  }

  .brand-logo {
    height: 40px;
  }

  .image-content {
    justify-content: center;
    width: 100%;
  }
}

.menu-intro {
  padding: 4rem 2rem;
  background: #FFB8D2; /* Changed from gradient to solid color #FFB8D2 */
}

.intro-content {
  max-width: 1200px;
  margin: 0 auto;
  text-align: center;
}

.intro-content h2 {
  font-size: 2.8rem;
  color: #000;
  margin-bottom: 3rem;
  font-family: 'Playfair Display', serif;
  font-weight: 600;
  position: relative;
  display: inline-block;
}

.intro-content h2::after {
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

.offerings {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  margin-top: 2rem;
}

.offering-card {
  background: white;
  padding: 2rem;
  border-radius: 20px;
  box-shadow: 0 4px 16px rgba(0,0,0,0.06);
  transition: transform 0.3s ease;
  display: flex;
  flex-direction: column;
  height: 100%;
}

.offering-card:hover {
  transform: translateY(-5px);
}

.offering-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.offering-card h3 {
  font-size: 1.8rem;
  color: #000;
  margin-bottom: 1rem;
  font-family: 'Playfair Display', serif;
  font-weight: 600;
}

.offering-card p {
  color: #000;
  line-height: 1.8;
  font-family: 'Poppins', sans-serif;
  font-size: 14px;
  font-weight: 300;
  flex-grow: 1;
  margin-bottom: 1rem;
  text-align: left; /* Added this to align text to the left */
}

@media (max-width: 768px) {
  .menu-intro {
    padding: 3rem 1rem;
  }

  .offerings {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .intro-content h2 {
    font-size: 2rem; /* Reduced from 2.4rem to fit better on mobile */
    margin-bottom: 2rem; /* Reduced margin */
    white-space: nowrap; /* Prevents text from wrapping */
  }

  .offering-card {
    padding: 1.5rem;
  }

  .offering-card h3 {
    font-size: 1.6rem;
  }

  .offering-card p {
    font-size: 0.9rem; /* Reduced font size for better mobile fit */
    line-height: 1.6; /* Tighter line height */
  }
}
.service-list {
  margin-top: 1rem;
  text-align: left;
}

.service-item {
  display: flex;
  align-items: center;
  margin-bottom: 0.8rem;
  transition: transform 0.2s ease;
}

.service-item:hover {
  transform: translateX(5px);
}

.service-dot {
  width: 8px;
  height: 8px;
  background: linear-gradient(90deg, #ffc8dd, #ffafcc);
  border-radius: 50%;
  margin-right: 10px;
  display: inline-block;
}

.service-name {
  color: #000;
  font-size: 14px;
  font-weight: 400;
}

@media (max-width: 768px) {
  .service-name {
    font-size: 0.9rem;
  }
  
  .service-item {
    margin-bottom: 0.6rem;
  }
 se  
  /* Styles for the unavailable service notice */
  .service-unavailable {
    background-color: #fff3cd;
    border-left: 4px solid #ffc107;
    padding: 0.75rem;
    margin: 0.5rem 0 1rem 0;
    border-radius: 4px;
    display: flex;
    align-items: center;
    text-align: left;
  }
  
  .unavailable-icon {
    font-size: 1.2rem;
    margin-right: 0.5rem;
  }
  
  .unavailable-text {
    color: #856404;
    font-size: 0.9rem;
    font-weight: 500;
  }
  
  @media (max-width: 768px) {
    .service-unavailable {
      padding: 0.5rem;
    }
    
    .unavailable-text {
      font-size: 0.8rem;
    }
  }
}
</style>