<template>
  <div class="about">
    <h1>fake cars</h1>
    <body>
      <h1>game cars</h1>

      <section class="box" id="box" v-for="car in cars" :key="car">
        <h1>{{ car.name }} by {{ car.manufacturers }}</h1>
        <h2>also known as the {{ car.realname }}</h2>
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
      cars: [
        {
          name: "calicogtf",
          location: "SSAA",
          manufacturers: "karin",
          realname: "celica",
          price: 1489000,
        },
        {
          name: "munroe",
          manufacturers: "pegassi",
        },
      ],
      cart:[]
    };
  },
  methods:{
    

  }
};
</script>
<style>
.box {
  display: flex;
  flex-direction: row;
  margin-right: 100px;
  margin-left: 100px;
  flex-grow: 1;
  flex-wrap: wrap;
  background-color: blue;
}
h1 {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;

  background-repeat: true;
  flex-grow: 1;
  flex-shrink: 1;
  scale: 0.8;
  align-items: flex-start;
}
img {
  padding: 30px;
  flex-shrink: 1;
  max-width: 40em;
}
</style>