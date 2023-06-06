<template>
  <div class="card">
    <div class="card-container">
      <img :src="proyecto.img" alt="Imagen del proyecto" />
    </div>
    <div class="card-details">
      <h3>{{ proyecto.title }}</h3>
      <p>{{ proyecto.description }}</p>
    </div>
    <div class="card-footer mt-14">
      <a target="_blank" :href="proyecto.repositoryLiunk"
        ><i class="lab la-github text-3xl"></i></a>
      <a target="_blank" :href="proyecto.deployLink"
        ><i class="las la-tv text-3xl"></i></a>
    </div>
  </div>
</template>
<script>
export default {
  props: ["proyecto"],
};
</script>
<style>


.card{
    background-color: rgb(8, 8, 8);
    border-radius: 20px;
    width: 250px;
    max-width: 300px;
    /* margin: 10px 10px; */
}
.card:hover > .card-container img{
    opacity: 1;
    transition: .6s;
}

.card:hover > .card-container > .card-container--box{
    opacity: 0;
    
}

.card-container--box{
    position: absolute;
    top: 20%;
    /* margin: 0 20%; */
}

.card-container--box i{
    font-size: 30px;
    color: var(--primary-color);
    /* margin: 5px 5px; */

}
.card .card-container {
    position: relative;
    clip-path: polygon(0 0,100% 0,100% 85%, 0 100%);
    filter: grayscale(0.1);
    width: 250px;
    height: auto;
    border-radius: 20px 20px 0 0;
    background-color: #FFA700;
}


.card-container img {
    width: 100%;
    display: block;
    border-radius: 20px 20px 0 0;
    opacity: 0;
}

.card .card-details {
    display: flex;
    flex-direction: column;
    align-items: center;
    /* margin: 15px; */
    min-height: 66px;
    max-height: 66px;
}

.card .card-details h3{
    /* margin: 2px 0; */
    color: var(--secondary-color);
    font-size: 20px;
}

.card-details p {
    color: var(--tertiary-color);
    font-size: 14px;
}

.card .card-footer{
    display: flex;
    justify-content: center;
}

.card .card-footer a{
    font-size: 16px;
    color: var(--tertiary-color);
    margin: 5px 5px;

}

.card .card-footer a:hover{
    color: var(--secondary-color);
    cursor: pointer;
}
</style>
