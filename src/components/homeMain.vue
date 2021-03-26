<template>
  <v-app>
    <div class="Main" style="position:relative; top: 5vh; bottom:20vh; width:100%;">
    <v-carousel class="slide" hide-delimiters :controls="false" :indicators="false" :interval="3000" direction="up">
    <v-carousel-item
      v-for="(item,i) in slides"
      :key="i"
      :src= "require('../assets/' + item)"
    ></v-carousel-item>
    </v-carousel>
    
    <div class="products col-xs-12 row container-fluid">
      <div class="products_intro col-md-2" >
        <p class="products_header"> Our Product Range </p>
      </div>
      
      <v-container class="col-md-9 ml-1 row container">
        <div v-for="(product, index) in products" :key="product"  style="position:relative; top:10vh">
          <v-card class="products_card">
          <div class="col-md-12">
          <v-img class="product_image" :src="require('../assets/' + product)"></v-img>
          </div>
          
          <div class="col-md-12" style="position:absolute; top:100px; text-align:center; color:#28b6e7; font-size:2vh;">
            <p>{{products_lable[index]}} </p>
          </div>
          
          </v-card>
          
          </div>
      </v-container>
      </div>

      <div class="about row" style="position:relative; top:55vh;">
      
      <v-card
      class="card"
      max-width="450"
    >
      <v-img
        src="../assets/services.jpg"
        height="300px"
      ></v-img>

      <v-card-title>
        Our Services
      </v-card-title>
      <v-card-text class="col-md-8 ml-5 text-right">
        We take the time to listen, understand and respond to customers' unique cleaning and hygiene needs.
      </v-card-text>

      <v-card-actions>
        <v-btn
          shaped
          color="primary"
        >
          View All
        </v-btn>
        
      </v-card-actions>
    </v-card>

    <v-card
      class="card"
      max-width="450"
    >
      <v-img
        src="../assets/wecare.jpg"
        height="300px"
      ></v-img>

      <v-card-title>
        We Care
      </v-card-title>
      <v-card-text class="col-md-8 ml-5 text-right">
        We are committed to a sustainable environment and that is why we design our products have the lowest total impact on the environment.
      </v-card-text>

      <v-card-actions>
        <v-btn
          shaped
          color="primary"
        >
          Find Out More
        </v-btn>
        
      </v-card-actions>
    </v-card>
    
    <v-card
      class="card"
      max-width="450"
    >
      <v-img
        src="../assets/whoweare.jpg"
        height="300px"
      ></v-img>

      <v-card-title>
        Who We Are 
      </v-card-title>
      <v-card-text>
        We are committed to providing viable and cost effective hygiene products, solutions and services for its customers across various sectors.
      </v-card-text>

      <v-card-actions>
        <v-btn
          shaped
          color="primary"
        >
          Learn More
        </v-btn>
        
      </v-card-actions>
    </v-card>

      </div>
    </div>
  </v-app>

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
            'LAUNDRY',
            'WATER TREATMENT',
            'SPECIALTIES',
        ],
        other_links: [
          'About Us',
          'Services',
          'Careers',
          'Contact Us'
        ]
      }
    },
  }
</script>
<style scoped>
.slides{
  position:absolute;
  top: -650px;
  height:500px;
}
.products{
    position:relative;
    top: 70vh;
}
.products_intro{
    background-color: #28b6e7;
    color:white;
    font-family: fantasy;
    height: 400px;
    width: 150px;
    margin: 40px;
    display:flex;
    border-radius: 15px 15px 15px 15px;
    display: inline-block;
    font-size:50px;
}
.products_header{
    position:relative;
    top:"200px";
    font-size: 7vh;
}
.product_image{
  width:100px;
  height:100px;
  position: relative;
  top:0px;
  left:60px;
}

.products_card{
    margin:5px;
    width:12vw;
    height:150px;
    background-color: #CCCCFF;
    display:flex;
}
.container{
  height:400px;
  display: flex
}
.container-fluid{
   position:relative;
   left:40px;
   top:30vh;
}
.card{
  position:relative;
  left:40px;
  top:20vh;
  max-width: 450;
}

@media only screen and (max-width: 768px) {
  .Main{
    position: relative;
    right: 0px;
    width: 800px;
  }
  .slides{
    position: relative;
    right: 0px;
    width: 400px;
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
  .container{
    height:auto;
    display: flex;
  }
  .about{
    height:auto;
    position: absolute;
    top:50vh;
  }
  .about{
    position: absolute;
    top:100vh;
  
  }
  .card{
  position:relative;
  left:20px;
  top:220vh;
  width: 90vw;
  margin: 10px;
}
}

/* screen size 375px */

@media only screen and (max-width: 375px) {
  
}

@media only screen and (max-width: 320px) {
  
}
</style>