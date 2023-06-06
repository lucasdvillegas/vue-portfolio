<template>
  <section class="mytabs">
    <input type="radio" id="proyectos" name="mytabs2" checked="checked" />
    <label for="proyectos"  class="md:text-4xl max-sm:text-3xl"
      >PROYECTOS
    </label>
    <transition class="animate__fadeInLeft">
      <div class="tab">
        <div class="grid justify-items-center 
          lg:grid-cols-3 
          md:grid-cols-2
          sm:grid-cols-1">
          <div
            v-for="proyecto in lucasProyectos"
            :key="proyecto.id"
            class="max-w-xs content-center m-2"
          >
            <ProjectCard :proyecto="proyecto" class="" />
          </div>
        </div>
      </div>
    </transition>

    <label class="md:text-4xl max-sm:text-3xl" style="margin-left: 5px; margin-right:5px; "> / </label>

    <input type="radio" id="practicas" name="mytabs2"  />
    <label for="practicas"  class="md:text-4xl max-sm:text-3xl">PRACTICAS</label>
    <transition class="animate__fadeInRight">
      <div class="tab">

        <div class="grid justify-items-center 
          lg:grid-cols-3 
          md:grid-cols-2
          sm:grid-cols-1">
          <div
            v-for="proyecto in lucasPracticas"
            :key="proyecto.id"
            class="max-w-xs content-center m-2"
          >
            <ProjectCard :proyecto="proyecto" class="items-center"/>
          </div>
        </div>

      </div>
    </transition>
  </section>
</template>
<script>
import dataLucas from "./../assets/data/data.json";
import ProjectCard from "./../components/ProjectCard.vue";

export default {
  components: {
    ProjectCard,
  },

  setup() {
    let lucasProyectos = dataLucas.user.projects;
    let lucasPracticas = dataLucas.user.practices;

    return {
      lucasProyectos,
      lucasPracticas
    };
  },
};
</script>
<style >
.mytabs {
  padding: 0;
}
.proyectos {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 3rem;
  margin: 3rem 0;
}
@media (max-width: 767px){
  section {
  margin-bottom: 50px;
}
}

</style>
