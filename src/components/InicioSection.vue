<script setup lang="ts">

const openWhatsappChat = () =>{
  window.open('https://wa.link/5i9p32', '_blank')
}

const openGmailMessage = () => {
  window.open("mailto:pietrobragaaquino@gmail.com?subject=Portfolio%20Contact%20-%20Inquiry&body=Hello%20Piêtro.%20I%20found%20your%20work%20through%20your%20portfolio%20and%20I'm%20very%20interested%20in%20discussing%20an%20opportunity%20or%20project.%20%0AAre%20you%20available%20for%20a%20quick%20chat?", '_blank')
}

const openLinkedin = () => {
  window.open("https://www.linkedin.com/in/pietrobragaprofissional/", "_blank")
}

const openResume = () => {
  window.open("https://docs.google.com/document/d/1pRGp0hriTj0rYl7ICifWTolocdETmijHsOM91Fh4HL8/export?format=pdf", "_blank")
}

</script>

<template>
  <div class="container fadeInUp-animation" >
    <div class="card">
      <div>
        <img class="imagePietro" src="../assets/images/pietro.jpg" alt="Pietro's image" />
        <h1 >Hello, 👋 my name is <span class="nameSpan">Piêtro Braga</span></h1>
        <h1>
          And i'm a Full-stack Developer <span class="vueText">Vue.js 3</span> &
          <span class="springText">Spring Boot</span>
        </h1>
        <h3>Ready to build your next <span class="textoExtraSpan">Amazing Application.</span></h3>
        <div class="divForContact">
          <button class="buttonWhatsapp" @click="openWhatsappChat">
            Contact via WhatsApp 📞
          </button>
          <button class="buttonGmail" @click="openGmailMessage">
            Contact via Gmail ✉️
          </button>
          <button class="buttonLinkedin" @click="openLinkedin">
            Contact via Linkedin 👔
          </button>
          <button class="buttonResume" @click="openResume">
            Resume in Pdf 📄
          </button>
        </div>

      </div>
      <div class="logoContainer">
        <img class="logoVue" src="../assets/images/vue.png" alt="Logo Vuejs" />
        <img class="logoSpring" src="../assets/images/spring.png" alt="Logo Spring Boot" />
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@use '../assets/styles/variaveis';

.container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: calc(100vh - 75px);
}
.card {
  display: flex;
  align-items: center;
  justify-content: space-between;
  max-width: 1150px;
}
.logoContainer {
  display: flex;
  gap: 30px;
  margin-left: -100px;
  transform: rotate(25deg);
}
.vueText {
  color: variaveis.$cor-vue;
}
.springText {
  color: variaveis.$cor-spring;
}

.imagePietro {
  width: 250px;
  height: 250px;
  border-radius: 50%;
  object-fit: cover;
  object-position: center;
  border: 4px solid variaveis.$cor-moldura;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  margin-bottom: 20px;
}

.logoVue {
  width: 200px;
}
.logoSpring {
  width: 200px;
}

.nameSpan {
  color: variaveis.$cor-azul;
}

.textoExtraSpan {
  color: variaveis.$cor-roxa;
  border-bottom: 2px solid variaveis.$cor-roxa;
}

.divForContact{
  padding-top: 20px;
  display: flex;
  gap: 20px;
}

.buttonWhatsapp{
  background: #25D366;
}

.buttonGmail{
  background: #E94235;
}

.buttonLinkedin{
  background: #0A66C2;
}

.buttonResume{
  background: variaveis.$cor-roxa;
}
</style>
