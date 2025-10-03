<script setup lang="ts">

import CardTecnologia from './CardTecnologia.vue'
import springSvg from "@/assets/images/tecnologias/spring.svg";
import javaSvg from "@/assets/images/tecnologias/java.svg";
import vueSvg from "@/assets/images/tecnologias/vue.svg";
import javascriptSvg from "@/assets/images/tecnologias/javascript.svg";
import typescriptSvg from "@/assets/images/tecnologias/typescript.svg";
import gitSvg from "@/assets/images/tecnologias/git.svg";
import postmanSvg from "@/assets/images/tecnologias/postman.svg";
import postgresSvg from "@/assets/images/tecnologias/postgres.svg";
import htmlSvg from "@/assets/images/tecnologias/html.svg";
import cssSvg from "@/assets/images/tecnologias/css.svg";
import sassSvg from "@/assets/images/tecnologias/sass.svg";
import bootstrapSvg from "@/assets/images/tecnologias/bootstrap.svg";
import dockerSvg from "@/assets/images/tecnologias/docker.svg";
import pythonSvg from "@/assets/images/tecnologias/python.svg";
import golangSvg from "@/assets/images/tecnologias/golang.svg";
import { NGrid, NGi } from 'naive-ui';

</script>

<template>
  <div class="card">
    <h1>Daily Technology Use & Expertise</h1>
    <h3>Proficiency levels based on my frequent, <span class="h3CorVermelha">day-to-day</span> work.</h3>

    <n-grid class="grid" :x-gap="12" :y-gap="12" :cols="4">
      <n-gi>
        <CardTecnologia :icone="springSvg" :nivel="5" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="javaSvg" :nivel="5" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="vueSvg" :nivel="5" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="javascriptSvg" :nivel="5" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="typescriptSvg" :nivel="5" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="gitSvg" :nivel="5" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="postmanSvg" :nivel="5" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="postgresSvg" :nivel="5" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="javaSvg" :nivel="5" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="htmlSvg" :nivel="5" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="cssSvg" :nivel="5" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="sassSvg" :nivel="3" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="bootstrapSvg" :nivel="3" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="dockerSvg" :nivel="3" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="pythonSvg" :nivel="2" />
      </n-gi>
      <n-gi>
        <CardTecnologia :icone="golangSvg" :nivel="2" />
      </n-gi>
    </n-grid>
  </div>
</template>

<style scoped lang="scss">
@use '../assets/styles/variaveis';

.card {
  width: 1150px;
  padding-top: 75px;
  margin: auto;
  padding-bottom: 75px;
}

.grid{
  padding-top: 75px;
}

.h3CorVermelha{
  color: variaveis.$cor-vermelho;
}
</style>
