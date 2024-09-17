<template>
  <div >
    <SecondPage/>

    <h1>nadia</h1>
    
  </div>
</template>

<script>
import SecondPage from './SecondPage'

export default {
   name: 'FirstPage',
   components:{
    SecondPage,
   }
 
}
</script>

<style scoped>
h1{
  color: red;
  
}
</style>
