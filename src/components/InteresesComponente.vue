<template>
  <section class="intereses-section">
    <!-- Fondo animado SVG -->
    <svg class="curved-bg" viewBox="0 0 1000 400" preserveAspectRatio="none">
      <defs>
        <!-- Gradiente -->
        <linearGradient id="curveGradient" x1="0" y1="0" x2="1" y2="1">
          <stop offset="0%" stop-color="#ff0057" />
          <stop offset="100%" stop-color="#ff6600" />
        </linearGradient>
      </defs>

      <!-- Líneas curvas animadas -->
      <path v-for="(wave, i) in waves" :key="i" :d="wave.d" fill="none" stroke="url(#curveGradient)" stroke-width="2"
        stroke-linecap="round">
        <animate attributeName="d" :values="wave.values" dur="8s" :begin="`${i * 1.2}s`" repeatCount="indefinite" />
      </path>

      <!-- Puntos animados -->
      <g>
        <circle v-for="(dot, i) in dots" :key="i" :cx="dot.x" :cy="dot.y" :r="dot.r" fill="#ff6600" opacity="0.8">
          <animate attributeName="r" values="6;10;6" dur="2.8s" :begin="`${i * 0.6}s`" repeatCount="indefinite" />
          <animate attributeName="fill" values="#ff6600;#ff0057;#ff6600" dur="3.5s" :begin="`${i * 0.4}s`"
            repeatCount="indefinite" />
        </circle>
      </g>
    </svg>

    <!-- Contenido principal -->
    <div class="intereses-content">
      <p>
        Me interesa la tecnología aplicada a la eficiencia y la innovación.
        Sigo de cerca las tendencias en software, inteligencia artificial y
        automatización, y me gusta experimentar con herramientas digitales que
        optimicen procesos y potencien la creatividad. En mi tiempo libre, disfruto
        explorar nuevas formas en que la tecnología puede mejorar la calidad de vida
        y fomentar el aprendizaje continuo.
      </p>
    </div>
  </section>
</template>

<script setup>
// Líneas curvas animadas (ondas suaves)
const waves = [
  {
    d: "M0,100 Q250,80 500,100 T1000,100",
    values: `
      M0,100 Q250,80 500,100 T1000,100;
      M0,90 Q250,120 500,80 T1000,110;
      M0,100 Q250,80 500,100 T1000,100
    `,
  },
  {
    d: "M0,200 Q300,230 600,200 T1000,210",
    values: `
      M0,200 Q300,230 600,200 T1000,210;
      M0,210 Q300,180 600,220 T1000,200;
      M0,200 Q300,230 600,200 T1000,210
    `,
  },
  {
    d: "M0,300 Q200,320 400,300 T800,320 T1000,300",
    values: `
      M0,300 Q200,320 400,300 T800,320 T1000,300;
      M0,310 Q200,290 400,310 T800,290 T1000,310;
      M0,300 Q200,320 400,300 T800,320 T1000,300
    `,
  },
];

// Puntos pulsantes alternados
const dots = [
  { x: 120, y: 120, r: 8 },
  { x: 350, y: 180, r: 10 },
  { x: 600, y: 260, r: 7 },
  { x: 850, y: 140, r: 9 },
  { x: 950, y: 300, r: 11 },
];
</script>

<style scoped>
.intereses-section {
  position: relative;
  min-height: 80vh;
  overflow: hidden;
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 4rem 2rem;
}

/* Fondo SVG animado */
.curved-bg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  opacity: 0.25;
  z-index: 0;
  pointer-events: none;
}

/* Contenido principal */
.intereses-content {
  position: relative;
  z-index: 2;
  max-width: 700px;
  backdrop-filter: blur(3px);
}

.intereses-content p {
  font-size: 1.1rem;
  color: #ddd;
  line-height: 1.6;
}
</style>
