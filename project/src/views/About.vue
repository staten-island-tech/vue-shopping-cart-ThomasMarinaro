<template>
  <div class="about">
    <h1>fake cars</h1>
    <button class=""> </button>
    <body>
      <h1>game cars</h1>

      <section class="box" id="box" v-for="car in cars" :key="car">
        <h1>{{ car.product }} by {{ car.customer }}</h1>
        <h2>also known as the {{ car.product }}</h2>
          <h1>{{ queue.product }} by {{ queue.customer }}</h1>
        <h2>also known as the {{ queue.product }}</h2>
            <button @click="queuecars">work</button>

      </section>
    </body>
  </div>
</template>

<script>
export default {
  name: "about",
  components: {},
    data() {
    return {
      queue: [{
      }],

     
      
    };
  },
  methods: {
    queuecars() {
      this.push(this.cars.product);
    }
  },
  // data() {
  //   return {
    
      cars: [
        {
          name: "calicogtf",
          location: "SSAA",
          manufacturers: "karin",
          realname: "celica",
          prices: 1489000,
        },
        { 
          manufacturers: "pegassi",
          
        },
       
      ],
  
  // methods:{
  //  methods: {
  //   addToCart(this.cart) {
  //     this.cart.push(this.cars.name);
  //   }
  //   },

  // }
};
</script>
<style>

  
</style>