<template>
  <div>
    <div class="title">
      <h1>A propos de moi</h1>
      <span></span>
    </div>
    <div class="divText">
      <p>
      Passionné de technologie et d’informatique depuis tout petit, je décide en 2020 d'en faire mon métier. 
    </p>
    <p>
      En 2020 d'un an où j'apprend les bases de programmation (HTML, CSS, JavaScript, SQL) et l'utilisation de 3 frameworks (VueJS, Node express, ReactJS).
      Suite à cela j'ai une année en alternance comme développeur web et mobile. Je suis actuellement à la recherche d'une alternance 
      d'un rythme de 3 semaine/ 1 semaine.
    </p>
    <p>

    </p>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style scoped>

h1{
  font-family:  'Roboto', sans-serif;
  font-weight: normal;
  font-size: 35px;
  color: #F5FFFA;
}
span{
  display: block;
  width: 300px;
  margin: auto;
  background: linear-gradient(to right, #F5FFFA 0%, #F5FFFA 50%, #B07FFD 50%, #B07FFD 100% ) !important;
  height: 10px !important;
  border-radius: 15px;
}
.title{
  margin: auto;
  text-align: center;
}
.divText{
  margin-top: 75px !important;
  width: 700px;
  border: 2px solid #B07FFD;
  border-radius:  15px;
  margin: auto;
  padding: 20px 30px;
}
p{
  font-family:  'Roboto', sans-serif;
  font-weight: normal;
  font-size: 17px;
  color: #F5FFFA;
}
</style>