<script setup>

import { loadFull } from "tsparticles";



const particlesInit = async engine => {
    await loadFull(engine);
};

// const particlesLoaded = async container => {
//     console.log("Particles container loaded", container);
// };

// particlesInit;
// particlesLoaded;
</script>

<template>
  <div>
      <Particles
          id="tsparticles"
          :particlesInit="particlesInit"
      />

      <Particles
          id="tsparticles"
          :particlesInit="particlesInit"
          :options="{
                  background: {
                      color: {
                          value: '#0a0a0a'
                      }
                  },
                  fullScreen: {
                    enable: true,
                    zIndex: -1
                  },
                  fpsLimit: 60,
                  interactivity: {
                      events: {
                        //   onClick: {
                        //       enable: true,
                        //       mode: 'push'
                        //   },
                          onHover: {
                              enable: true,
                              mode: 'repulse'
                          },
                          resize: true
                      },
                      modes: {
                          bubble: {
                              distance: 100,
                              duration: 2,
                              opacity: 0.8,
                              size: 80
                          },
                          push: {
                              quantity: 4
                          },
                          repulse: {
                              distance: 100,
                              duration: 0.2
                          }
                      }
                  },
                  particles: {
                      color: {
                          value: '#ffa700'
                      },
                      links: {
                          color: '#ffa700',
                          distance: 150,
                          enable: true,
                          opacity: 0.2,
                          width: 1
                      },
                      collisions: {
                          enable: true
                      },
                      move: {
                          direction: 'none',
                          enable: true,
                          outMode: 'bounce',
                          random: false,
                          speed: 0.5,
                          straight: false
                      },
                      number: {
                          density: {
                              enable: true,
                              area: 800
                          },
                          value: 80
                      },
                      opacity: {
                          value: 0.1
                      },
                      shape: {
                          type: 'circle'
                      },
                      size: {
                          random: true,
                          value: 5
                      }
                  },
                  detectRetina: true
              }"
      />
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
