<template>
  <div class="center">
  <div class="container" :style="{
    scale: scaleNav,
    translate: translateNav
  }">
    <ul class="nav-ul">
      <li class="logo-li"><img src="../assets/logo.svg" alt="" class="logo">GBank</li>
      <div class="content-li">
        <span>Why Us</span>
        <span>Services</span>
        <span>Our Process</span>
        <span>Payments</span>
        <span>FAQs</span>
      </div>
      <li class="contact-li"><button class="btn-contact">
        Contact
      </button></li>
    </ul> 
  </div>
  </div>
  
</template>

<script setup>
import { onMounted, ref } from 'vue';

const scaleNav = ref(0.5);
const translateNav = ref('0px -75px');

onMounted(() => {
  setTimeout(() => {
    translateNav.value = '0px 0px'
  }, 100);
  setTimeout(() => {
    scaleNav.value = 1
  }, 300);
})
</script>
<style scoped>
@keyframes animatenav {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
.container {
  padding-top: 32px;
  width: 100%;
  max-width: 1440px;
  display: flex;
  justify-content: center;
  animation: animatenav 2s ease;
  transition: 1s ease;
}
.logo {
  width: 24px;
}
.center {
  width: 100%;
  display: flex;
  justify-content: center;
}
.logo-li {
  display: flex;
  gap: 10px;
  font-weight: bold;
  font-size: 20px;
  line-height: 24px;
  align-items: center;
  letter-spacing: -3%;
  color: white;
}
.nav-ul {
  width: 90%;
  display: flex;
  justify-content: space-between;
}
.btn-contact {
  background-color: transparent;
  padding: 12px 32px;
  border-radius: 64px;
  border: 2px solid #2BB32A;
  color: #2BB32A;
  font-weight: bold;
  font-size: 16px;
  line-height: 24px;
  letter-spacing: 0%;
  cursor: pointer;
  transition: all 0.3s ease;
  filter: drop-shadow(0px 4px 4px 0px rgb(0,0,0,25));
}
.btn-contact:active {
  background-color: #2BB32A;
  color: white;
}
.dora {
  width: 492px;
  height: 492px;
  background-color: #2BB32A;
  border-radius: 100%;
  filter: blur(200px);
}
.one {
  position: absolute;
  right: 236px;
  top: -336px;
}
li {
  color: white;
  display: flex;
  align-items: center;
}
.content-li {
  display: flex;
  width: 100%;
  max-width: 462px;
  gap: 30px;
  color: white;
  align-items: center;
}
@media(max-width:820px) {
  .content-li {
    display: none;
  }
}
</style>
