<template>
  <div class="divSkill">
    <h1>Compétences</h1>
    <span></span>
    <div class="divSuperior">
      <div class="cardSkillDiv" v-for="item in skillData" :key="item.id">
        <div class="cardSkill" >
        <h2>{{ item.skill }}</h2>
        <span class="cardBar"></span>
        <img :src="item.img" :alt="item.skill">
      </div>
    </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      skillData : [
    {
        id: 1,
        skill: 'HTML',
        img:'img/html.png',
    },
    {
        id: 2,
        skill: 'CSS',
        img:'img/css.png'
    },
    {
        id: 3,
        skill: 'Vue JS',
        img: 'img/vue.png'
    },
    {
        id: 4,
        skill: 'React JS',
        img: 'img/react.png'
    },
    {
        id: 5,
        skill: 'Express Node',
        img: 'img/nodeExpress.png'
    },
    {
        id: 6,
        skill: 'Flutter',
        img: 'img/flutter.png'
    },
    {
        id: 7,
        skill: 'Bootstrap',
        img: 'img/bootstrap.png'
    },
    {
        id: 8,
        skill: 'Git',
        img:'img/git2.png'
    }
  ]
    }
  }

}
</script>

<style scoped>
.divSkill{
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  overflow-y: auto;
}
.divSuperior{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 20px;
}
h1{
  font-size: 30px;
  text-align: center;
  font-family: 'Roboto', sans-serif;
  margin: 5px;
  color: #F5FFFA ;
}
.cardSkillDiv{
  height: 300px;
  width: 250px;

}
.cardSkill{
  height: 280px;
  width: 200px;
  border: 1px #B07FFD solid;
  border-radius: 7px;
  display: flex;
  flex-direction: column;
  box-shadow: 1px 5px 25px #b78bff;
}
span{
  display: block;
  width: 250px;
  margin: auto;
  background: linear-gradient(to right, #F5FFFA 0%, #F5FFFA 50%, #B07FFD 50%, #B07FFD 100% ) !important;
  height: 2px !important;
  border-radius: 15px;
}
.cardSkill h2{
  font-size: 15px;
  font-family:  'Roboto', sans-serif;
  text-align: center;
  color: #F5FFFA ;
  
}

.cardBar{
  display: block;
  width: 130px;
  margin: auto;
  background: linear-gradient(to right, #F5FFFA 0%, #F5FFFA 50%, #B07FFD 50%, #B07FFD 100% ) !important;
  height: 2px !important;
  border-radius: 15px;
}
.cardSkill img{
  width: 150px;
  margin: auto;
}
</style>