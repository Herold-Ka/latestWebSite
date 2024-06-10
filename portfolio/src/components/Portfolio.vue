<template>
  <div class="divPortfolio">
     <div class="titrePortfolio">
      <h1>Portfolio</h1>
      <span></span>
    </div>
    <div class="portfolio">
      <div class="cardPortfolioDiv" v-for="item in portfolioData" :key="item.id">
        <div class="cardItem">
          <img :src="item.logo" alt="Logo">
          <h2>
            {{ item.name }}
          </h2>
          <span></span>
          <div class="techno">
            <p>{{ item.techno1 }}</p>
            <p>{{ item.techno2 }}</p>
            <p>{{ item.techno3 }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      portfolioData: [
        {
          id: 1,
          name:"weeb nation",
          techno1: "VueJS", 
          techno2: "NodeJS/Express",
          techno3: "SQL",
          logo: "img/Weeb2.png",
          img:"img/vue cardMangaEx",
        },
        {
          id: 2,
          name:"Vitrine",
          techno1: "ReactJS",
          techno2: "NodeJS/Express",
          techno3: "SQL",
          logo: "img/Violet Moderne Technologie et Gaming Logo.png",
          img: "img/vitre.png",
        },
        {
          id: 3,
          name: "Genshin Picker",
          techno1: "VueJS", 
          techno2: "NodeJS/Express",
          techno3: "SQL",
          logo: "img/genshin-impact-paimon.png",
          img: "img/genshin picker screen.png"
        },
        {
          id: 4,
          name: "Grimoire BOTC",
          techno1: "Flutter", 
          techno2: "",
          techno3: "",
          logo: "img/boct logo.jpg",
          img: "img/",
        }
      ]
    }
  }
}
</script>

<style scoped>
.divPortfolio{
  height: 100vh;
  overflow-y: auto;
}
.titrePortfolio{
  margin: auto;
}

h1{
  text-align: center;
  font-size: 30px;
  text-align: center;
  font-family: 'Roboto', sans-serif;
  margin: 5px;
  color: #F5FFFA ;
}

span{
  display: block;
  width: 250px;
  margin: auto;
  background: linear-gradient(to right, #F5FFFA 0%, #F5FFFA 50%, #B07FFD 50%, #B07FFD 100% ) !important;
  height: 2px !important;
  border-radius: 15px;
}

.portfolio{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 20px !important;
  justify-content:center;
}
.cardItem{
  justify-self: start;
  height: 280px;
  width: 200px;
  border: 1px #B07FFD solid;
  border-radius: 7px;
  margin-right: 20px;
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  box-shadow: 1px 5px 25px #b78bff;

}
.cardItem img{
  height: 50px;
  margin: auto;
  margin-top: 5px;
}
.cardItem h2{
  font-size: 15px;
  font-family:  'Roboto', sans-serif;
  text-align: center;
  color: #F5FFFA ;
  /*flex-grow: 0.1;*/
}
.cardItem span{
  width: 150px;
  
}
.cardItem .techno{
  flex-grow: 4;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.techno p {
  
  font-size: 12px;
  font-family:  'Roboto', sans-serif;
  text-align: center;
  color: #F5FFFA ;
}
</style>