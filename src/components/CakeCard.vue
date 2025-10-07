<template>
  <div class="cake-card">
    <img :src="image" :alt="name" class="cake-image" />
    <h3 class="cake-name">{{ name }}</h3>
    <p class="cake-description">{{ description }}</p>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    description: String,
    image: String,
  },
};
</script>

<style scoped>
.cake-card {
  background: #fff;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  text-align: center;
  transition: transform 0.3s;
}

.cake-card:hover {
  transform: translateY(-5px);
}

.cake-image {
  width: 100%;
  height: auto;
  object-fit: cover;
}

.cake-name {
  font-size: 1.2rem;
  margin: 0.5rem 0;
  color: #333;
}

.cake-description {
  font-size: 1rem;
  color: #666;
  padding: 0 1rem 1rem;
}

@media (max-width: 768px) {
  .cake-name {
    font-size: 1.1rem;
    margin: 0.4rem 0;
  }

  .cake-description {
    font-size: 0.9rem;
    padding: 0 0.8rem 0.8rem;
  }
}
</style>
