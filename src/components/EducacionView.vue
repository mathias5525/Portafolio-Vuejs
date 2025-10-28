<template>
  <section class="max-w-3xl mx-auto py-10 px-6">
    <h2 class="text-3xl font-bold text-center mb-10 text-gray-800">
      📚 Educación y Cursos Realizados
    </h2>

    <div class="relative border-l border-gray-300">
      <div v-for="item in educacion" :key="item.id" class="mb-10 ml-6">
        <!-- Punto en la línea -->
        <span
          class="absolute -left-3 flex items-center justify-center w-6 h-6 bg-blue-500 rounded-full ring-4 ring-white"></span>

        <!-- Contenido -->
        <div class="p-4 bg-white rounded-xl shadow-md hover:shadow-lg transition">
          <p class="text-sm text-gray-500">{{ item.fecha }}</p>
          <h3 class="text-lg font-semibold text-gray-800">{{ item.titulo }}</h3>
          <p class="text-gray-600 text-sm mt-1">{{ item.descripcion }}</p>
          <a :href="item.enlace" target="_blank"
            class="inline-block mt-2 text-blue-600 hover:text-blue-800 text-sm font-medium">
            Ver más →
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const educacion = ref([
  {
    id: 1,
    fecha: '2024',
    titulo: 'Técnico Universitario en Programación',
    descripcion:
      'Carrera orientada al desarrollo de software y fundamentos de ingeniería en sistemas.',
    enlace: '#',
  },
  {
    id: 2,
    fecha: '2023',
    titulo: 'Certificación en Redes Informáticas',
    descripcion:
      'Curso sobre configuración de redes LAN/WAN, administración de routers y protocolos TCP/IP.',
    enlace: '#',
  },
  {
    id: 3,
    fecha: '2022',
    titulo: 'Curso de Instalación y Mantenimiento de Equipos Informáticos',
    descripcion:
      'Capacitación práctica en montaje, diagnóstico y mantenimiento de hardware.',
    enlace: '#',
  },
  {
    id: 4,
    fecha: '2021',
    titulo: 'Curso de Desarrollo Web Frontend',
    descripcion:
      'Aprendizaje de HTML, CSS, JavaScript y frameworks modernos para la creación de sitios web.',
    enlace: '#',
  },
])
</script>

<style scoped>
/* Línea de tiempo vertical */
.relative::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  border-left: 2px solid #d1d5db;
  /* gris claro */
}
</style>
