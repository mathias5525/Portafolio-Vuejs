<template>
  <section class="timeline">
    <div v-for="(item, index) in educacion" :key="item.id" :class="['container', index % 2 === 0 ? 'left' : 'right']">
      <div class="content">
        <h3>{{ item.titulo }}</h3>
        <p>{{ item.descripcion }}</p>
        <span class="year">{{ item.fecha }}</span>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const educacion = ref([
  {
    id: 1,
    fecha: '2025 - Presente',
    titulo: 'Técnico Universitario en Programación',
    descripcion: 'UTN - San Rafael.',
  },
  {
    id: 2,
    fecha: '2023',
    titulo: 'Primeros pasos Desarrollo Frontend',
    descripcion: 'Argentina Programa 4.0.',
  },
  {
    id: 3,
    fecha: '2022',
    titulo: 'Curso Programacion Python',
    descripcion: 'Fundacion Santisima Trinidad.',
  },
  {
    id: 4,
    fecha: '2021',
    titulo: 'Curso Python para ciencia de datos',
    descripcion: 'Cognitive Class.ai',
  },
  {
    id: 5,
    fecha: '2013 - 2015',
    titulo: 'Tec. Sup. en Analisis de Datos',
    descripcion: 'Instituto Superior de Informatica Virasoro - San Rafael.',
  },
  {
    id: 6,
    fecha: '2010 - 2012',
    titulo: 'Tec. Sup. en Instalacion y Reparacion de Equipios Informaticos',
    descripcion: 'IES 9-010 Rosario Vera Peñaloza - San Carlos.',
  },
  {
    id: 7,
    fecha: '2008',
    titulo: 'Curso Operador de PC',
    descripcion: 'Instituto de Formacion y Enseñanza de Informatica.',
  },

])
</script>

<style scoped>
/* Fondo general */
.timeline {
  position: relative;
  max-width: 900px;
  margin: 60px auto;
  padding: 20px 0;
}

/* Línea central */
.timeline::after {
  content: '';
  position: absolute;
  width: 6px;
  background: linear-gradient(180deg, #ff0057, #ff7b00);
  top: 0;
  bottom: 0;
  left: 50%;
  margin-left: -3px;
  border-radius: 6px;
}

/* Contenedores alternados */
.container {
  padding: 10px 40px;
  position: relative;
  width: 50%;
}

/* Puntos en la línea */
.container::after {
  content: '';
  position: absolute;
  width: 18px;
  height: 18px;
  right: -9px;
  background: linear-gradient(135deg, #ff0057, #ff7b00);
  border: 4px solid #1e1e1e;
  top: 15px;
  border-radius: 50%;
  z-index: 1;
}

/* Izquierda */
.left {
  left: 0;
}

/* Derecha */
.right {
  left: 50%;
}

/* Cuadros de contenido */
.content {
  background-color: #1e1e1e;
  color: white;
  padding: 20px;
  border-radius: 10px;
  position: relative;
  box-shadow: 0 4px 10px rgba(255, 255, 255, 0.05);
  /* Sombra suave */
  transition: all 0.3s ease;
}

.content:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 14px rgba(255, 255, 255, 0.1);
  /* Sombra más intensa */
}

/* Ajuste de puntos para la derecha */
.right::after {
  left: -9px;
}

/* Fecha */
.year {
  display: block;
  margin-top: 10px;
  color: #ff7b00;
  font-size: 0.9rem;
  font-weight: bold;
}

/* Responsivo */
@media screen and (max-width: 768px) {
  .timeline::after {
    left: 31px;
  }

  .container {
    width: 100%;
    padding-left: 70px;
    padding-right: 25px;
  }

  .container::after {
    left: 15px;
  }

  .right {
    left: 0;
  }
}
</style>
