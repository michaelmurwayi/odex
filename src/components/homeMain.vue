<template>
  <v-app>
    <div class="Main" style=" position:absolute; top:-130px; width:100%;">
    <v-carousel
    cycle
    
    height="800"
    hide-delimiter-background
    show-arrows-on-hover
    :show-arrows="false"
    >
    <v-carousel-item
        v-for="(slide, i) in slides"
        :key="i"
      >
        <v-sheet
          color="black"
          height="100%"
        >
          <v-row
            class="fill-height"
            align="center"
            justify="center"
          >
            <div class="display-3">
              <v-img
                :src= "require('../assets/' + slide)"
                height="800px"
                width="100vw"
              ></v-img>
            </div>
            <div class="display-4 ">
              
              <v-carousel
              height="300" 
              cycle 
              hide-delimiters
              show-arrows-on-hover
              :show-arrows="false"
              >
              <v-carousel-item
                v-for="(header) in headers"
                :key="header"
                reverse-transition="fade-transition"
                transition="fade-transition"
              >
              
              <h2 style="font-size:8vh; margin-left:5vw;"> {{ headers[i].header }} </h2>
              <p style="font-size:4vh; margin-left:5vw;"> {{ headers[i].text }} </p>
              
              <v-btn style=" background-color:white; color:  rgba(0, 116, 165, 0.6); font-size:3vh; margin-left:5vw; position:relative; top: -40px; "> learn More </v-btn>
              </v-carousel-item>
            </v-carousel>
            </div>
          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
    </div>
    
    <div class="products col-md-12 row container-fluid">
      <div class="products_intro col-md-2" >
        <p class="products_header"> Our Product Range </p>
      </div>
      
      <v-container class="col-md-9 ml-1 row container">
        <div v-for="(product, index) in products" :key="product"  style="position:relative; top:0vh">
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

      <div class="about row " style="position:absolute; top:150vh; right:10px; left:10px; background-position: 0 0; background-size: 100vw 100vh;">
      
      <v-card
      class="card"
      max-width="450"
      shaped
      style="box-shadow: 5px 5px 5px 5px grey;"
    >
      <v-img
        src="../assets/services.jpg"
        height="300px"
      ></v-img>

      <v-card-title>
        Our Services
      </v-card-title>
      <v-card-text class="col-md-12 text-justified">
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
      shaped
      style="box-shadow: 5px 5px 5px 5px grey;"
    >
      <v-img
        src="../assets/wecare.jpg"
        height="300px"
      ></v-img>

      <v-card-title>
        We Care
      </v-card-title>
      <v-card-text class="col-md-12 text-justified">
        We are committed to a sustainable environment and that is why we design our products have the lowest total impact on the environment.
      </v-card-text>

      <v-card-actions>
        <v-btn
          shaped
          color="primary"
          right
        >
          Find Out More
        </v-btn>
        
      </v-card-actions>
    </v-card>
    
    <v-card
      class="card"
      max-width="450"
      shaped 
      style="box-shadow: 5px 5px 5px 5px grey;"
    >
      <v-img
        src="../assets/whoweare.jpg"
        height="300px"
      ></v-img>

      <v-card-title>
        Who We Are 
      </v-card-title>
      <v-card-text class="col-md-12 text-justified">
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
        ],
         headers: [
          { 
            header: 'wide Range of Products',
            text: "Check out our conveyor Lubes"
          },
          { 
            header: 'We are the Hygiene Solution',
            text: "we have a wide range of Housekeeping Products"
          },
          { 
            header: '25 years of Experience',
            text: "we manufacture specialized detergents and sanitation products"
          },
      ]
      }
    },
  }
</script>
<style scoped>
.display-4{
  position:absolute;
  opacity: ;
  top: 150px;
  left: 0px;
  background-color: rgba(0, 116, 165, 0.6);
  height:auto;
  width: 60vw;
  font-size: 1vh;
}

.products{
    position:absolute;
    background-color:;
    margin-top: 670px;
}
.products_intro{
    background-color: #28b6e7;
    color:white;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    height: 400px;
    width: 150px;
    margin-left: 50px;
    display:flex;
    border-radius: 15px 15px 15px 15px;
    display: inline-block;
    font-size:50px;
}
.products_header{
    position:relative;
    top:"50px";
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
    width:15vw;
    height:150px;
    background-color: #CCCCFF;
    display:flex;
}
.container{
  height:400px;
  display: flex
}

.card{
  position:relative;
  left:40px;
  top:vh;
  margin: 30px;
  max-width: 450;
}

@media only screen and (max-width: 768px) {
  .Main{
    position: relative;
    right: 0px;
    width: 100vw;
  }
  .slides{
    position: relative;
    right: 0px;
    width: 400px;
  }
  .products{
    background-color: white ;
    position: absolute;
    top:120vh;
    left: 0px;
  }
  .products_intro{
    background-color: #28b6e7;
    height: 80px;
    width: 100vw;
    margin-top: 25px;
    margin-left: 15px;
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
    width:80vw;
    height:25vh;
    background-color:#E8E8E8;
    display:flex;
    margin-left: 30px;
  }
  .product_image{
  width:100px;
  height:100px;
  position: relative;
  top:0px;
  left:80px;
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
  position:absolute;
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