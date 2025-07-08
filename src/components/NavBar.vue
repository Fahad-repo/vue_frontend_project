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
  flex-wrap: wrap;
  gap: 1rem;
  background: #ffffff;
  padding: 1rem 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.06);
}

a {
  text-decoration: none;
  color: #555;
  font-weight: 500;
  padding: 0.5rem 1rem;
  border-radius: 999px;
  transition: all 0.3s ease;
  background: #f1f5f9;
}

a:hover {
  background: linear-gradient(135deg, #38b2ac, #81e6d9);
  color: #fff;
}

.router-link-active {
  font-weight: 600;
  color: #fff;
  background: linear-gradient(135deg, #2c7a7b, #68d391);
}
</style>
