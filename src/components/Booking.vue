<template>
  <div class="booking-container" id="booking">
    <div class="booking-content">
      <h2>Book Your Appointment</h2>
      <p class="booking-intro">Ready to transform your look? Schedule your appointment with our easy online booking system.</p>
      
      <div class="calendly-container">
        <!-- Calendly inline widget -->
        <div 
          class="calendly-inline-widget" 
          data-url="https://calendly.com/pamfection1"
          style="min-width:320px;height:700px;"
        ></div>
      </div>
      
      <div class="whatsapp-follow-up">
        <p>Need to discuss details after booking?</p>
        <a href="https://wa.me/447466351407?text=Hello!%20I%20just%20booked%20an%20appointment%20and%20would%20like%20to%20discuss%20some%20details." class="whatsapp-btn" target="_blank">
          <span>Message us on WhatsApp</span>
          <svg class="whatsapp-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24">
            <path fill="currentColor" d="M12 2C6.48 2 2 6.48 2 12c0 1.82.49 3.53 1.35 5L2 22l5-.35C8.47 22.51 10.18 23 12 23c5.52 0 10-4.48 10-10S17.52 2 12 2zm5.46 14.06c-.24.66-1.2 1.26-1.96 1.42-.52.11-1.21.08-1.95-.03-.61-.09-1.29-.27-2.27-.61-1.33-.46-2.5-1.17-3.42-2.09-.92-.92-1.63-2.1-2.09-3.42-.34-.98-.52-1.66-.61-2.27-.11-.74-.14-1.43-.03-1.95.16-.76.76-1.72 1.42-1.96.37-.13.83-.1 1.24.1.03.01.06.02.08.03.22.09.46.35.6.67l.95 2.05c.06.13.08.25.08.37 0 .14-.03.28-.09.41-.1.23-.17.46-.25.71-.11.35-.17.6.01.87l.27.35c.31.39.78.86 1.31 1.39.53.53 1 1 1.39 1.31l.35.27c.27.18.52.12.87.01.25-.08.48-.15.71-.25.13-.06.27-.09.41-.09.12 0 .24.02.37.08l2.05.95c.32.14.58.38.67.6.01.02.02.05.03.08.2.41.23.87.1 1.24z"/>
          </svg>
        </a>
      </div>
      
      <div class="booking-info">
        <div class="info-card">
          <div class="info-icon">📅</div>
          <h3>Easy Scheduling</h3>
          <p>Choose a service, select your preferred date and time, and confirm your booking in minutes.</p>
        </div>
        <div class="info-card">
          <div class="info-icon">📱</div>
          <h3>Instant Confirmation</h3>
          <p>Receive immediate confirmation and reminders directly to your email or phone.</p>
        </div>
        <div class="info-card">
          <div class="info-icon">✨</div>
          <h3>Personalized Service</h3>
          <p>Add notes about your preferences to help us prepare for your appointment.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Booking',
  mounted() {
    // Load the Calendly script
    const head = document.querySelector('head');
    const script = document.createElement('script');
    script.type = 'text/javascript';
    script.src = 'https://assets.calendly.com/assets/external/widget.js';
    script.async = true;
    head.appendChild(script);
  }
}
</script>
<style scoped>
.booking-container {
  padding: 5rem 2rem;
  background: #E8E2F4;
}

.booking-content {
  max-width: 1200px;
  margin: 0 auto;
  text-align: center;
}

.booking-content h2 {
  font-size: 2.8rem;
  color: #333;
  margin-bottom: 1.5rem;
  font-family: 'Playfair Display', serif;
  font-weight: 600;
  position: relative;
  display: inline-block;
}

.booking-content h2::after {
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

.booking-intro {
  max-width: 700px;
  margin: 0 auto 3rem;
  font-size: 1.1rem;
  line-height: 1.8;
  color: #555;
}

.calendly-container {
  margin: 2rem auto;
  max-width: 900px;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 8px 30px rgba(0,0,0,0.1);
}

.booking-info {
  display: flex;
  justify-content: space-between;
  gap: 2rem;
  margin-top: 4rem;
}

.info-card {
  background: white;
  padding: 2rem;
  border-radius: 20px;
  box-shadow: 0 4px 16px rgba(0,0,0,0.06);
  transition: transform 0.3s ease;
  flex: 1;
}

.info-card:hover {
  transform: translateY(-5px);
}

.info-icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.info-card h3 {
  font-size: 1.5rem;
  color: #333;
  margin-bottom: 1rem;
  font-family: 'Playfair Display', serif;
  font-weight: 600;
}

.info-card p {
  color: #666;
  line-height: 1.6;
}

@media (max-width: 768px) {
  .booking-container {
    padding: 3rem 1rem;
  }
  
  .booking-content h2 {
    font-size: 2rem;
  }
  
  .booking-intro {
    font-size: 0.95rem;
    line-height: 1.6;
  }
  
  .booking-info {
    flex-direction: column;
    gap: 1.5rem;
  }
  
  .calendly-container {
    margin: 1.5rem auto;
  }
  
  .info-card {
    padding: 1.5rem;
  }
  
  .info-card h3 {
    font-size: 1.3rem;
  }
}

.whatsapp-follow-up {
  margin: 2rem auto;
  text-align: center;
}

.whatsapp-follow-up p {
  margin-bottom: 1rem;
  color: #000;
  font-size: 1.1rem;
}

.whatsapp-btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.8rem;
  padding: 0.8rem 1.5rem;
  background-color: #25D366;
  color: white;
  border-radius: 50px;
  text-decoration: none;
  font-weight: 500;
  font-family: 'Poppins', sans-serif;
  transition: all 0.3s ease;
  box-shadow: 0 4px 12px rgba(37, 211, 102, 0.3);
}

.whatsapp-btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 16px rgba(37, 211, 102, 0.4);
}

.whatsapp-icon {
  width: 24px;
  height: 24px;
}

.payment-section {
  max-width: 600px;
  margin: 3rem auto;
  padding: 2rem;
  background-color: white;
  border-radius: 20px;
  box-shadow: 0 4px 16px rgba(0,0,0,0.08);
}

.payment-section h3 {
  font-size: 1.8rem;
  margin-bottom: 1rem;
  font-family: 'Playfair Display', serif;
}

.payment-section p {
  margin-bottom: 1.5rem;
  color: #555;
}

.payment-options {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.apple-pay-button {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  background-color: black;
  color: white;
  border: none;
  border-radius: 8px;
  padding: 0.8rem 1.5rem;
  font-size: 1rem;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.2s ease;
}

.apple-pay-button:hover {
  background-color: #333;
}

.stripe-button {
  background-color: #6772e5;
  color: white;
  border: none;
  border-radius: 8px;
  padding: 0.8rem 1.5rem;
  font-size: 1rem;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.2s ease;
}

.stripe-button:hover {
  background-color: #5469d4;
}

.payment-message {
  margin-top: 1rem;
  min-height: 20px;
  color: #5469d4;
}

@media (max-width: 768px) {
  .payment-options {
    flex-direction: column;
    gap: 1rem;
  }
  
  .apple-pay-button, .stripe-button {
    width: 100%;
  }
}
</style>
