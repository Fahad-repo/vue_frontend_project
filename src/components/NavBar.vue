<template>
  <nav>
    <router-link to="/posts">Posts</router-link>
    <router-link to="/users">Users</router-link>
    <router-link to="/comments">Comments</router-link>
    <router-link to="/albums">Albums</router-link>
    <router-link to="/photos">Photos</router-link>
    <router-link to="/todos">Todos</router-link>
  </nav>
</template>

<style scoped>
nav {
  display: flex;
  justify-content: center;
  gap: 1.5rem;
  background: #f8f9fa;
  padding: 1rem 2rem;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.05);
}

a {
  text-decoration: none;
  color: #444;
  font-weight: 500;
  padding: 0.5rem 0.75rem;
  border-radius: 4px;
  transition: background-color 0.2s ease, color 0.2s ease;
}

a:hover {
  background-color: #e2f0ec;
  color: #2c7a7b;
}

.router-link-active {
  font-weight: 600;
  color: #2c7a7b;
  background-color: #c6f6d5;
}
</style>
