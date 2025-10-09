<template>
  <div class="review-container">
    <div class="review-header">
      <h2>Why Choose Us?</h2>
      <p class="subtitle"></p>
    </div>
    <div class="review-box">
      <div class="review-card">
        <div class="review-content">
          <div class="quote-icon">❝</div>
          <h3>Client-Centered Approach</h3>
          <p>We listen, consult, and personalize each service to match your unique vision and style</p>
          <div class="stars">★★★★★</div>
        </div>
       
      </div>

      <div class="review-card">
        <div class="review-content">
          <div class="quote-icon">❝</div>
           <h3>Experienced Professionals</h3>
          <p>Our certified and trained beauty artists stay up-to-date with the latest trends and techniques</p>
          <div class="stars">★★★★★</div>
        </div>
      
      </div>
       <div class="review-card">
        <div class="review-content">
          <div class="quote-icon">❝</div>
           <h3>Premium Products</h3>
          <p>Only the best tools and products touch your skin and hair, because you deserve nothing less.</p>
          <div class="stars">★★★★★</div>
        </div>
      
      </div>

      <div class="review-card">
        <div class="review-content">
          <div class="quote-icon">❝</div>
          <h3>Comfortable Environment</h3>
          <p>Enjoy your beauty experience in a welcoming, relaxing and hygienic studio.</p>
          <div class="stars">★★★★★</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// Component logic can be added here if needed
</script>

<style scoped>
.review-container {
  padding: 5rem 2rem;
  width: 100%;
  background: linear-gradient(rgba(255, 200, 221, 0.1), rgba(255, 255, 255, 0.95));
}

.review-header {
  text-align: center;
  margin-bottom: 3rem;
}

.review-header h2 {
  font-size: 2.5rem;
  color: #000;
  font-family: 'Playfair Display', serif;
  margin-bottom: 1rem;
}

.subtitle {
  color: #666;
  font-size: 1.2rem;
  font-family: 'Open Sans', sans-serif;
}

.review-box {
  display: flex;
  gap: 2rem;
  justify-content: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 1rem;
}

.review-card {
  flex: 1;
  max-width: 350px;
  background: white;
  border-radius: 20px;
  padding: 2rem;
  box-shadow: 0 4px 20px rgba(0,0,0,0.08);
  transition: transform 0.3s ease;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.review-card:hover {
  transform: translateY(-5px);
}

.review-content {
  position: relative;
  padding-top: 1rem;
}

.quote-icon {
  position: absolute;
  top: -1.5rem;
  left: -0.5rem;
  font-size: 4rem;
  color: #ffc8dd;
  opacity: 0.5;
}

.review-content p {
  position: relative;
  font-size: 1.1rem;
  line-height: 1.6;
  color: #444;
  margin-bottom: 1rem;
  font-family: 'Open Sans', sans-serif;
}

.stars {
  color: #FFD700;
  font-size: 1.2rem;
  margin: 1rem 0;
}

.reviewer-info {
  display: flex;
  align-items: center;
  margin-top: 1.5rem;
  padding-top: 1rem;
  border-top: 1px solid #eee;
}

.avatar {
  width: 40px;
  height: 40px;
  background: #ffc8dd;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
  margin-right: 1rem;
}

.name {
  font-weight: 600;
  color: #333;
  font-family: 'Open Sans', sans-serif;
}

@media (max-width: 1024px) {
  .review-box {
    flex-direction: column;
    align-items: center;
  }

  .review-card {
    width: 100%;
    max-width: 500px;
  }
}

@media (max-width: 768px) {
  .review-container {
    padding: 3rem 1rem;
  }

  .review-header h2 {
    font-size: 1.8rem;
  }

  .subtitle {
    font-size: 0.95rem;
  }

  .review-card {
    padding: 1.5rem;
  }

  .review-content p {
    font-size: 0.9rem;
    line-height: 1.5;
  }

  .review-content h3 {
    font-size: 1.2rem;
  }

  .stars {
    font-size: 1rem;
  }
}
</style>