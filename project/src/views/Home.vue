<template>
  <div class="home">
 <h1>the proverbial door</h1> 
 <img src="https://media2.giphy.com/avatars/julianeasily/XgpXIhg4pL5V.gif" alt="someone stole this cat">
  
  <div> 
    <h1> welcome to my store you have {{money}}</h1>
    <h2 v-if="isShow"> you got an audi</h2>
    <h2 v-if="willShow"> you got a celica</h2>
    <h2 v-if="canShow"> you got a carrera</h2>

  </div>
  <h1> Buy  my cars</h1>
 
  <div class="things">  
    <div class="items" id="ferrari">
    <h1> The F40 competizione</h1>
    <p>this ferrari is not for keeping in a garage but it has been let this caged tiger out</p>
    <img src="https://www.supercars.net/blog/wp-content/uploads/2019/10/JcQ9GNJ7REKQFiVJzXmmTA.jpg" alt="ferrari">
    <button @click="ferrarifund" v-if="wannaShow"> refund</button>
    </div>
    <div class="items" id="rs200">
    <h1> ford rs200 </h1>
    <p> this beaut is packing a cosworth engine so good i should not be selling </p>
    <img src="https://images.cdn.circlesix.co/image/1/700/0/uploads/posts/2016/03/f4c48dff4244772e8c9562f694204a02.jpg" alt="rs200"> 
    <button @click="rs200refund" v-if="mightShow"> refund</button>
    <button @click="rs200" v-else  > 450000</button>
</div>

   <div class="items" id="audi">
    <h1> the audi quattro </h1>
    <p> The german group b machine sometimes they can have a little fun </p>
    <img src="https://c4.wallpaperflare.com/wallpaper/373/72/25/audi-ur-quattro-audi-drifting-wallpaper-preview.jpg" alt="rs200">
    <button @click="quattro" >450000 credits to cart</button>
    <button @click="quattrorefund" v-if="isShow">refund</button>
    </div>
  <div class="items" id="carrera">
    <h1> The 1973 911 carrera</h1>
    <p>this porsche is ready to rumble with a classic livery and a tried and true 911 body</p>
    <img src="https://silodrome.com/wp-content/uploads/2017/08/Porsche-911-Carrera-RS-2.7-1480x988.jpg" alt="carrera">
    <button @click="carrera" id="gimme carrera"> 350000 credits</button>
    <button @click="carrerarefund" v-if="canShow"> refund</button>
    </div>
    <div class="items" id="celica">
    <h1> The 1994 celica </h1>
    <p>this toyota beauty proved 10 years later rally was not dead</p>
    <img src="https://i.pinimg.com/originals/5f/3f/46/5f3f4694f56c5f3a40319df79eb7d399.jpg" alt="celica">
    <button @click="celica" id="gimme toyota">350000 credits  </button>
    <button @click="celicarefund" v-if="willShow">refund</button>

    </div> 
  </div>
 </div>
</template>


<script>
export default {
  data(){

    return {
      money:1000000,
      showmoney:1,
      isShow: false,
      willShow:false,
      canShow:false,
      mightShow:false,
      wannaShow:false,
    }

  },
  methods: {
    quattro:function (){
      
      this.showmoney+= 1;
      this.isShow = true,
      this.money -=450000,
      alert('you have ' + this.money)
      this.willShow = false
    },  
    quattrorefund:function (){
    
      this.money += 450000,
      this.isShow = false,
      alert('you have ' + this.money)
    },
    celica:function (){
      this.willShow = true,
      this.money -= 450000,
      alert('you have ' + this.money)
    },
    celicarefund:function (){
    
      this.money += 450000,
      this.willShow = false,
      alert('you have ' + this.money)
    },
    carrera:function (){
      this.canShow = true,
      this.money -= 450000,
      alert('you have ' + this.money)
    },
    carrerarefund:function (){
    
      this.money += 450000,
      this.canShow = false,
      alert('you have ' + this.money)
    },
     ferrari:function (){
      
      this.showmoney+= 1;
      this.wannaShow = true,
      this.money -=450000,
      alert('you have ' + this.money)
      
    },  
    ferrarirefund:function (){
    
      this.money += 450000,
      this.wannaShow = false,
      alert('you have ' + this.money)
    },
    rs200:function (){
      this.mightShow = true,
      this.money -= 450000,
      alert('you have ' + this.money)
    },
    rs200refund:function (){
    
      this.money += 450000,
      this.mightShow = false,
      alert('you have ' + this.money)
    },
 
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
