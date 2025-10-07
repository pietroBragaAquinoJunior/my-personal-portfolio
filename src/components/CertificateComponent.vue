<script setup lang="ts">
defineProps<{
  image?: string
  url?: string
  credential?: string
}>()
</script>

<template>
  <div class="container">
    <img class="image" :src="image" />
  </div>
  <div class="urlECredencial">
    <a class="link" target="_blank" :href="url">Click here to Verify</a>
    <p>Credential Code: {{ credential }}</p>
  </div>
</template>

<style scoped lang="scss">
@use '../assets/styles/variaveis';

.container {
  max-width: 150px;
}

.image {
  width: 400px;
  height: 300px;
  border-radius: 15px;
}

.nivel-wrapper {
  padding-top: 10px;
  display: flex;
  justify-content: center;
  gap: 5px;
}
.link {
  cursor: pointer;
  color: variaveis.$cor-roxa;
}
</style>
