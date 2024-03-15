<template>
  <div class="art-grid">
    <div v-for="artwork in artworks" :key="artwork.id" class="artwork">
      <img :src="artwork.image" alt="Artwork" class="artwork-image" />
      <h3 class="artwork-title">{{ artwork.title }}</h3>
      <p class="artwork-description">{{ artwork.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      artworks: [
        {
          id: 1,
          image: './src/assets/art/mai.jpg',
          title: 'Artwork 1',
          description: 'Description of Artwork 1'
        },
        {
          id: 2,
          image: './src/assets/art/random.jpeg',
          title: 'Artwork 2',
          description: 'Description of Artwork 2'
        }
        // Add more artworks as needed
      ]
    }
  }
}
</script>

<style scoped>
.art-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 20px;
}

.artwork {
  text-align: center;
}

.artwork-image {
  width: 100%;
  height: auto;
}

.artwork-title {
  margin-top: 10px;
}

.artwork-description {
  margin-top: 5px;
}
</style>
