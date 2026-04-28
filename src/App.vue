<script setup lang="ts">
import Home from '@/components/Home.vue';
import Hero from './components/Hero.vue';
import Home_Section from './components/Home_Section.vue';
import Home_Sectiontwo from './components/Home_Sectiontwo.vue';
import Home_Section3 from './components/Home_Section3.vue';
</script>

<template>
  <main>
     <Home/>
     <Hero/>
     <Home_Section/>
     <Home_Sectiontwo/>
     <Home_Section3/>
  </main>
</template>

<style >
/* Global Reset - Side gap aur default margins khatam karne ke liye */

html, body {
  width: 100%;
  min-height: 100vh;
  margin: 0;
  overflow-x: hidden;
}

#app {
  width: 100%;
  max-width: 1800px;
  min-height: 100vh;
  margin: 0 auto;
  padding: 0px;

  display: flex;
  flex-direction: column;
}
</style>
