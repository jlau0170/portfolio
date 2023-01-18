<script setup>
import Main from './components/Main.vue'
import Experience from './components/Experience.vue'
import Projects from './components/Projects.vue'
import Me from './components/Me.vue'
import NavBar from './components/NavBar.vue'
import PageLoader from './components/PageLoader.vue'
</script>
<template>
  <PageLoader />
  <NavBar/>
  <main>
      <Main />
      <Experience />
      <Projects />
      <Me />
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  width: 104.5%;
  right: 8.4rem;
}

section {
  height: 100vh;
  width: 100%;
  margin: 0;
}

.experienceSection {
  height: 2000px;
  width: 100%;
  top: 600px;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
