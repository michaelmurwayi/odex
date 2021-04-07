<template>
    <v-app>
    <v-carousel hide-delimiters :controls="false" :show-arrows="false" :indicators="false" style=" background-color:red; height:600px;position:absolute; top:-16.5vh"
    >
    <v-carousel-item
      v-for="(item,i) in slides"
      :key="i"
      :src= "require('../assets/' + item)"
    >
    
    <v-card class="services_page">
        <v-card-title class="" style="position:relative; left:0px; top:20px; font-weight:bold; font-size: 8vh;">Services</v-card-title>
    </v-card>
    
    </v-carousel-item>
    </v-carousel>


    <div class="services col-md-12  row container-fluid"  v-for="service in services" :key="service">
        <ul style="">
            <li>
                {{ service  }}
            </li>
        </ul>
    </div>

    <div style="position:relative; top:85vh; right:0px; left:10px; font-size: 3.5vh;">

        <p> We are committed to doing this by:</p>
    </div>
    
    <div class="commitment" v-for="commit in commits" :key="commit" style="line-height: 55px;">
        <ul >
            <li style="margin-top:5vh;">
                {{ commit  }}
            </li>
        </ul>
    </div>
    
    </v-app>
</template>
<script>
export default {
     data () {
      return {
        slides: [
            'servicesmain.jpg',
            
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

.container{
  height:600px;
  display: "flex"
}
.services{
  position:relative;
  top:60vh;
  height: 30vh;
  font-size: 3.5vh;
  right:0px;
  left:10px;
  background-color: ;
  color: #787878;
  line-height: 55px;
}
.commitment{
    position:relative;
    top:80vh;
    font-size: 3.5vh;
    right:0px;
    left:10px;
    color: #787878;
    line-height: 55px;
}
.services_page{
    position:absolute;
    top:150px;
    left:650px;
    height:15vh;
    width: fit-content;
    background-color:#28b6e7;
    opacity:0.8;
  }
@media only screen and (max-width: 768px) {
    .services{
        position: relative;
        top:60vh;
        left: 10px;
        font-size: 2.5vh;
    }
    
    .services_page{
        position:absolute;
        top:150px;
        left:50px;
        height:15vh;
        width: fit-content;
        background-color:#28b6e7;
        opacity:0.8;
    }
}
</style>