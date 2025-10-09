<template>
  <footer class="footer" id="footer">
    <div class="footer-content">
      <div class="footer-section">
        <h3>Contact Us</h3>
        <p>📍United Kingdom</p>
        <p>📞 +44 7466 351407 </p>
        <p>✉️ Pamfection1@gmail.com</p>
      </div>
      <div class="footer-section">
        <h3>Follow Us</h3>
        <div class="social-links">
          <a href="https://instagram.com/Pamfection1" target="_blank" rel="noopener noreferrer" class="social-link">
            <i class="fab fa-instagram"></i>
          </a>
          
          <a href="https://www.tiktok.com/@pamfection" target="_blank" rel="noopener noreferrer" class="social-link">
            <i class="fab fa-tiktok"></i>
          </a>
          
          <a href="https://wa.me/234" target="_blank" rel="noopener noreferrer" class="social-link">
            <i class="fab fa-whatsapp"></i>
          </a>
        </div>
      </div>
      <div class="footer-section">
        <h3>Business Hours</h3>
        <p>Monday - Friday: 08:00am - 18:00pm </p>
        <p>Saturday: 09:00am - 19:00pm </p>
        <p>Sunday: 13:00pm - 18:00pm </p>
      </div>
    </div>
    <div class="footer-bottom">
      <p>&copy; {{ new Date().getFullYear() }} Pamfection. All rights reserved.</p>
    </div>
  </footer>
</template>

<script setup>
// No additional script needed
</script>

<style scoped>
.footer {
  background: #FFF;
  padding: 4rem 2rem 2rem;
  color: #000;
  width: 100%;
}

.footer-content {
  max-width: 1200px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 3rem;
  margin-bottom: 3rem;
}

.footer-section h3 {
  font-family: 'Playfair Display', serif;
  font-size: 1.8rem;
  margin-bottom: 1.5rem;
  color: #000;
  position: relative;
  display: inline-block;
}

.footer-section h3::after {
  content: '';
  position: absolute;
  bottom: -8px;
  left: 0;
  width: 40px;
  height: 2px;
  background: #333;
}

.footer-section p {
  margin-bottom: 0.8rem;
  font-size: 1.1rem;
  line-height: 1.6;
}

.social-links {
  display: flex;
  gap: 1.5rem;
  margin-top: 1rem;
}

.social-link {
  color: #333;
  font-size: 1.5rem;
  transition: all 0.3s ease;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.2);
}

.social-link:hover {
  transform: translateY(-3px);
  background: rgba(255, 255, 255, 0.4);
  color: #ff4d6d;
}

.footer-bottom {
  text-align: center;
  padding-top: 2rem;
  border-top: 1px solid rgba(255, 255, 255, 0.2);
}

.footer-bottom p {
  font-size: 0.9rem;
  color: #1C1C1C;
}

@media (max-width: 768px) {
  .footer {
    padding: 3rem 1rem 1.5rem;
  }

  .footer-content {
    grid-template-columns: 1fr;
    gap: 2.5rem;
    text-align: center;
  }
  
  .footer-section {
    padding: 0 1rem;
    border-bottom: 1px solid rgba(0,0,0,0.05);
    padding-bottom: 2rem;
  }
  
  .footer-section:last-child {
    border-bottom: none;
  }
  
  .footer-section h3 {
    font-size: 1.5rem;
    margin-bottom: 1.5rem;
  }
  
  .footer-section p {
    font-size: 1rem;
    margin-bottom: 0.8rem;
  }
  
  .footer-section h3::after {
    left: 50%;
    transform: translateX(-50%);
    width: 60px;
    height: 3px;
  }
  
  .social-links {
    justify-content: center;
    gap: 2rem;
    margin-top: 1.5rem;
  }
  
  .social-link {
    width: 45px;
    height: 45px;
    font-size: 1.5rem;
    background: rgba(0,0,0,0.03);
  }
}

@media (max-width: 576px) {
  .footer {
    padding: 2rem 1rem 1rem;
  }
  
  .footer-section {
    padding-bottom: 1.5rem;
  }
  
  .footer-section h3 {
    font-size: 1.4rem;
  }
  
  .footer-section p {
    font-size: 0.95rem;
  }
  
  .social-link {
    width: 40px;
    height: 40px;
    font-size: 1.3rem;
  }
  
  .footer-bottom {
    padding-top: 1.5rem;
  }
  
  .footer-bottom p {
    font-size: 0.85rem;
  }
}
</style>