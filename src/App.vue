<script setup>
import { ref, onMounted } from 'vue'

const animClass = ref('wtf')

onMounted(() => {
  setTimeout(function () {
    animClass.value = "hide";
    console.log("WELCOME: Carolingian Royalty Registery")
  }, 5000);
})

</script>

<template>

<div class="page">
  <div class="foo">
    <img alt="logo" class="responsive" src="./assets/NPPA_logo.svg" />
  </div>
  <div class="verificaiton">
    (( VERIFICATION from QR code | mobile ))
  </div>


  <div>
    <img alt="Lord Kai C. Bellina" src="./assets/kai.png" width="225" />
  </div>

  <div class="container">
    <div />

    <div>
      <div><span class="labels">Name:</span> <span>Kai Christopher Bellina</span></div>
      <div><span class="labels">ID:</span> <span> 21668683768290</span></div>
      <div><span class="labels">EXP:</span> <span>1/12/2024</span></div>
    </div>
    <div />
  </div>

  <footer class="footer">
    <div>
      public | view record: As3908817283
    </div>
  </footer>

</div>


  <!-- <div :class="animClass">
    <div>
      <div class="logo_container">
        <img alt="flag" class="logo" src="./assets/vegitable_lamb.svg" />
      </div>
    </div>
  </div> -->

</template>


<style scoped>
.page{
  display: flex;
}
  .labels{
    font-weight: 800;
  }
.container {
  display: grid;
  grid-template-columns: 10% 1fr 10%;
}

.foo {
  display: flex;
}

.verificaiton {
  text-align: center;
  color: black;
  background-color: #9F8C8C;
}

body {
  margin: 0;
}

.footer {
  text-align: center;
  display: grid;
  grid-template-columns: 1fr;
  width: 100%;
  color: rgb(146, 146, 136);
  height: 60px;
}

.wtf {
  width: 100%;
  height: 100vh;
  top: 0;
  left: 0;
  position: fixed;
  display: flex;
}

.wtf div {
  width: 100%;
  height: 100%;
  background: rgb(21, 10, 10);
  animation: up 5s ease-in forwards;
  transform: scaleY(0);
  /* background: rgb(211, 34, 3); */
}

@keyframes up {

  100% {
    transform-origin: top;
    /* transform: scaleY(0);*/
    transform: translateY(100%);
  }

  0% {
    transform-origin: bottom;
    /* transform: scaleY(1); */
    transform: translateY(-0%);
  }
}

.hide {
  visibility: hidden;
}
</style>