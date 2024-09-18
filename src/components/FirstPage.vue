<template>
  <div >
    <SecondPage/>

    <h1>nadia</h1>
    <!--props-->
    <h2>{{ msg }}</h2>
        <!--interpolation-->
        <h2>{{ num }}</h2>
        <p>{{country[3] }}</p>
        <p>{{ getName() }}</p>
        <p>{{ getEmail() }}</p>

  </div>
  <!-------- class c'est un attribute--------->
  <!-------- avec binding on peut utiliser javascript dans class--------->
  <div v-bind:class="getstyle()">
   Nadia bouzayani 
  </div>
  <a :href="link"> google </a>

</template>

<script>
import SecondPage from './SecondPage'

export default {
   name: 'FirstPage',
   components:{
    SecondPage,
   },
   props:{
    msg:String
   },
      /****************  data   ***************************** */

   data(){
      return{

        num:10,
        name:'bouzayani',
        country:['tunisia','libya','marroco','algeria','egypt'],
        verif:true,
        className:'fl',
        link:'http://google.com'
      }

   },
   /****************  constructor  ***************************** */
   beforeCreate(){
   },
   created(){

   },
         /****************  function   ***************************** */
    methods:{
      getName(){
        return'nadia Bouzayani'
      },
      getEmail(){
        return 'nadiabouzayani3@gmail.com'
      },
      getstyle(){
        return'fl'
      }
      
    }


 
}
</script>

<style scoped>
h1{
  color: red;
  
}
.fl{
  color: blueviolet;
  font: optional;
  font-size: medium;
}
</style>
