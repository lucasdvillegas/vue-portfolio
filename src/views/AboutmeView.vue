<template>
  <section class="mytabs">
    <input type="radio" id="description" name="mytabs" checked="checked" />
    <label for="description" class="md:text-4xl max-sm:text-3xl">SOBRE MI </label>  
    <transition class="animate__fadeInLeft">
      <div class="tab">
        <AboutDescription />
      </div>
    </transition>

    <label class="md:text-4xl max-sm:text-3xl" style="margin-left: 5px; margin-right:5px; "> / </label>

    <input type="radio" id="skills" name="mytabs" /> 
    <label for="skills" class="md:text-4xl max-sm:text-3xl">HABILIDADES</label>
    <transition class="animate__fadeInRight">
      <div class="tab">
        <AboutSkills />
      </div>
    </transition>
  </section>

</template>
<script>
import 'animate.css';
import AboutDescription from './../components/AboutDescription.vue';
import AboutSkills from './../components/AboutSkills.vue';
export default {
  components: { AboutDescription, AboutSkills },
};

</script>
<style>
label {
  font-size: 36px;
  margin-top: 30px;
  font-weight: 600;
  font-family: "Roboto Condensed", sans-serif;
  color: var(--tertiary-color);
}

label:hover {
  color: var(--secondary-color);
  cursor: pointer;
  transition: 0.5s;
  color: var(--secondary-color);
  /* text-shadow: 0 0 10px var(--secondary-color), 0 0 20px var(--secondary-color),
    0 0 20px var(--secondary-color), 0 0 40px var(--secondary-color); */
}

span {
  color: var(--tertiary-color);
  margin: 0 10px;
  font-weight: bold;
}

.mytabs {
  display: flex;
  flex-wrap: wrap;
  /* margin: 50px auto; */
  /* padding: 25px; */
}

.tab {
  transition: 0.5s;

}

.mytabs input[type="radio"] {
  display: none;
}

.tab label {
  padding: 30px;
  background-color: #fff;
  font-weight: bold;
}

.mytabs .tab {
  width: 100%;
  padding: 20px;
  order: 1;
  display: none;
}

.mytabs input[type="radio"]:checked + label + .tab {
  display:block;
}

.mytabs input[type="radio"]:checked + label {
  color: var(--secondary-color);
}

section {
  will-change: transform, opacity;
  overflow-x: hidden;
}

.fade-enter-form, .fade-leave-to {
  opacity: 0;
}

.animate__fadeInLeft, .animate__fadeInRight {
  animation-duration: 1s;
}
</style>