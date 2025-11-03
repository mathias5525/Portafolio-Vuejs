<template>
  <section class="projects-section">
    <h2 class="projects-title">Mis proyectos más importantes</h2>
    <p class="projects-subtitle">
      Aquí hay algunos proyectos de diseño pasados en los que he trabajado.
      ¿Quieres ver más? <a href="mailto:contacto.aminformatica@gmail.com">Envíame un correo.</a>
    </p>

    <div class="projects-grid">
      <div v-for="(project, index) in projects" :key="index" class="project-card" :style="{ background: project.bg }">
        <div class="project-content">
          <h3 class="project-title">{{ project.title }}</h3>
          <p class="project-desc">{{ project.description }}</p>
          <a :href="project.link" target="_blank" class="project-btn">
            Visit Website →
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    title: "Portafolio Web.",
    description: "Portafolio personal desarrollado con HTML y CSS.",
    bg: "linear-gradient(135deg, #0b0b2c, #141446)",
    link: "https://github.com/mathias5525/Portafolio_web.git",
  },
  {
    title: "Portafolio Web.",
    description: "Portafolio HTML, CSS del Grupo Escuadrón Lobo.",
    bg: "linear-gradient(135deg, #00b3b3, #008c8c)",
    link: "https://github.com/mathias5525/Portafolio-Grupo-Escuadron-Lobo.git",
  },
  {
    title: "Repositorio de GitHub.",
    description: "Repositorio de prueba para inicio: uso de Git y GitHub.",
    bg: "linear-gradient(135deg, #4a00e0, #8e2de2)",
    link: "https://github.com/mathias5525/Prueba-Inicio.Repo.git",
  },
];
</script>

<style scoped>
/* 🎨 Fondo general */
.projects-section {

  color: #eee;
  text-align: center;
  padding: 4rem 2rem;
}

/* 🏷️ Título */
.projects-title {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
  color: #fff;
}

/* ✉️ Subtítulo */
.projects-subtitle {
  color: #ccc;
  margin-bottom: 3rem;
  font-size: 1rem;
}

.projects-subtitle a {
  color: #00b3ff;
  text-decoration: none;
  font-weight: 500;
}

.projects-subtitle a:hover {
  text-decoration: underline;
}

/* 📦 Contenedor de tarjetas */
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  justify-content: center;
  align-items: stretch;
  max-width: 1100px;
  margin: 0 auto;
}

/* 🧱 Tarjetas individuales */
.project-card {
  border-radius: 16px;
  padding: 2rem;
  color: #fff;
  display: flex;
  align-items: flex-end;
  height: 220px;
  transition: transform 0.4s ease, box-shadow 0.4s ease;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
}

.project-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 6px 25px rgba(255, 255, 255, 0.2);
}

/* 📋 Contenido de las tarjetas */
.project-content {
  text-align: left;
}

.project-title {
  font-size: 1.1rem;
  font-weight: 700;
  margin-bottom: 0.3rem;
}

.project-desc {
  font-size: 0.9rem;
  color: #ddd;
  margin-bottom: 1.2rem;
}

/* 🔘 Botón */
.project-btn {
  display: inline-block;
  background-color: rgba(255, 255, 255, 0.1);
  border: 1px solid #fff;
  padding: 0.5rem 1rem;
  border-radius: 999px;
  color: #fff;
  text-decoration: none;
  font-size: 0.9rem;
  transition: all 0.3s ease;
}

.project-btn:hover {
  background-color: #fff;
  color: #000;
}
</style>
