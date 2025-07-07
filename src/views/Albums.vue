<template>
  <div>
    <h1>Albums</h1>
    <div v-if="loading">Loading...</div>
    <div v-else class="grid">
      <div v-for="album in albums" :key="album.id" class="card">
        <h3>{{ album.title }}</h3>
        <p>{{ album.body }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  data() {
    return {
      albums: [],
      loading: true,
    };
  },
  mounted() {
    axios.get('https://jsonplaceholder.typicode.com/albums').then(res => {
      this.albums = res.data;
      this.loading = false;
    });
  },
};
</script>

<style scoped>
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 1.5rem;
  padding: 1rem;
}

.card {
  background-color: #fff;
  padding: 1.25rem;
  border-radius: 12px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  cursor: pointer;
}

.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}

.card h3 {
  margin: 0 0 0.5rem;
  font-size: 1.1rem;
  color: #333;
}

.card p {
  margin: 0;
  font-size: 0.95rem;
  color: #666;
  line-height: 1.4;
}

h1 {
  text-align: center;
  font-size: 2rem;
  margin: 1rem 0;
  color: #2c3e50;
}
</style>
