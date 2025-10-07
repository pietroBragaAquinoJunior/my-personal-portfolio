<script setup lang="ts">
const props = defineProps<{
  image?: string
  title?: string
  textList?: Array<string>
  linkToProject?: string
}>()

const handleClick = () => {
  window.open(props.linkToProject, '_blank')
}
</script>

<template>
  <div class="container" @click="handleClick">
    <div class="imageDiv">
      <img class="image" :src="image" />
    </div>

    <div class="contentDiv">
      <h3>{{ title }}</h3>
      <ul>
        <li v-for="(value, index) in textList" :key="index">
          {{ value }}
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped lang="scss">
@use '../assets/styles/variaveis';

.container {
  max-width: 350px;
  border: 2px dashed variaveis.$cor-fundo-escuro;
  height: 450px;
  border-radius: 15px;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  background: variaveis.$cor-fundo-principal;
  cursor: pointer;
  position: relative;

  .imageDiv {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    opacity: 1;
    transition: opacity 0.5s ease-in-out;
    position: absolute;
  }
  .image {
    width: 200px;
  }

  .contentDiv {
    padding: 25px;
    display: flex;
    flex-direction: column;
    align-items: start;
    transition: opacity 0.5s ease-in-out;
    opacity: 0;
  }

  &:hover {
    background-color: rgba(0, 0, 0, 0.3);

    .imageDiv {
      opacity: 0;
    }
    .contentDiv {
      opacity: 1;
    }
  }

  li {
    font-size: 14px;
    padding-top: 7px;
  }
}
</style>
