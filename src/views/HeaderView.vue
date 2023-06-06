<template>
  <header id="home">
    <div class="header-container">

      <div class="left">
        <a target="_blank" href="https://github.com/lucasdvillegas" class="max-md:hidden"
          ><i class="lab la-github"></i></a>
        <a target="_blank" href="https://www.linkedin.com/in/lucasdavillegas/" class="max-md:hidden"
          ><i class="lab la-linkedin-in"></i></a>
        <a href="#contact" class="max-md:hidden"><i class="lar la-envelope"></i></a>
      </div>

      <div class="portada">
        <div class="loader"></div>
        <div class="img-container">
          <img
            src="./../assets/photos/Lucas.png"
            alt="Foto del desarrollador"
          />
        </div>
      </div>

      <div class="right"></div>
    </div>

    <div class="home-text-bottom">
      <h1 class="text-5xl">
        <!-- <b
          ><span>{{ person.name | uppercase }}</span>
          {{ person.surname | uppercase }}</b
        > -->
        <b><span>LUCAS</span> VILLEGAS</b>
      </h1>
      <h2 class="text-4xl">FRONTEND DEVELOPER | VUE</h2>
    </div>
  </header>
</template>
<script>
export default {};
</script>
<style>
header {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  height: 100vh;
  min-width: 100%;
}

header .header-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  width: 100%;
}

header .header-container .right {
  margin-right: 3em;
}

header .header-container .left {
  margin-left: 3em;
  display: flex;
  flex-direction: column;
}

header .left a i {
  font-size: 40px;
  color: var(--tertiary-color);
  margin: 20px 0 20px 0;
  text-decoration: none;
}

header .left a i:hover {
  transition: 0.5s;
  color: var(--secondary-color);
  text-shadow: 0 0 10px var(--secondary-color), 0 0 20px var(--secondary-color),
    0 0 40px var(--secondary-color), 0 0 80px var(--secondary-color);
}

.portada {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  position: relative;
}

.loader {
  position: relative;
  width: 430px;
  height: 430px;
  border-radius: 50%;
  background: linear-gradient(
    45deg,
    transparent,
    transparent 40%,
    var(--secondary-color)
  );
  animation: animar 18s linear infinite;
}

@keyframes animar {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

.loader:before {
  content: "";
  position: absolute;
  top: 35px;
  left: 35px;
  right: 35px;
  bottom: 35px;
  border-radius: 50%;
  z-index: 1000;
  background-color: var(--primary-color);
  /* background: url('./../../../assets/test/fondo-sinruido.jpg'); */
}

.loader:after {
  content: "";
  position: absolute;
  top: 0px;
  left: 0px;
  right: 0px;
  bottom: 0px;
  background: linear-gradient(
    45deg,
    transparent,
    transparent 40%,
    var(--secondary-color)
  );
  border-radius: 50%;
  z-index: 1;
  filter: blur(20px);
}

.img-container {
  width: 400px;
  height: auto;
  position: absolute;
  bottom: 30.5px;
  margin-right: 3.5px;
  z-index: 1;
}

.img-container img {
  max-width: 100%;
  height: auto;
  filter: contrast(112%);
  filter: sepia(50%);
}

.home-text-bottom {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.home-text-bottom h1 {
  font-family: var(--primary-font);
  letter-spacing: 5px;
  color: var(--tertiary-color);
  font-size: 78px;
}

.home-text-bottom h2 {
  font-family: var(--secondary-font);
  color: var(--tertiary-color);
  letter-spacing: 2px;
  font-size: 24px;
  margin-top: 10px;
}

.home-text-bottom span {
  color: var(--secondary-color);
  
}
</style>
