<template>
    <v-app class="" style="position:absolute; top:20vh; height:400px; bottom:; width:100%;">
    <div class="Main">
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
    </div>
    <div class="products col-md-12  row container-fluid"  style="position:absolute; top:60vh; width:100vw;">
      <v-container class="col-md-12  row container">
        <div v-for="(product, index) in products" :key="product"  style="position:relative; top:10vh; margin-bottom:10vh">
          <v-card class="products_card">
          <div class="col-md-12">
          <v-img style="width:80px; height:150px position relative; top:0px; left:90px;" :src="require('../assets/' + product)"></v-img>
          </div>
          
          <div class="col-md-12" style="position:absolute; top:120px; text-align:center; color:#28b6e7; font-size:2vh;">
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
            'house.png',
            'food.png',
            'conveyer.png',
            'care.png',
            'workshop.png',
            'laundry.png',
            'water.png',
            'special.png',
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
.products_card{
    margin-left:50px;
    width:18vw;
    height:180px;
    display:flex;
}
.container{
  background-color:;
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
    background-color:#E8E8E8;
    display:flex;
    margin-left: 5px;
  }
  .product_image{
  width:100px;
  height:100px;
  position: relative;
  top:0px;
  left:60px;
  }
  .slide{
    position: relative;
    right: 0px;
    width: 4000px;
  }
}
</style>