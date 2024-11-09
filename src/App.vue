<template>
  <div id="app">
    <!-- Barra de navegación con enlaces a diferentes rutas -->
    <nav class="navbar">
      <router-link to="/" class="navbar-brand" style="text-decoration: none;">
        <img src="https://upload.wikimedia.org/wikipedia/commons/f/f1/Vue.png" alt="Vue Logo" class="logo" />
        <span class="brand-name">Gestor de Tareas</span>
      </router-link>
      <!--Enlaces de navegacion-->
      <div class="nav-links">
        <router-link to="/addtask">Agregar Tarea</router-link>
        <router-link to="/tasklist">Lista de Tareas</router-link>
        <router-link to="/combinedview">Vista Combinada</router-link>
      </div>
    </nav>
    <!-- Aquí se cargará el componente correspondiente a la ruta seleccionada -->
    <router-view/>
  </div>
</template>

<style>
.navbar-brand {
  display: flex;
  align-items: center;
  color: white; /* Asegura que el texto sea blanco */
  text-decoration: none; /* Elimina el subrayado del enlace */
}
.navbar-brand:hover,
.navbar-brand:focus,
.navbar-brand.router-link-active {
  color: white; /* Mantiene el color blanco al pasar el mouse o al estar activo */
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #007bff; /* Fondo azul */
  padding: 15px 30px;
  color: white;
}
.logo {
  width: 40px; /* Ajusta el tamaño del logo según sea necesario */
  margin-right: 10px;
}
.brand-name {
  font-size: 1.5rem;
  font-weight: bold;
}
.nav-links {
  display: flex;
  gap: 20px;
}
.nav-links a {
  color: white;
  font-weight: bold;
  text-decoration: none;
  font-size: 1rem;
}
.nav-links a.router-link-exact-active {
  text-decoration: underline;
}
.nav-links a:hover {
  text-decoration: underline;
}
</style>
