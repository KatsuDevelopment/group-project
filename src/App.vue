<template>
  <nav class="navbar navbar-expand-lg" style="background-color: #b6d7a8;">
    <div class="container d-flex align-items-center">
      <router-link to="/"><a class="navbar-brand" href="#">
        <img src="./assets/brand.jpg" alt="Logo" class="navbar-logo">
      </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
    </router-link>
      <div class="ms-3">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About Us</router-link>
      </div>
    </div>
  </nav>
  <router-view />
</template>

<style>
#app {
  font-family: Berlin Sans FB, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

.nav-link {
  color: white !important;
  font-weight: 500;
}

.nav-link:hover {
  text-decoration: underline;
}

.navbar-logo {
  width: 48px;
  height: 48px;
  object-fit: contain;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  background: #fff;
  padding: 4px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  margin: 0 8px;
  text-decoration: none;
}

nav a.router-link-exact-active {
  color: #314D0D;
}
</style>