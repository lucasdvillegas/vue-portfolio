<template >
    <div class="about-container">

<div class="about-skill-soft">
  <h4>HABILIDADES BLANDAS</h4>
  <div class="about-skill-soft-box">
    <div id="work-group" class="soft-box">
        <i class="las la-users"></i>
      <p>Trabajo en equipo</p>
    </div>
    <div id="time-manager" class="soft-box">
        <i class="las la-user-clock"></i>
      <p>Gestión del tiempo</p>
    </div>
    <div id="autodidact" class="soft-box">
        <i class="las la-user"></i>
      <p >Autodidacta</p>
    </div>
  </div>
</div>

<div class="about-skill-hard">
  <h4>HABILIDADES TÉCNICAS</h4>
  <div class="grid grid-cols-3 mt-3">
    <div class="flex flex-col">
      <i class="lab la-html5" style="color:rgb(183, 119, 50)"></i>
      <p>HTML</p>
    </div>
    
    <div class="flex flex-col">
      <i class="lab la-css3-alt" style="color:rgb(58, 98, 166)"></i>
      <p>CSS</p>
    </div>

    <div class="flex flex-col">
      <i class="lab la-js" style="color:rgb(206, 201, 54)"></i>
      <p>Javascript</p>
    </div>

    <div class="flex flex-col">
      <i class="lab la-vuejs" style="color:rgb(54, 161, 156)"></i>
      <p>Vue</p>
    </div>

    <div class="flex flex-col">
      <i class="lab la-php" style="color:rgb(57, 98, 159)"></i>
      <p>PHP</p>
    </div>

    <div class="flex flex-col">
      <i class="lab la-laravel" style="color:rgb(175, 68, 41)"></i>
      <p>Laravel</p>
    </div>

    <!-- <i class="lab la-css3-alt" style="color:rgb(58, 98, 166)"></i>
    <i class="lab la-js" style="color:rgb(206, 201, 54)"></i>
    <i class="lab la-vuejs" style="color:rgb(54, 161, 156)"></i>
    <i class="lab la-php" style="color:rgb(57, 98, 159)"></i>
    <i class="lab la-laravel" style="color:rgb(175, 68, 41)"></i> -->
  </div>
</div>

<div class="about-skill-others">
  <h4>OTRAS HABILIDADES</h4>

  <div class="about-skill-soft-box">
    <div id="work-group" class="soft-box">
        <i class="lab la-adobe"></i>
      <p>Adobe Photoshop</p>
    </div>
    <div id="time-manager" class="soft-box">
        <i class="las la-terminal"></i>
      <p>Uso de terminal</p>
    </div>
  </div>

</div>
</div>

</template>
<script>
export default {
    
}
</script>
<style>
.about-container {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  margin-top: 30px;
  
}

.about-container,  i {
  font-size: 40px;
}

.about-skill-soft, .about-skill-hard, .about-skill-others {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 15px;
}

.about-skill-soft-box i{
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: var(--icon-fontSize);
  color: var(--secondary-color);
  margin: 10px 0;
}

.about-skill-soft-box i, .about-skill-hard-box i, .about-skill-others-box i{
  margin-top: 15px;
  font-size: 45px;
}

.about-skill-hard-box{
  display: flex;
  flex-wrap: wrap;
}

.about-skill-hard-box > i{
  flex: 40%;
  color: var(--secondary-color);
}
.about-skill-hard-box i{
  font-size: 45px;
  margin: 5px 0;
}

.about-skill-others-box {
  display: flex;
}

.about-skill-others-box .icon-container {
  max-width: 50px;
  height: auto;
}

.about-skill-others-box img {
  width: 100%;
  height: auto;
}

h4 {
  color:var(--tertiary-color);
  font-family: var(--primary-font);
  font-size: 20px;
}

</style>