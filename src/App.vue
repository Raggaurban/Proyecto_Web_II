<!-- App.vue -->
<template>
  <div id="app">
    <header>
      <Menu @cambiar-seccion="cambiarSeccion" />
    </header>

    <main>
      <component :is="seccionActual" />
    </main>
  </div>
</template>

<script>
import InicioHome from "@/components/InicioHome.vue";
import HistoriaHistory from "@/components/HistoriaHistory.vue";
import JuegosGame from "@/components/JuegosGame.vue";
import ArticulosArticule from "@/components/ArticulosArticule.vue";
import ContactosFont from "@/components/ContactosFont.vue";

export default {
  data() {
    return {
      seccionActual: "InicioHome"
    };
  },
  components: {
    InicioHome,
    HistoriaHistory,
    JuegosGame,
    ArticulosArticule,
    ContactosFont
  },
  methods: {
    cambiarSeccion(seccion) {
      this.seccionActual = seccion;
    }
  }
};
</script>

<style>
/* Estilos globales de la aplicación */
header {
  background-color: #ddd;
  padding: 10px;
}
</style>
