<template lang="">
  <nav class="max-md:hidden md:block">
    <ul>
      <li class="home">
        <a href="#home" alt="home"> INICIO </a>
      </li>
      <li class="about">
        <a href="#about" alt="about-me"> SOBRE MI </a>
      </li>
      <li class="project">
        <a href="#project" alt="project"> PROYECTOS </a>
      </li>
      <li class="contact"><a href="#contact" alt="contact">CONTACTO</a></li>
    </ul>
  </nav>


  <nav class="md:hidden">
    <ul class="fixed bottom-0 left-0 right-0 z-10">
      <li>
        <a href="#home" alt="home">
          <i class="las la-home"></i>
        </a>
      </li>

      <li><a href="#about" alt="about-me"><i class="las la-user"></i></a></li>

      <li><a href="#project" alt="project"><i class="las la-briefcase"></i></a></li>

      <li><a href="#contact" alt="contact"><i class="las la-envelope"></i></a></li>
    </ul>
  </nav>

  <main>
    <!-- <HeaderView  user="user"/> -->
    <AboutmeView class="mt-20" id="about" />
    <ProjectView class="mt-20" id="project"/>
  </main>
</template>
<script>
// import HeaderView from "./../views/HeaderView.vue";
import AboutmeView from "./../views/AboutmeView.vue";
import ProjectView from "./../views/ProjectView.vue";

export default {
  components: {
    // HeaderView,
    AboutmeView,
    ProjectView,
  },
};
</script>
<style>
nav {
  box-sizing: border-box;
  list-style: none;
  position: fixed;
  right: 1em;
  top: 2em;
  text-align: center;
  max-height: 100%;
  margin: 5% 0;
  padding: 0;
}

nav ul {
  display: flex;
  flex-direction: column;
  align-items: center;
  display: inline-block;
}

nav ul li {
  list-style: none;
  font-size: 18px;
  color: var(--tertiary-color);
  font-family: var(--tertiary-font);
  writing-mode: vertical-lr;
  transform: rotate(180deg);
  margin: 2.5rem;
}

a {
  text-decoration: none;
  color: var(--tertiary-color);
  letter-spacing: 2px;
}

nav ul li a:hover {
  transition: 0.5s;
  color: var(--secondary-color);
  text-shadow: 0 0 10px var(--secondary-color), 0 0 20px var(--secondary-color),
    0 0 40px var(--secondary-color), 0 0 80px var(--secondary-color);
}

/*
  Elementos del main
*/

main {
  margin: 0 12%;
}

/* main hr {
  border: none;
  margin-bottom: 70px;
} */

.active {
  color: var(--secondary-color);
}

footer {
  text-align: center;
  margin-bottom: 15px;
}

@media (max-width: 767px){
  nav ul li {
  list-style: none;
  font-size: 18px;
  color: var(--tertiary-color);
  font-family: var(--tertiary-font);
  writing-mode:initial;
  transform: rotate(0);
  }

  nav {
    position: absolute;
    width: 100%;
    margin: 0;
    padding: 0;
  }

  nav ul {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    margin: 0;
    width: 100%;
    background-color: rgb(19, 19, 19);
    height: 70px;
  }

}
</style>
