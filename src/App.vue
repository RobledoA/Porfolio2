<template>
  <v-app>
    <v-main>
      <Header></Header>
      <v-container class="Abouts">
        <AboutMe></AboutMe>
      </v-container>
      <v-container>
        <Projects></Projects>
      </v-container>

      <v-container>
        <Skills></Skills>
      </v-container>
    </v-main>
  </v-app>
  <AppFooter></AppFooter>
</template>

<script setup>

import AboutMe from './components/AboutMe.vue';
import AppFooter from './components/AppFooter.vue';
import Header from './components/Header.vue';
import Projects from './components/Projects.vue';
import Skills from './components/Skills.vue';

  //
</script>

<style scoped>


</style>