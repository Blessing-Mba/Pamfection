<template>
  <div class="menu" id="catalog">
    <div class="menu-section birthday-cakes">
      <h2>Hair Installation</h2>
      <p class="section-description">Flawless hair installations that blend seamlessly, boost confidence, and turn heads every time.</p>
      <div class="menu-grid">
        <div class="menu-item">
          <div class="menu-image">
            <img src="../assets/sew-in.jpg" alt="Sew-in" />
            <div class="overlay">
              
            </div>
          </div>
          <div class="item-details">
            <h3>Sew-in</h3>
            <p>Perfect for any celebration</p>
          </div>
        </div>
        <div class="menu-item">
          <div class="menu-image">
            <img src="../assets/wig-install.jpg" alt="Wig installation" />
            <div class="overlay">
              
            </div>
          </div>
          <div class="item-details">
            <h3>Wig installation</h3>
            <p>Elegantly crafted for special moments</p>
          </div>
        </div>
        <div class="menu-item">
          <div class="menu-image">
            <img src="../assets/tape-in.jpg" alt="tape-in" />
            <div class="overlay">
              
            </div>
          </div>
          <div class="item-details">
            <h3>Tape-in</h3>
            <p>Designed to match your theme</p>
          </div>
        </div>
      </div>
    </div>

    <div class="menu-section pastries">
      <h2>Braiding Services</h2>
      <p class="section-description">Neat, stylish braids that protect your hair, elevate your look, and boost your confidence</p>
      <div class="menu-grid">
        <div class="menu-item">
          <div class="menu-image">
            <img src="../assets/knotless.jpg" alt="Knotless" />
            <div class="overlay">
              
            </div>
          </div>
          <div class="item-details">
            <h3>Knotless Braids</h3>
            <p>Perfect for tea time</p>
          </div>
        </div>
        <div class="menu-item">
          <div class="menu-image">
            <img src="../assets/tribal.jpg" alt="Tribal" />
            <div class="overlay">
              
            </div>
          </div>
          <div class="item-details">
            <h3>Tribal Braids</h3>
            <p>Handcrafted with love</p>
          </div>
        </div>
        <div class="menu-item">
          <div class="menu-image">
            <img src="../assets/passion twists.jpg" alt="Passion twists" />
            <div class="overlay">
              
            </div>
          </div>
          <div class="item-details">
            <h3>Passion Twists</h3>
            <p>For the finest occasions</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.menu {
  width: 100%;
  padding: 2rem 0;
  background-color: #fff;
}

.menu-section {
  padding: 4rem 2rem;
  max-width: 1200px;
  margin: 0 auto;
}

.menu-section h2 {
  font-size: 2.5rem;
  color: #000;
  text-align: center;
  font-family: 'Playfair Display', serif;
  margin-bottom: 1rem;
}

.section-description {
  text-align: center;
  color: #000;
  font-size: 1.2rem;
  margin-bottom: 3rem;
  font-family: 'Open Sans', sans-serif;
}

.menu-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  padding: 1rem;
}

.menu-item {
  background: white;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 4px 16px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.menu-item:hover {
  transform: translateY(-5px);
}

.menu-image {
  position: relative;
  width: 100%;
  height: 420px;
  overflow: hidden;
}

.menu-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.menu-item:hover .menu-image img {
  transform: scale(1.05);
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.4);
  display: flex;
  justify-content: center;
  align-items: center;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.menu-item:hover .overlay {
  opacity: 1;
}

.order-now {
  padding: 0.8rem 1.5rem;
  background-color: #ffc8dd;
  color: #333;
  border: none;
  border-radius: 25px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
}

.order-now:hover {
  background-color: #ffb3d1;
  transform: scale(1.05);
}

.item-details {
  padding: 1.5rem;
  text-align: center;
}

.item-details h3 {
  font-size: 1.2rem;
  color: #333;
  margin-bottom: 0.5rem;
  font-family: 'Playfair Display', serif;
}

.item-details p {
  color: #000;
  font-size: 0.9rem;
  font-family: 'Open Sans', sans-serif;
}

@media (max-width: 1024px) {
  .menu-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .menu-section {
    padding: 3rem 1rem;
  }

  .menu-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .menu-section h2 {
    font-size: 1.8rem;
  }

  .section-description {
    font-size: 0.95rem;
    margin-bottom: 2rem;
  }

  .item-details h3 {
    font-size: 1.1rem;
  }

  .item-details p {
    font-size: 0.85rem;
  }
}
</style>