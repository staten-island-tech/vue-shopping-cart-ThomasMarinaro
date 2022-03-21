<template>
  <div class="home">
 <h1>the proverbial door</h1> 
 <img src="https://media2.giphy.com/avatars/julianeasily/XgpXIhg4pL5V.gif" alt="someone stole this cat">
  <h2>welcome to my store  </h2>
  
  <h1> Buy my cars</h1>
 <h2>{{money}} credits <h2>
  <div class="things">  
    <div class="items" id="ferrari">
    <h1> The F40 competizione</h1>
    <p>this ferrari is not for keeping in a garage but it has been let this caged tiger out</p>
    <img src="https://www.supercars.net/blog/wp-content/uploads/2019/10/JcQ9GNJ7REKQFiVJzXmmTA.jpg" alt="ferrari">
    </div>
    <div class="items" id="rs200">
    <h1> ford rs200 </h1>
    <p> this beaut is packing a cosworth engine so good i should not be selling </p>
    <img src="https://images.cdn.circlesix.co/image/1/700/0/uploads/posts/2016/03/f4c48dff4244772e8c9562f694204a02.jpg" alt="rs200"> 
</div>

   <div class="items" id="audi">
    <h1> the audi quattro </h1>
    <p> The german group b machine sometimes they can have a little fun </p>
    <img src="https://c4.wallpaperflare.com/wallpaper/373/72/25/audi-ur-quattro-audi-drifting-wallpaper-preview.jpg" alt="rs200">
    <button @click="quattro">450000 credits</button>
    </div>
  <div class="items" id="carrera">
    <h1> The 1973 911 carrera</h1>
    <p>this porsche is ready to rumble with a classic livery and a tried and true 911 body</p>
    <img src="https://silodrome.com/wp-content/uploads/2017/08/Porsche-911-Carrera-RS-2.7-1480x988.jpg" alt="carrera">
    <button class="button" id="gimme carrera"> 350000 credits</button>
    </div>
    <div class="items" id="celica">
    <h1> The 1994 celica </h1>
    <p>this toyota beauty proved 10 years later rally was not dead</p>
    <img src="https://i.pinimg.com/originals/5f/3f/46/5f3f4694f56c5f3a40319df79eb7d399.jpg" alt="celica">
    <button id="gimme toyota">350000 credits  </button>
    </div> 
  </div>
 </div>
</template>


<script>
export default{
  data(){
    return {
      money:1000000
    }
  },
  methods: {
    quattro:function (){
      this.money -= 350000;
    }
  }
}
</script>

<style>

.things{
  display: flex;
  flex-direction: row; 
  margin-right: 100px;
  margin-left: 100px;
  flex-grow:1;
  flex-wrap: wrap;
}
.items{
display: flex;
flex-direction: column;
flex-wrap: wrap;

background-repeat:true;
flex-grow: 1;
flex-shrink:1;
scale:0.8;
align-items: flex-start;
}
img{
padding:30px; 
flex-shrink: 1;
max-width: 40em;
}

#rs200{
  background: crimson;
}
#audi{
background: darkorange;

}
#carrera{
background-color: rgb(255, 208, 0);

}
#ferrari{
background-color: rgb(206, 0, 0);

}
#celica{
background-color: rgb(110, 223, 5);


}
</style>
