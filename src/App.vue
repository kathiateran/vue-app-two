<template>
  <!-- <Greet name="Bruce" heroName="Batman"/>
  <Greet name="Johana" heroName="Superman"/>
  <Greet :name="name" :heroName="dept"/> -->

  <!-- <Article id="my-article" title="Article Title" :likes="1000" :isPublished="true"></Article> -->
  <button @click="showPopup=true">Show</button>
  <Popup v-show="showPopup" @close="closePopup"/>
</template>


<script>
//import Greet from './components/Greet'
//import Article from './components/Article'
import Popup from './components/Popup'

export default {
  name: 'App',
  components: {
    //Greet,
    //Article,
    Popup,
  },
  methods:{
    closePopup(msg){
      this.showPopup=false
      console.log(msg)
    }
  },
  data(){
    return{
      name:"John",
      dept:"Sales",
      showPopup:false

    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
  margin-top: 60px;
}
</style>
