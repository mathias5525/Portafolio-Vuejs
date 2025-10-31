<template>
  <section class="skills-section">

    <div class="skills-grid">
      <div v-for="(skill, index) in skills" :key="index" class="skill-card">
        <img :src="skill.icon" :alt="skill.name" class="skill-icon" />
        <p class="skill-name">{{ skill.name }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
const skills = [
  {
    name: "HTML 5",
    icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg",
  },
  {
    name: "CSS 3",
    icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg",
  },
  {
    name: "JavaScript",
    icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg",
  },
  {
    name: "Python",
    icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg",
  },
  {
    name: "Java",
    icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg",
  },
  {
    name: "Git",
    icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg",
  },
  {
    name: "Github",
    icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg",
  },
  {
    name: "Trello",
    icon: "https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/trello.svg",
  },
];
</script>

<style scoped>
.skills-section {
  color: #fff;
  padding: 4rem 2rem;
  text-align: center;
}

.skills-title {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 2rem;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
  gap: 1.5rem;
  justify-items: center;
  align-items: center;
  max-width: 700px;
  margin: 0 auto;
}

.skill-card {
  background-color: #292626;
  border-radius: 16px;
  padding: 1.5rem;
  width: 120px;
  height: 120px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  cursor: default;
}

.skill-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 4px 20px rgba(255, 255, 255, 0.15);
}

.skill-icon {
  width: 48px;
  height: 48px;
  margin-bottom: 0.8rem;
  object-fit: contain;
  filter: drop-shadow(0 0 2px rgba(255, 255, 255, 0.1));
}

.skill-name {
  font-size: 0.9rem;
  font-weight: 500;
  color: #eee;
}
</style>
