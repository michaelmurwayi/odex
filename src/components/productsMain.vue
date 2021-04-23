<template>
    <v-app>
    <v-carousel hide-delimiters :controls="false" :indicators="false" :show-arrows="false"  class="slide" show-arrows-on-hover
    >
    <v-carousel-item
      v-for="(item,i) in slides"
      :key="i"
      :src= "require('../assets/' + item)"
    >
    
    <v-card class="products_page">
        <v-card-title class="" style="position:relative; left:0px; top:20px; font-weight:bold; font-size: 8vh;">Products</v-card-title>
    </v-card>
    
    </v-carousel-item>
    </v-carousel>
    <div class="products col-md-12  row container-fluid" >
      <v-container class="col-md-12  row container">
        <div v-for="(product, index) in products" :key="product" >
          <v-card class="products_card">
          <div class="col-md-12">
          <v-img class="product_image" :src="require('../assets/' + product)"></v-img>
          </div>
          
          <div class="col-md-12 products_lable" >
            <p>{{products_lable[index]}} </p>
          </div>
          
          </v-card>
          
          </div>
      </v-container>

      </div>
    </v-app>
</template>
<script>
export default {
     data () {
      return {
        slides: [
            'products_intro.jpg',
            
        ],
         products: [
            'kitchen.png',
            'house.jpg',
            'food.jpeg',
            'conveyer.png',
            'personal.jpeg',
            'workshop.jpeg',
            'laundry.jpeg',
            'water.jpeg',
            'specials.jpeg',
        ],
        products_lable: [
            'KITCHEN HYGIENE',
            'HOUSE KEEPING',
            'FOOD & BEVERAGE  ',
            'CONVEYER SYSTEM',
            'PERSONAL CARE',
            'WORKSHOP',
            'LAUNDRY',
            'WATER TREATMENT',
            'SPECIALTIES',
        ],
      
}
     }
     }
</script>
<style scoped>
.products_page{
    position:absolute;
    top:150px;
    left:650px;
    height:15vh;
    width: fit-content;
    background-color:#28b6e7;
    opacity:0.8;
}
.products{
    position:absolute;
    top:60vh;
    width:100vw;
}
.products_intro{
    background-color: #28b6e7;
    color:white;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    height: 400px;
    width: 150px;
    margin-left: 80px;
    display:flex;
    border-radius: 15px 15px 15px 15px;
    display: inline-block;
    font-size:50px;
}
.products_header{
    position:relative;
    top:"150px";
    font-size: 8vh;
    font-family: cursive;
    text-align: right;
    margin-top: 60px;
}
.product_image{
  width:100%;
  height:150px;
  position: relative;
  top:0px;
  opacity: 0.8;
  left:0px;
}
.products_lable{
  position:absolute;
  top:200px;
  text-align:center;
  color:#28b6e7;
  font-size:2vh;
}
.products_card{
    margin-top:35px;
    width:20vw;
    height:250px;
    margin-left: 50px;
    background-color: white;
    display:flex;
}
.container{
  margin-top: 20px;
  height:850px;
  display: "flex"
}

@media only screen and (max-width: 768px) {
  .products_page{
    position:absolute;
    top:150px;
    left:50px;
    height:15vh;
    width: fit-content;
    background-color:#28b6e7;
    opacity:0.8;
  }
  .products{
    background-color: white ;
    position: absolute;
    top:80vh;
  }
  .products_intro{
    background-color: #28b6e7;
    height: 80px;
    width: 80%;
    margin-top: 25px;
    margin-left: 0px;
    margin-right: 25px;
    margin-bottom: 0px;
  }
  .products_header{
    position:relative;
    top:20px;
    font-size: 4vh;
    text-align: center;
  }
  .products_card{
    margin:px;
    width:60vw;
    height:25vh;
    background-color: white;
    display:flex;
    margin-left: 55px;
  }
  .product_image{
  width:100%;
  height: 100px;
  position: relative;
  top:0px;
  opacity: 0.8;
  left:0px;
}
.products_lable{
  position:absolute;
  top: 130px;
  text-align:center;
  color:#28b6e7;
  font-size:2vh;
}
  .slide{
    position: relative;
    right: 0px;
    width: 4000px;
  }
}
</style>