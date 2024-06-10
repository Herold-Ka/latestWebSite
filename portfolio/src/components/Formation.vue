<template>
  <div class="divContact">
    <div class="title">
      <h1>Contact</h1>
      <span></span>
    </div>
    
    <div class="social">
      <p>
        Un projet? Contacter moi.
      </p>
      <ul>
        <li class="linkedin">
          <a href="https://www.linkedin.com/in/karl-merzi-094929180/" target="_blank"><img src="img/linkedIn.png" alt="linkedIn Link"></a>
        </li>
        <li class="facebook">
          <a href="https://www.instagram.com/karlmerzi/" target="_blank"><img src="img/fb.png" alt="facebook Link"></a>
        </li>
        <li class="instagram">
          <a href="https://www.facebook.com/karl.merzi" target="_blank"><img src="img/insta.png" alt="instagram Link"></a>
        </li>
      </ul>
    </div>
    
  </div>
</template>

<script>
export default {
  data(){
    return{

    }
  }

}
</script>

<style scoped>
  .divContact{
    display: flex;
    flex-direction: column;
  }
  h1{
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
    height: 10px !important;
    border-radius: 15px;
  }
  .title{
    flex-grow: 1;
  }
  .social{
    margin: auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex-grow: 4;
  }
  p{
    font-size: 17px;
    font-family:  'Roboto', sans-serif;
    text-align: center;
    color: #F5FFFA ;
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