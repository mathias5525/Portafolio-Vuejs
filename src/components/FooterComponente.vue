<template>
  <footer>
    <div class="footer-content">
      <svg class="footer-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor"
        stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2h-4a2 2 0 0 1-2-2V12H9v8a2 2 0 0 1-2 2H3z" />
      </svg>
      <a href="#top">Inicio</a>
    </div>
    <p>© 2025 Matías Altamiranda - Portafolio Vue </p>
  </footer>
</template>

<style scoped>
footer {
  text-align: center;
  padding: 1rem;
  font-size: medium;
  color: #98938f;
  margin-top: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.3rem;
}

.footer-content {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-weight: 500;
  color: #fff;
}

.footer-icon {
  width: 18px;
  height: 18px;
  color: #ff6600;
  transition: transform 0.3s ease, color 0.3s ease;
}

.footer-content:hover .footer-icon {
  transform: rotate(15deg) scale(1.1);
  color: #ff4500;
}
</style>
