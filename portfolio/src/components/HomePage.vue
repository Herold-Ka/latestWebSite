<template>
  <div class="divHomePage">
    <div class="prez">
        <div class="homeImg">
            <img src="img/image profil.jpg" alt="profil image">
        </div>
        <h1>Vous recherchez un développeur?</h1>
        <p>Vous êtes au bon endroit</p>
    </div>
    <div class="contact">
        <ul>
        <li class="linkedin">
          <a href="https://www.linkedin.com/in/karl-merzi-094929180/" target="_blank"><img src="img/linkedIn.png" alt="linkedIn Link"></a>
        </li>
        <li class="git">
          <a href="https://github.com/herold-ka " target="_blank"><img src="img/git2.png" alt="github Link"></a>
        </li>
      </ul>
      <span class="homeNext"  @click="envoyerValeurAuParent"><p>LIRE LA SUITE</p></span>
    </div>
  </div>
</template>
<script>
export default {
    data(){
        return{
            valeur: 2
        }
    },
    methods: {
        envoyerValeurAuParent() {
      this.$emit('valeurAuParent', this.valeur);
    },
    }
}
</script>

<style scoped>
    .divHomePage{
        height: 100vh;
        width: 50%;
        margin: auto;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
    }

    .homeImg {
        border: 1px black solid;
        border-radius: 50%;
        height: 175px;
        width: 175px;
        margin: auto;
        
    }
    .homeImg img{
        object-fit: cover;
        height: 175px;
        width: 175px;
        border-radius: 50%;
    }
    h1, p{
        text-align: center;
        font-family:  'Roboto', sans-serif;
        font-weight: normal;
        color: #F5FFFA ;
    }
    .contact{
        display: flex;
    }
    .homeNext{
        margin: auto; 
        font-family:  'Roboto', sans-serif;
        border: 1px #F5FFFA solid;
        border-radius: 5px;
        font-weight: bold;
        font-size: 12px;
        width: 130px;
        height: 45px;
        background-color: #B07FFD;
        text-align: center;
        cursor: pointer;
        color: #343a40;
    }
    .homeNext p{
        color: #343a40;
        text-align: center;
        font-family:  'Roboto', sans-serif;
        font-weight: normal;
        text-align: center;
        font-weight: bold;
    }
    ul{
    list-style: none;
    display: flex;
    width: 50%;
    margin: auto;
    justify-content: space-evenly;
    align-items: center;
  }
  img{
    height: 125px;
    align-self: center;
  }
</style>