<template>
  <div class="timeline-container">
    <div class="timeline">
      <div v-for="(item, index) in timeline" :key="index" class="timeline-item">
        <!-- Línea entre puntos -->
        <div v-if="index < timeline.length - 1" class="timeline-line"></div>

        <!-- Punto -->
        <div class="timeline-dot"></div>

        <!-- Tarjeta -->
        <div class="timeline-content">
          <h3 class="timeline-periodo">{{ item.periodo }}</h3>
          <h4 class="timeline-titulo">{{ item.titulo }}</h4>
          <p class="timeline-descripcion">{{ item.descripcion }}</p>
          <p class="timeline-descripcion2">{{ item.descripcion2 }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const timeline = [
  {
    periodo: "2008 - 2015",
    titulo: "Empresa familiar",
    descripcion: "Electricidad domiciliaria e industrial:",
    descripcion2: "Instalaciones electricas domiciliarias, armado de tableros, mantenimiento industrial",
  },
  {
    periodo: "2013 - Actualmente",
    titulo: "Hospital Grl. Las Heras",
    descripcion: "IT Servicio Informático:",
    descripcion2: "Soporte técnico, mantenimiento de hardware y software, gestión de redes.",
  },
  {
    periodo: "2013 - Actualmente",
    titulo: "AEM Informática",
    descripcion: "IT - CCTV - Alarmas:",
    descripcion2: "Instalación y mantenimiento de cámaras de vigilancia, alarmas, control de accesos, redes y soporte IT.",
  },

];
</script>

<style scoped>
/* Contenedor general */
.timeline-container {
  /* min-height: 100vh; */
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2rem;
  overflow-x: auto;
}

/* Línea de tiempo horizontal*/
.timeline {
  display: flex;
  align-items: center;
  position: relative;
  gap: 4rem;
}

/* Cada ítem */
.timeline-item {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* Punto naranja/blanco
.timeline-dot {
  width: 18px;
  height: 18px;
  background-color: #111;
  border: 4px solid #ff4500;
  border-radius: 50%;
  z-index: 2;
}*/

/* Tarjetas */
.timeline-content {
  background-color: #1f1f1f;
  color: #eee;
  padding: 1rem;
  border-radius: 12px;
  margin-top: 1rem;
  min-width: 250px;
  text-align: center;
  box-shadow: 0 0 10px rgba(255, 69, 0, 0.3);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.timeline-content:hover {
  transform: scale(1.05);
  box-shadow: 0 0 15px rgba(255, 69, 0, 0.6);
}

/* Estilos del texto */
.timeline-periodo {
  color: #ff6600;
  font-weight: bold;
  margin-bottom: 0.3rem;
}

.timeline-titulo {
  color: #fff;
  font-size: 1rem;
  font-weight: 600;
  margin-bottom: 0.4rem;
}

.timeline-descripcion {
  font-size: 0.9rem;
  color: #ccc;
  line-height: 1.3;
}

.timeline-descripcion2 {
  font-size: 0.9rem;
  color: #ccc;
  line-height: 1.3;
}
</style>
