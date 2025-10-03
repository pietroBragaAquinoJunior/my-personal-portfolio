<script setup lang="ts">
const openTceLink = () => {
  window.open('https://www.tcema.tc.br/', '_blank')
}
const openTransparenciaPortalLink = () => {
  window.open('https://www.transparencia.ma.gov.br/', '_blank')
}
</script>

<template>
  <div class="container">
    <div class="card">
      <h1 class="h1Diferente">💼 Systems Development Supervisor (09/2022 to Current)</h1>
      <h3 class="h3ComBorda">
        Court of Accounts of the State of Maranhão - São Luís, Maranhão, Brazil
      </h3>
      <ul>
        <li>
          🔗 Interoperability: Integrated APIs and third-party services to successfully expand the
          core functionality of web platforms.
        </li>
        <li>
          💻 Back-end Development: Developed and maintained robust APIs using the Java framework to
          ensure efficient and reliable data exchange between applications.
        </li>
        <li>
          🌐 Front-end Implementation: Developed and maintained internal web applications utilizing
          the Vue.js 3 framework, to significantly enhance the overall user experience (UX) and
          system efficiency.
        </li>
        <li>
          🧠 Team Mentorship: Mentored junior developers, actively fostering skill development and
          promoting knowledge sharing across the development team.
        </li>
        <li>
          📚 Continuous Learning: Participated in specialized training sessions to master Ports and
          Adapters Architecture, Spring Boot, and Artificial Intelligence.
        </li>
        <li>
          🤖 Automation & AI: Applied Artificial Intelligence principles to software development
          processes by utilizing n8n workflow automation tools.
        </li>
        <li>
          🔒 Critical System Portfolio: Developed and maintained highly sensitive internal
          platforms, including systems for:
        </li>
        <ul style="margin-left: 40px">
          <li>Payroll and Fiscal Data Collection (from entities and municipalities).</li>
          <li>Internal Server Performance Measurement and assessment.</li>
          <li>Specialized Audit and Financial Oversight applications.</li>
        </ul>
      </ul>
      <div class="divForButton">
        <button class="buttonVermelho" @click="openTceLink">
          Visit the Official Institution Website 🏢
        </button>
      </div>
    </div>

     <div class="card">
      <h1 class="h1CorAzul">💻 Front-End Developer (01/2022 to 09/2022)</h1>
      <h3 class="h3ComBorda">
        State Secretariat for Transparency and Control of Maranhão (SETC) - São Luís, Maranhão, Brazil
      </h3>
      <ul>
        <li>
          ✅ Integral participation in the creation of a public website focused on transparency for consulting government information.
        </li>
        <li>
          ♿ Strong focus on Accessibility (WCAG), ensuring the public portal was usable by all citizens, in alignment with public service guidelines.
        </li>
        <li>
          🎨 Development of custom UI/UX components from scratch using plain HTML, CSS, and JavaScript, resulting in a unique and high-performance interface.
        </li>
        <li>
          📱 Created responsive web applications (mobile-first approach) optimized for performance and usability across various devices.
        </li>
        <li>
          🌐 Ensured cross-browser compatibility through rigorous testing, providing a consistent user experience on all platforms.
        </li>
        <li>
          ⚙️ Utilized Git for version control, efficient source code management, and streamlined team collaboration.
        </li>
      </ul>
      <div class="divForButton">
        <button class="buttonAzul" @click="openTransparenciaPortalLink">
          Access the Public Transparency Portal 🔎
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@use '../assets/styles/variaveis';

.container {
  padding-bottom: 100px;
  display: flex;
  align-items: center;
  flex-direction: column;
  background: variaveis.$cor-fundo-escuro;
  min-height: calc(100vh - 75px);
}
.card {
  width: 1150px;
  padding-top: 75px;
}
.h1Diferente {
  color: variaveis.$cor-vermelho;
  padding-bottom: 10px;
}
.h1CorAzul{
  color: variaveis.$cor-azul;
  padding-bottom: 10px;
}
.h3ComBorda {
  border-top: 1px dashed variaveis.$cor-cinza;
  padding-top: 10px;
}

ul li {
  margin-top: 20px;
}
.divForButton {
  padding-top: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.buttonVermelho{
  background: variaveis.$cor-vermelho;
}
.buttonAzul{
  background: variaveis.$cor-azul;
}
</style>
