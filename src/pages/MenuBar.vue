<script setup lang="ts">
import GridTecnologies from '@/components/GridTecnologies.vue'
import InicioSection from '@/components/InicioSection.vue'
import { computed, onMounted, onUnmounted, ref } from 'vue'
import ProjectsSection from '@/components/ProjectsSection.vue'
import ExperienceSection from '@/components/ExperienceSection.vue'
import MyCertificates from '@/components/MyCertificates.vue'

const scrollNaPosicaoInicial = ref(true)

const flutuando = computed(() => {
  return !scrollNaPosicaoInicial.value
})

const handleScroll = () => {
  scrollNaPosicaoInicial.value = window.scrollY < 10
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <div class="divMenu" :class="{ flutuante: flutuando }">
    <nav>
      <a href="#inicio">Home</a>
      <a href="#experience">Experience</a>
      <a href="#tecnologies">Tecnologies</a>
      <a href="#projects">Featured Projects</a>
      <a href="#minorProjects">Smaller projects</a>
      <a href="#certificates">Certificates</a>
    </nav>
  </div>
  <div :class="{ substituto: flutuando }"></div>
  <div>
    <section class="section" id="inicio">
      <InicioSection />
    </section>
    <section class="section" id="experience">
      <ExperienceSection />
    </section>
    <section class="section" id="tecnologies">
      <GridTecnologies />
    </section>
    <section class="section cor-preta" id="projects">
      <ProjectsSection />
    </section>
    <section class="section" id="certificates">
      <MyCertificates />
    </section>
  </div>
</template>

<style scoped lang="scss">
@use '../assets/styles/variaveis';

.substituto {
  height: 75px;
}

.divMenu {
  height: 75px;
  display: flex;
  justify-content: end;
  align-items: center;
  padding-right: 100px;
  &.flutuante {
    position: fixed;
    width: 100%;
    background: variaveis.$cor-fundo-escuro;
    z-index: 999;
  }
}

nav {
  gap: 30px;
  display: flex;
}

.section {
  scroll-margin-top: 75px;
}

.cor-preta {
  background: variaveis.$cor-fundo-escuro;
}
</style>
