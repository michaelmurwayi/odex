<template>
    <div class="Main" style="position:absolute; top:160px; width:100%;">
    <v-carousel hide-delimiters style="height:500px"
    >
    <v-carousel-item
      v-for="(item,i) in slides"
      :key="i"
      :src= "require('../assets/' + item)"
    ></v-carousel-item>
    </v-carousel>
    <div class="products col-xs-12 row" style="height:450px display:flex;" >
      <div class="col-md-2 mt-10 ml-15 " style="background-color: #28b6e7; color:white; font-weight:bold; height: 400px; width: 150px; display:flex; border-radius: 15px 15px 15px 15px; display: inline-block; font-size:50px;">
        <p style="position:relative; top:150px"> Our Product Range </p>
      </div>
      
      <div class="col-md-9 ml-1  mt-10 row" style="height:400px;">
        
        <div v-for="(product, index) in products" :key="product" class="">
          <v-card  style="margin:5px; width:200px; height:150px; background-color:#E8E8E8; background-image" >
          <div class="col-md-12">
          <v-img style="width:60px; height:80px position relative; top:0px; left:60px;" :src="require('../assets/' + product)"></v-img>
          </div>
          
          <div class="col-md-12" style="position:absolute; top:100px; text-align:center; color:#28b6e7; font-size:2vh;">
            <p>{{products_lable[index]}} </p>
          </div>
          
          </v-card>
          
          </div>

        </div>
      </div>
    </div>
    </div>

</template>

<script>
  export default {
    data () {
      return {
        slides: [
            'homeslider01.jpg',
            'home1.jpg',
            'Systems.jpg',
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
            'lAUNDRY',
            'WATER TREATMENT',
            'SPECIALTIES',
        ],
      }
    },
  }
</script>
<style scoped>
</style>