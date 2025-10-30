<template>
  <nav class="navbar navbar-expand-lg" style="background-color: #b6d7a8;">
    <div class="container d-flex align-items-center">
      <router-link to="/" class="navbar-brand">
        <img src="./assets/brand.jpg" alt="Logo" class="navbar-logo">
      </router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="ms-3 d-flex align-items-center">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About Us</router-link> |
        <div class="btn btn-custom ms-2">
        <router-link to="/login">Join</router-link>
        </div>
      </div>
    </div>
  </nav>
  <router-view />
</template>

// ...existing code...
<style>
/* Global background for entire site */
html, body, #app {
  background-color: #e9ffff;
  min-height: 100%;
  margin: 0;
}

/* keep existing rules */
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
  transform: translateY(-2px);
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
  transition: transform .15s ease, color .15s ease;
}

nav a.router-link-exact-active {
  color: #314D0D;
}

nav a:hover {
  transform: translateY(-2px);
  text-decoration: underline;
}

/* Added styles for alignment */
.ms-3 {
  display: flex;
  align-items: center;
}

.btn-custom {
  background-color: #314D0D;
  color: #2c3e50;
  font-family: Berlin Sans FB, Helvetica, Arial, sans-serif;
  font-weight: bold;
  border: 2px solid #1a3a0d;
  border-radius: 4px;
  padding: 10px 20px;
  font-size: 1.2em;
}

.btn-custom:hover {
  background-color: darkgreen;
  border-color: #1a3a0d;
  transform: translateY(-2px);
}

</style>