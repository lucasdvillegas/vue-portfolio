<template>


  <HeaderView />
  <NavBar />
  <!-- <HeaderView />
  <AboutmeView /> -->
  <ParticlesC />
</template>

<script>
import ParticlesC from './components/ParticlesC.vue'
import NavBar from './components/NavBar.vue';
import HeaderView from './views/HeaderView.vue';
// import AboutmeView from './views/AboutmeView.vue';

export default {
  name: 'App',
  components: {
    ParticlesC,
    NavBar,
    HeaderView,
    // AboutmeView
  }
}
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto+Condensed:wght@400;700&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");
:root {
  --primary-color: #0a0a0a;
  --secondary-color: #ffa700;
  --tertiary-color: #f5f5f5;

  --tertiary-font: "Roboto Condensed", sans-serif;
  --secondary-font: "Roboto", sans-serif;
  --primary-font: "Roboto Condensed", sans-serif;

  --icon-fontSize: 30px;
}

::-webkit-scrollbar {
    width: 12px;
}

::-webkit-scrollbar-thumb {
    background: var(--secondary-color);
}

::-webkit-scrollbar:hover {
    filter: blur(45px);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
  
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
  padding: 0;
  box-sizing: none;
}

</style>
