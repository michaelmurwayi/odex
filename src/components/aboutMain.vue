<template>
    <v-app  style="position:absolute; top:170px; bottom:20vh; width:100%;">
    <div class="Main">
    <v-carousel hide-delimiters :controls="false" :indicators="false" :interval="3000" :show-arrows="false" direction="up" style="height:400px"
    >
    <v-carousel-item
      v-for="(item,i) in slides"
      :key="i"
      :src= "require('../assets/' + item)"
    >
    
    <v-card class="about_page" >
        <v-card-title class="" style="position:relative; left:0px; top:15px; font-weight:bold; font-size: 8vh;">About Medilab Allied</v-card-title>
    </v-card>
    
    </v-carousel-item>
    </v-carousel>
    </div>
    <div class="services col-md-12  row container-fluid"  style="position:relative; top:10vh; right:0px; left:0px;">
        <ul style="line-height: 5.0em;">
            <p style="font-size:4vh">
                Medilab & Allied Products K Ltd is a Kenyan company, which is committed to providing Medical and Research Reagents and Consumables, Water treatment chemicals, Cooling Tower/Boiler/Chiller chemicals and Condition Monitoring reagents/Sensors.
            </p>
        </ul>
    </div>
   
    <div class="row about-div">
        <div class="col-md-3 about">
            <v-card-title >Our Vision</v-card-title>
            <v-card-subtitle>
                To be Africa’s leading Manufacturer & Provider of Industrial Detergents & Hygiene Solutions.
            </v-card-subtitle>
        </div>
        <div class="col-md-3 about white">
            <v-card-title >Our Mission</v-card-title>
            <v-card-subtitle>
                To manufacture & supply quality Industrial Hygiene products with exceptional service at affordable prices.
                
            </v-card-subtitle>
        </div>
        <div class="col-md-3 about" >
            <v-card-title >Our Customers</v-card-title>
            <v-card-subtitle class="mt-5">
                <ul>
                    <li>
                    Power Plants
                    </li>
                    <li>
                    Research Institutions
                    </li>
                    <li>
                    Hospitals
                    </li>
                    <li>
                    Food Processors
                    </li>        
                </ul>
            </v-card-subtitle>
                Across East and West Africa
            <v-card-subtitle>
            </v-card-subtitle>
        </div>
        
    </div>
   
    </v-app>
</template>
<script>
export default {
     data () {
      return {
        slides: [
            'About_odex.jpg',
            
        ],
        services:[
            'Supply of quality food grade detergents to cater for all cleaning & hygiene needs.',
            'Preparation of a detailed cleaning manual for the factories to ensure a harmonized cleaning and hygiene system.',
            'Technical support to ensure good and consistent cleaning and hygiene results and to resolve quality challenges encountered from time to time.',
            'Analysis of utilities water( boilers, cooling towers, pasteurizers, ETP and process water treatment to confirm that the treatment regime are delivering the desired results.',
            'Quarterly trainings to ensure continuous improvement in the factories.',
            'Supply of high quality dosing and control equipment to ensure accurate and consistent dosing of the chemicals.',
            'Regular visit to the factory to monitor the cleaning and hygiene standards, and to identify any areas requiring urgent attention.',
            'Reports to the management indicating the levels of hygiene, cost trends against the budget, projects in progress and recommendations for improvements.',
            'Periodic audits for the entire factory to identify major improvement projects.'
            ],
        commits: [
            'Investing the time to listen, understand and respond to customers’ unique cleaning and hygiene needs.',
            'Taking a personal interest to ensure the facilities they care for are consistently clean, safe and attractive.',
            'Pursuing innovation in every form likely to make the lives of our customers simpler and more profitable.',
            'Customer collaborating to exceed their expectations, every day, everywhere.'
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
.about_page{
    position:absolute;
    top:150px;
    left:450px;
    height:15vh;
    width: fit-content;
    background-color:#28b6e7;
    opacity:0.8;
}
.products_card{
    margin-left:25px;
    margin-top: 10px;
    width:15vw;
    height:250px;
    background-color: #CCCCFF;
    display:flex;
}
.container{
  height:400px;
  background-color: red;
  display: "flex";
}
.about-div{
    position:absolute;
    top: 100vh;
    right:0px;
    left:100px;
    /* margin-bottom:40px; */
}
.about{
    width: 80%;
    /* margin: 20px; */
    height:300px;
    text-align:center;
    background-color:#909090;
}

@media only screen and (max-width: 768px) {
  .about_page{
    position:absolute;
    top:150px;
    font-size: 3vh;
    left:15px;
    height:15vh;
    width: fit-content;
    background-color:#28b6e7;
    opacity:0.8;
  }
  .about-div{
      position:relative;
      top:10vh;
      right:0px;
      left:40px;
      margin-bottom:40px;
  }
  .about{
    width: 80%;
    position: relative;
    left: 0px;
    height:300px;
    text-align:center;
    background-color:#909090;
}
}
</style>