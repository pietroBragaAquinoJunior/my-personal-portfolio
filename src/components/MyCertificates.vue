<script setup lang="ts">

import { NGrid, NGi } from 'naive-ui';
import CertificateComponent from './CertificateComponent.vue';
import decoderCertificate from "@/assets/images/decoderCertificate.jpg";
import javaCertificate from "@/assets/images/javaCertificate.png";
import htmllCssCertificate from "@/assets/images/htmllCssCertificate.jpg";
import databaseCertificate from "@/assets/images/databaseCertificate.jpg";
import githubCertificate from "@/assets/images/githubCertificate.jpg";
import javascriptCertificate from "@/assets/images/javascriptCertificate.jpg";
</script>

<template>
  <div class="card">
    <h1>Certificates & Courses</h1>
    <h3>My most impactful learning experience was the Decoder Project with <a href="https://mvp.microsoft.com/it-IT/mvp/profile/981d237a-ed9f-ea11-a811-000d3a8ccaf5" target="_blank"><span class="h3CorVermelha">Michelli Britto</span></a>, Microsoft MVP, where I deepened my skills in Java and real-world development.</h3>

    <n-grid class="grid" :x-gap="12" :y-gap="12" :cols="2">
      <n-gi>
        <CertificateComponent :image="decoderCertificate" url="https://e-certificado.com/login/autenticar" credential="1763692A8150F7A011679540" />
      </n-gi>
      <n-gi>
        <CertificateComponent :image="javaCertificate" url="https://www.udemy.com/certificate/UC-b0db20f5-438e-435a-8d3d-090afff20d64/" credential="UC-b0db20f5-438e-435a-8d3d-090afff20d64" />
      </n-gi>
      <n-gi>
        <CertificateComponent :image="htmllCssCertificate" url="https://www.b7web.com.br/certificado/" credential="492620" />
      </n-gi>
      <n-gi>
        <CertificateComponent :image="databaseCertificate" url="https://www.b7web.com.br/certificado/" credential="4529178" />
      </n-gi>
      <n-gi>
        <CertificateComponent :image="githubCertificate" url="https://www.b7web.com.br/certificado/" credential="4725776" />
      </n-gi>
      <n-gi>
        <CertificateComponent :image="javascriptCertificate" url="https://www.b7web.com.br/certificado/" credential="8244144"/>
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
  color: variaveis.$cor-roxa;
}
</style>
