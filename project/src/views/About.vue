<template>
  <div class="about">
    <h1>fake cars </h1>
 <body>
  <h1>gta cars </h1>
  <div class="btn">  
    <button id="setting" type="button"> setting</button>
    <button id="expensive" type="button" > The Land of Price </button>
    <button id="sportsclassic" type="button">Sportsclassics</button>
    <button id="sports" type="button">Sports</button>
    <button id="Offroad" type="button">Offroad</button>
  </div>
    <section class="box" id="box"> 
    

    </section>
 </body>
  </div>
</template>
<script>
let DOMSelectors = {
  _card: document.getElementById("box"),
  get card() {
    return this._card;
  },
  set card(value) {
    this._card=value;
  },
};
const GtaCars = [
    {
        Name: "Sultan",
        Manufacturer: "Karin",
        Class: "Sports",
        Image: "https://gtamag.com/images/photo/gta-mag-Sultan-750332.jpg",
        topSpeed: 115.75,
        price: 12000,
        fourDoor:true,
        methodOfObtaining: ["Benny's Original Motorsports Website","off the street"],
        
    },
    {
        Name: "Zentorno",
        Manufacturer: "Pegassi",
        Image:"https://www.gta5car.com/wp-content/uploads/2014/10/Pegassi-Zentorno-GTA-5-Front.jpg",
        Class: "Supers",
        topSpeed:122, 
        price:725000,
        fourDoor:false,
        methodOfObtaining: ["Legendary Motorsports"]
    },
    {
        Name: "Caracara 4x4",
        Manufacturer: "Vapid",
        Image:"https://gtamag.com/images/photo/small/gta-mag-vapid-caracara-4x4-220496.jpg",
        Class: "Off-Road",
        topSpeed: 103.25,
        price:875000,
        fourdoor:true, 
        methodOfObtaining: ["South San Andreas Super Autos"],
        
    },
    {
        Name: "Viseris",
        Manufacturer:"Lampadati",
        Class: "SportsClassics",
        Image:"https://gtamag.com/images/photo/gta-mag-lampadati-viseris-325108.jpg" ,
        topSpeed:124.75,
        price:875000,
        fourDoor:true,
        methodOfObtaining: ["Legendary Motorsports"]



    },
    {
        Name: "Torero",
        Manufacturer:"Pegassi",
        Class: "SportsClassics",
        Image: "https://gtamag.com/images/photo/gta-mag-pegassi-torero-238447.jpg",
        topSpeed:116.5, 
        price:998000,
        fourDoor:false,
        methodOfObtaining: ["Legendary Motorsports"]



        
    },
    {
    Name:"Monroe",
    Manufacturer:"Pegassi",
    Class: "SportsClassics",
    Image: "https://gtamag.com/images/photo/gta-mag-Monroe-459747.jpg",
    topSpeed:122,
    price:490000, 
    fourDoor:false, 
    methodOfObtaining:["Legendary Motorsports"]
    },
    {
    Name:"Banshee",
    Manufacturer:"Bravado",
    Class: "Sports",
    Image:"https://gtamag.com/images/photo/gta-mag-Banshee-936343.jpg",
    price:105000,
    fourDoor:false,
    methodOfObtaining:["Legendary Motorsports", "off the street", "benny's"],
    topSpeed:116,        
    },
    {
        Name:"Brawler",
        Manufacturer:"Coil",
        Class: "Off-Road",
        Image:"http://www.gta5rides.com/vehicleImages/cropped/brawler.jpg.jpg",
        price:715000,
        fourDoor:false,
        methodOfObtaining:["Legendary Motorsports"],
        topSpeed:117.75,
        }]

  GtaCars.forEach((GtaCars)=>{
    
    console.log("imhere"),
    document.getElementById("box").insertAdjacentHTML("beforeend",`
    
    
    <div class= "card">
    <h1 class="Name"> ${GtaCars.Manufacturer} ${GtaCars.Name} </h1>
    <img class="pic" src="${GtaCars.Image}" alt="pic"> </img> 
    <h2 class="Class"> ${GtaCars.Class} price:${GtaCars.price}</h2>
    </div>
    
    
    `);
    
    
});  


</script>
