<script setup lang="ts">
const props = defineProps<{
  image?: string
  title?: string
  subtitle?: string
  linkToProject?: string
}>()

const handleClick = () => {
  window.open(props.linkToProject, '_blank')
}
</script>

<template>
  <div class="container" @click="handleClick">
    <img class="image" :src="image" />
    <div class="titleAndSubtitle">
      <p class="title">{{ title }}</p>
      <p class="subtitle">{{ subtitle }}</p>
    </div>
  </div>
</template>

<style scoped lang="scss">
@use '../assets/styles/variaveis';

.container {
  max-width: 350px;
  border-radius: 5px;
  padding: 10px;
  min-height: 100px;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
  &:hover {
    background-color: variaveis.$cor-fundo-principal;
  }
}

.image {
  width: 50px;
  height: 50px;
  border-radius: 50%;
}

.title{
  font-size: 1rem;
}

.titleAndSubtitle{
  display: flex;
  flex-direction: column;
  align-items: start;
  justify-content: center;
}

.subtitle{
  font-size: 12px;
  font-style: italic;
}
</style>
