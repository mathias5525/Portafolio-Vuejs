<template>
  <nav class="navbar">
    <div class="navbar-menu">
      <ul>
        <a v-for="nav in navegacion" :key="nav.nombre" :href="nav.enlace" class="nav-item">{{
          nav.nombre
          }}</a>
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'
const navegacion = ref([
  { id: 1, nombre: 'Educación', enlace: '#educacion' },
  { id: 2, nombre: 'Experiencia', enlace: '#experiencia' },
  { id: 3, nombre: 'Proyectos', enlace: '#proyectos' },
  { id: 4, nombre: 'Habilidades', enlace: '#habilidades' },
  { id: 5, nombre: 'Intereses', enlace: '#intereses' },
])
</script>

<style scoped>
.navbar {
  background: linear-gradient(90deg, #75757a, #2c2b31);
  color: #fff;
  padding: 0.5rem 1rem;
  align-items: center;
}

.navbar-item {
  color: #fff;
  margin-right: 1rem;
  text-decoration: none;
}

.navbar-menu {
  display: flex;
  justify-content: flex-end;
  list-style: none;
}

.navbar-menu li {
  list-style: none;
}

/* .nav-list {
  list-style: none;
} */

a {
  border: 1px solid;
  border-color: hsla(0, 10%, 82%, 0.2);
  border-radius: 5px;
  text-decoration: none;
  /*elimina el subrayado predeterminado de los enlaces */
  transition: 0.4s;
  /*suaviza la transición de estilos */
  padding: 5px;
  /*añade padding alrededor del contenido */
}

a:hover {
  background-color: hsla(247, 75%, 11%, 0.2);
  /*cambia el color de fondo al pasar el ratón */
}

@media (max-width: 768px) {
  .navbar-menu {
    display: flex;
    justify-content: flex-end;
    width: 100%;
  }
}
</style>
