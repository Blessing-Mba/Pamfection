<template>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">
  <nav class="navbar">
    <div class="navbar-brand">
      <p>Pamfection</p>
    </div>
    <ul class="navbar-links" :class="{ open: isMenuOpen }">
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#catalog">Catalog</a></li>
      <li><a href="#booking">Book Your Spot</a></li>
      <li><a href="#footer">Contact</a></li>
    </ul>
    <button class="menu-toggle" @click="toggleMenu">
      <span class="bar"></span>
      <span class="bar"></span>
      <span class="bar"></span>
    </button>
  </nav>
</template>

<script setup>
import { ref } from 'vue';
import Logo from '../assets/Logo.png';

const isMenuOpen = ref(false);
const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>

<style scoped>
/* General styles */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.5rem 2rem;
  background-color: white;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  width: 100%;
  box-sizing: border-box;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1000;
}

.navbar-brand {
  display: flex;
  align-items: center;
}


.navbar-brand p {
  font-size: 3rem;
  font-family: "Pacifico", cursive;
  font-weight: 400;
  font-style: normal;
}
.logo {
  height: 80px;
  width: auto;
  padding: 0.5rem 0;
}

.menu-toggle {
  display: none;
  flex-direction: column;
  justify-content: space-between;
  width: 25px;
  height: 20px;
  background: none;
  border: none;
  cursor: pointer;
  margin-left: 1rem;
}

.menu-toggle .bar {
  width: 100%;
  height: 3px;
  background-color: #333;
}

/* Links */
.navbar-links {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
}

.navbar-links li {
  margin: 0 1rem;
}

.navbar-links a {
  text-decoration: none;
  color: #333;
  font-weight: 500;
  transition: color 0.3s;
}

.navbar-links a:hover {
  color: #ffc8dd;
}

/* Responsive styles */
@media (max-width: 768px) {
  .menu-toggle {
    display: flex;
  }

  .navbar-brand p {
    font-size: 2.2rem;
  }

  .navbar-links {
    position: fixed;
    top: 72px;
    left: 0;
    right: 0;
    flex-direction: column;
    align-items: flex-start;
    background-color: white;
    width: 100%;
    display: none;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }

  .navbar-links.open {
    display: flex;
  }

  .navbar-links li {
    margin: 1rem;
  }

  .navbar-links a {
    font-size: 0.95rem;
  }
}
</style>
