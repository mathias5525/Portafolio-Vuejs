<script setup>
import linkedin from '/src/assets/linkedin_icon.svg'
import instagram from '/src/assets/instagram_icon.svg'
import github from '/src/assets/github_icon.svg'
import email from '/src/assets/email_icon.svg'
import whatsapp from '/src/assets/whatsapp_icon.svg'
import cv from '/src/assets/cv_resume_icon.svg'

const title = 'Matias Altamiranda - Portafolio'
const descripcion = 'Técnico Universitario en Programación - UTN'
const residencia = 'Tupungato, Mendoza, Argentina'
const presentacion =
  'Hola, Bienvenido a mi portafolio de proyectos. Soy un un tecnico IT con experiencia en el desarrollo de aplicaciones web y móviles.'
const redesSociales = [
  {
    id: 1,
    name: 'linkedin',
    src: linkedin,
    url: 'https://www.linkedin.com/in/matias-altamiranda-1a9609b4/?originalSubdomain=arhttps://www.instagram.com/matti_altamiranda/?igsh=czY4cGNvcjJqaTZ0&utm_source=qr#',
  },
  { id: 2, name: 'Instagram', src: instagram, url: 'https://www.instagram.com/matti_altamiranda/' },
  { id: 3, name: 'github', src: github, url: 'https://github.com/mathias5525' },
  { id: 4, name: 'email', src: email, url: 'mailto:matiasemanuel25@gmail.com' },
  {
    id: 5,
    name: 'whatsapp',
    src: whatsapp,
    url: 'https://wa.me/+5492622437320?text=Hola%20Matias%2C%20te%20contacto%20desde%20tu%20portafolio.',
  },
  { id: 6, name: 'curriculum', src: cv, url: 'https://drive.google.com/file/d/1mb_mcjx145ahoz31fUnQ8H-HgvUAL-H-/view?usp=sharing' },
]
const telefono = '+54 9 2622-437320'
</script>

<template>
  <section class="datos-personales">
    <div class="card">
      <h1>{{ title }}</h1>
      <h2>{{ descripcion }}</h2>
      <p>{{ presentacion }}</p>
      <ul class="container-lista">
        <li v-for="red in redesSociales" :key="red.id">
          <a :href="red.url"><img class="icon-redsocial" :src="red.src" width="35rem" :alt="red.name" /></a>
        </li>
      </ul>
      <h3>Mi Telefono personal: {{ telefono }}</h3>
      <h4>{{ residencia }}</h4>
    </div>
  </section>
</template>

<style scoped>
h1 {
  font-size: 2.5rem;
}

p {
  font-size: 1.2rem;
  font-weight: 600;
  margin-bottom: 1rem;
}

.card {
  background-color: rgb(28, 41, 52);
  border-radius: 10px;
  padding: 10px;
  margin: 10px;
  text-align: center;
}

.container-lista {
  display: flex;
  justify-content: center;
  list-style: none;
  padding: 0;
  margin: 0;
  text-align: center;
}

.icon-redsocial {
  align-items: center;
  background-color: aliceblue;
  border-radius: 50%;
  padding: 2px;
  margin: 5px;
  box-shadow: 0 0 5px rgba(95, 124, 205, 0.934);
}

.icon-redsocial:hover {
  background-color: rgb(28, 41, 52);
  box-shadow: 0 0 5px rgba(255, 255, 255, 0.934);
}

h3 {
  font-size: 1.2rem;
  font-weight: 600;
}

h4 {
  font-size: 1rem;
  font-weight: 400;
}
</style>
