<script setup>
import NavBar from './components/NavBar.vue'
import DatosPersonales from './components/DatosPersonales.vue'
import EducacionTimeLine from './components/EducacionTimeLine.vue';
import ExperienciaView from './components/ExperienciaView.vue';
import ProyectoComponente from './components/ProyectoComponente.vue';
import HabilidadesComponente from './components/HabilidadesComponente.vue';
import InteresesComponente from './components/InteresesComponente.vue';
import FooterComponente from './components/FooterComponente.vue';
</script>

<template>
  <header>
    <!--Barra de navegacion-->
    <NavBar />
    <!--Componente Datos Personales-->
    <DatosPersonales />

  </header>
  <main>
    <section id="educacion">
      <h2>Educación - Cursos</h2>
      <!--Componente Educacion Time Line-->
      <EducacionTimeLine />
    </section>
    <section id="experiencia">
      <h2>Experiencia</h2>
      <!--Componente Experiencia View-->
      <ExperienciaView />
    </section>
    <section id="proyectos">
      <h2>Proyectos</h2>
      <!--Componente Proyecto Componente-->
      <ProyectoComponente />
    </section>
    <section id="habilidades">
      <h2>Habilidades</h2>
      <!--Componente Habilidades Componente-->
      <HabilidadesComponente />
    </section>
    <section id="intereses">
      <h2>Intereses</h2>
      <!--Componente Intereses Componente-->
      <InteresesComponente />
    </section>
  </main>
  <footer>
    <!--Componente Footer Componente-->
    <FooterComponente />
  </footer>
</template>

<style scoped></style>
