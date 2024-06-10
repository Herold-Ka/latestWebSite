<template >
  <div class="app">
    <div class="menu">
      <ul>
        <li>
          <img src="img/logo.png" alt="logo" class="logo">
        </li>
        <li v-on:click="selectedMenu(1)" :style="{backgroundColor: HomePage ? '#B07FFD' : 'transparent', border: HomePage ? '1px solid #F5FFFA' : 'none'}"> 
          <img src="img/home.png" alt="Home"> 
          <h1>Accueil</h1>
        </li>
        <li v-on:click="selectedMenu(2)" :style="{backgroundColor: AboutMe ? '#B07FFD' : 'transparent', border: AboutMe ? '1px solid #F5FFFA' : 'none'}"> 
          <img src="img/face.png" alt="à propos de moi icone"> 
          <h1>A propos de moi</h1>
        </li>
        <li v-on:click="selectedMenu(3)" :style="{backgroundColor: Skill ? '#B07FFD' : 'transparent', border: Skill ? '1px solid #F5FFFA' : 'none'}"> 
          <img src="img/skill_icon.png" alt="Compétences icone"> 
          <h1>Compétences</h1>
        </li>
        <li v-on:click="selectedMenu(4)" :style="{backgroundColor: Portfolio ? '#B07FFD' : 'transparent', border: Portfolio ? '1px solid #F5FFFA' : 'none'}"> 
          <img src="img/task.png" alt="Portfolio icone"> 
          <h1>Portfolio</h1>
        </li>
        <li v-on:click="selectedMenu(5)" :style="{backgroundColor: Formation ? '#B07FFD' : 'transparent', border: Formation ? '1px solid #F5FFFA' : 'none'}"> 
          <img src="img/mail.png" alt="Formation icone"> 
          <h1>Formation</h1>
        </li>
      </ul>
    </div>
    <div class="selectedMenu">
      <HomePage v-show="HomePage"  @valeurAuParent="recevoirValeurDuEnfant"/>
      <AboutMe v-show="AboutMe"/>
      <Portfolio v-show="Portfolio"/>
      <Skill v-show="Skill"/>
      <Formation v-show="Formation"/>
    </div>
  </div>

</template>

<script>
import AboutMe from './components/AboutMe.vue';
import Formation from './components/Formation.vue';
import Skill from './components/Skill.vue';
import Portfolio from './components/Portfolio.vue';
import HomePage from './components/HomePage.vue';

export default {
    components: { AboutMe, Formation, Skill, HomePage, Portfolio },
    data(){
      return{
        AboutMe: false,
        Formation: false,
        Skill: false,
        Portfolio: false,
        HomePage: true,
      }
    },
    methods: {

      recevoirValeurDuEnfant(valeur) {
       this.selectedMenu(valeur);
    },
      selectedMenu(value){
        console.log(value);
        switch(value){
          case 1: this.HomePage = true, this.Formation = false, this.Skill = false, this.Portfolio = false, this.AboutMe = false;
          break;
          case 2: this.HomePage = false, this.Formation = false, this.Skill = false, this.Portfolio = false, this.AboutMe = true;
          break;
          case 3: this.HomePage = false, this.Formation = false, this.Skill = true, this.Portfolio = false, this.AboutMe = false;
          break;
          case 4: this.HomePage = false, this.Formation = false, this.Skill = false, this.Portfolio = true, this.AboutMe = false;
          break;
          case 5: this.HomePage = false, this.Formation = true, this.Skill = false, this.Portfolio = false, this.AboutMe = false;
          break;
          default: console.log("Err Switch case");
        }
      }
    }
}
</script>

<style scoped>
*{ 
  margin: 0;
  box-sizing: border-box;
  padding: 0 !important;
}
  .app{
    display: flex;
    width: 100vw;
    height: 100vh;
    background-color: #343a40;
    /*background-color: #F5FFFA;*/
  }
  .menu{
    /*flex-grow: 1;*/
    width: 20%;
    display: flex;
    justify-content: center;
  }
  .menu ul{
    margin: auto;
    list-style: none;
    height: 300px;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    padding: 20px 20px 20px 0 !important;
    border-right: 2px solid #F5FFFA;
  }

  li{
    display: flex;
    justify-content: start;
    padding: 10px !important;
    
  }
  li{
    /*background-color: #F5FFFA;*/
    border-radius: 5px;
    padding: 10px !important;
    -webkit-transition-duration: 0.4s; 
    /* Safari */
    transition-duration: 0.5s;
    
  }

  .logo{
    width: 90px;
    margin: auto;
  }
  li img{
    width: 30px;
    cursor: pointer;
  }
  li h1 {
    font-family:  'Roboto', sans-serif;
    font-weight: normal;
    font-size: 20px;
    margin: auto;
    cursor: pointer;
  }
  .selectedMenu{
    width: 80%;   
  }
</style>