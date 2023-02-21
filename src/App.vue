<template>
  <div>
    <div ref="lottieEle"></div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import lottie from 'lottie-web';

const lottieEle = ref();

onMounted(() => {
  lottie.loadAnimation({
    container: lottieEle.value, // the dom element that will contain the animation
    renderer: 'canvas',
    loop: true,
    autoplay: true,
    path: 'https://assets10.lottiefiles.com/packages/lf20_lS88YC8r3Y.json' // the path to the animation json
  });
});
</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
