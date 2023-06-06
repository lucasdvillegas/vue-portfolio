<template >
  <div class="container">
    <div >
      <p class="text-start">
        ¡Hola! Mi nombre es Lucas Villegas y actualmente me encuentro trabajando
        como administrativo contable. En mi tiempo libre me dedico a estudiar y
        realizar cursos y/o prácticas de Frontend developer en plataformas como
        Udemy, FreeCodeCamp, Frontend Mentor, entre otras. <br />
        Angular es mi framework de preferencia y suelo usarlo mucho con
        typescript, también me encanta cuando las cosas quedan estéticamente bien
        o tienen armonía. Tiendo a fijarme mucho en los detalles lo que me hace
        querer estar en constante aprendizaje. Sí querés saber más sobre mí te
        invito a pasarte por mi perfil en
        <a target="_blank" 
            href="https://www.linkedin.com/in/lucasdavillegas/"
            style="color:blueviolet"
          ><b>LinkedIn</b></a
        >.
      </p>

      <div class="mt-20">
        <a
          class="inline-block rounded border border-yellow-600 px-12 py-3 text-sm font-medium text-yellow-600 hover:bg-yellow-600 hover:text-white focus:outline-none focus:ring active:bg-yellow-500"
          href="/download">
          Descargar CV
        </a>
      </div>
    </div>

    <div class="about-description-img-container">
      <img src="./../assets/photos/lucasBlancoyNegro.jpg" alt=""/>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style >
h2 {
  color: var(--secondary-color);
}

p {
  font-size: 18px;
  color: var(--tertiary-color);
  padding: 15px;
  font-family: var(--tertiary-font);
}

.container {
  display: flex;
  flex-direction: row;
}



.about-description-img-container {
  max-width: 200px;
  min-width: 300px;
  height: auto;;
}

img {
  max-width: 100%;
}

</style>
