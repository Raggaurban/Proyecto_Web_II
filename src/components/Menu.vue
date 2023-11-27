<template>
    <nav>
      <button @click="mostrarSeccion('inicio')">Inicio</button>
      <button @click="mostrarSeccion('historia')">Historia</button>
      <button @click="mostrarSeccion('juegos')">Juegos</button>
      <button @click="mostrarSeccion('articulos')">Artículos</button>
      <button @click="mostrarSeccion('contacto')">Contacto</button>
    </nav>
  </template>
  
  <script>
  export default {
    methods: {
      mostrarSeccion(seccion) {
        this.$emit('cambiar-seccion', seccion);
      }
    }
  };
  </script>
  
  <style scoped>
  /* Estilos específicos del menú */
  nav {
    background-color: #333;
    padding: 10px;
  }
  
  button {
    margin-right: 10px;
    color: white;
    background-color: transparent;
    border: none;
    cursor: pointer;
  }
  
  button:hover {
    text-decoration: underline;
  }
  </style>
  