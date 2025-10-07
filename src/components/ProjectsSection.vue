<script setup lang="ts">

import springImage from "@/assets/images/spring.png";
import vueImage from "@/assets/images/vue.png";
import htmlCssJs from "@/assets/images/htmlCssJs.png"
import CardProjeto from "./CardProjeto.vue";
import {NGrid, NGi} from 'naive-ui'

</script>

<template>
  <div class="card">
    <h1>Featured Projects</h1>
    <h3>A selection of work demonstrating my skills and <span class="h3corAzul">hands-on</span> experience.</h3>

     <n-grid class="grid" :x-gap="12" :y-gap="48" :cols="3">
      <n-gi>
        <CardProjeto :image="springImage" title="Spring Boot Clean Arch Api (JPA)" :text-list="[
           'Frameworks: Spring Boot (Java), JPA, H2 Memory Database.',
           'Architecture: Ports and Adapters (Hexagonal) Architecture, Clean Code Principles.',
           'DevOps/Data: Flyway for Database Migrations.',
           'Quality: Junit & Mockito for Unit/Integration Tests.',
           'Mappers: MapStruct for type-safe and performant data mapping.',
           'Robustness: Global Exception Handlers, Spring Validation.']"
           linkToProject="https://github.com/pietroBragaAquinoJunior/spring-boot-clean-arch-api"
            />
      </n-gi>
      <n-gi>
            <CardProjeto :image="springImage" title="Spring Boot Clean Arch Api (Mybatis)" :text-list="[
           'Frameworks: Spring Boot (Java), Mybatis, H2 Memory Database.',
           'Architecture: Ports and Adapters (Hexagonal) Architecture, Clean Code Principles.',
           'DevOps/Data: Flyway for Database Migrations.',
           'Mappers: MapStruct for type-safe and performant data mapping.',
           'Robustness: Global Exception Handlers, Spring Validation.']"
           linkToProject="https://github.com/pietroBragaAquinoJunior/spring-boot-clean-arch-mybatis-api/"
            />
      </n-gi>
       <n-gi>
        <CardProjeto
            :image="springImage"
            title="Spring Security API (JWT + RSA)"
            :text-list="[
                'Frameworks: Spring Boot (Java), JPA (Hibernate), H2 Memory Database.',
                'Architecture: Ports and Adapters (Hexagonal), Clean Code Principles.',
                'Security: JWT Authentication, RSA Keys, Spring Security 6.5.5.',
                'Mappers: MapStruct for type-safe and performant DTO / Domain / Entity mapping.',
                'Robustness: Global Exception Handlers (@RestControllerAdvice), Spring Validation.'
            ]"
            linkToProject="https://github.com/pietroBragaAquinoJunior/spring-security"
        />
      </n-gi>
      <n-gi>
            <CardProjeto :image="vueImage" title="My Personal Portfolio" :text-list="[
            'Frontend Framework: Vue.js 3 (Composition API & <script setup>).',
            'Styling: SCSS for preprocessing and extensive custom CSS.',
            'Component Library: Naive UI for specific components.',
            'Organization: Component-based architecture with data flow via Props.',
            'Build Tool: Vite for a fast development and build experience.']"
            linkToProject="https://github.com/pietroBragaAquinoJunior/my-personal-portfolio"
            />
      </n-gi>
      <n-gi>
          <CardProjeto
              :image="htmlCssJs"
              title="Public Transparency Portal"
              :text-list="[
                  'Role: Frontend Developer.',
                  'Scope: 7-month project spanning multiple thematic sections.',
                  'Design: Developed adaptive (mobile-first) layout, strictly following the design provided by the team.',
                  'Technologies: Html5, Css3 and Javascript.',
                  'Differential: Strong focus on accessibility to serve users with disabilities.'
              ]"
              linkToProject="https://www.transparencia.ma.gov.br/"
          />
      </n-gi>
    </n-grid>



  </div>
</template>

<style scoped lang="scss">
@use '../assets/styles/variaveis';

.card {
  width: 1150px;
  padding-top: 75px;
  padding-bottom: 75px;
  margin: auto;
}

.h3corAzul{
  color: variaveis.$cor-azul;
}

.grid{
  margin-top: 75px;
}
</style>
