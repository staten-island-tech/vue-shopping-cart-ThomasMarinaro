<template>
  <div class="about">
    <h1>fake cars </h1>
 <body>
  <h1>game cars </h1>
  
  
 
    <section class="box" id="box"> 
       <ul>
      <li v-for="car in cars" :key="car">{{ car }}</li>
    </ul>

    </section>
 </body>
  </div>
</template>
<script>
export default {
  name: "about",
  components: {},
  data(){
    return{
      cars: [
        {
          name:"calicogtf",
          location:"SSAA",
        }]
        
    };
  
  }


}



</script>
