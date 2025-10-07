<script setup lang="ts">
defineProps<{
  icone?: string
  nivel?: number
}>()
</script>

<template>
  <div class="container">
    <img class="image" :src="icone" />
    <div class="nivel-wrapper">
      <div class="girarInfinito" v-for="i in nivel" :key="i">⭐</div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.container {
  max-width: 150px;
}

.image {
  width: 125px;
  height: 125px;
}

.nivel-wrapper {
  padding-top: 10px;
  display: flex;
  justify-content: center;
  gap: 5px;
}
</style>
