<template>
  <v-app>
    <v-footer dark padless inset fluid class="footer">
    <div class="col-md-12 row" style="background-color:#0074a5; position:relative; left:12px">
      <div class="col-md-3">
        <v-app-bar-title class="ml-3" style="font-size:4vh;">Contact Us </v-app-bar-title>
        <div class="col-md-8" style="line-height: 1.5em;">
        <p style="font-size:1.7vh; color:black">
          MEDILAB AND ALLIED PRODUCTS (K)LTD,
          GENERAL WARUINGE ROAD,
          OLD RACE COURSE, STAREHE COURT 7638 (2),
          P.O BOX 14705-00400,
          NAIROBI, KENYA
          TEL: +254 721 811 499, +254 734 768
          110, +254 020 4401525, +254 774 768
          110
          EMAIL: sales@medilaballied.com
          info@medilaballied.com

          medilab.alliedproductsltd@gmail.com
        </p>
      </div>
      </div>

      <div class="col-md-3">
        <v-app-bar-title class="ml-3" style="font-size:4vh;">Product Range </v-app-bar-title>
        <div class="col-md-8" v-for="product in products_label" :key= product style="line-height:0.05em;">
        <p style="font-size:1.5vh; color:black">
          {{ product }}
        </p>
      </div>
      </div>

      <div class="col-md-3">
        <v-app-bar-title class="ml-3" style="font-size:4vh;">OTHER LINKS</v-app-bar-title>
        <div class="col-md-8" v-for="link in other_links" :key= link style="line-height:0.1em;">
        <p style="font-size:1.5vh; color:black"> {{ link }} </p>
      </div>
      </div>

      <div class="col-md-3">
        <v-app-bar-title class="ml-3" style="font-size:3vh;">SUBSCRIBE TO NEWSLETTER </v-app-bar-title>
        <div class="col-md-8">
        <v-text-field
            name="search"
            label="Search"
            placeholder= "search"
            height="5%"
            width= "30%"
            background-color="white"
            solo
          >
      </v-text-field>
        <v-text-field
            name="search"
            label="Search"
            placeholder= "Subscribe"
            height="5%"
            width= "50%"
            background-color="white"
            solo
          >
      </v-text-field>
        <button  class="btn btn-primary">SUBSCRIBE</button>

      </div>
      </div>

    </div>
    <div class="col-md-12 copyright text-center">
    <p> Copyright ©{{ new Date().getFullYear() }}. Medilab Allied Limited. All Rights Reserved.</p>
        
    </div>
    </v-footer>
    
    
  </v-app>
</template>
<style scoped>
.footer{
    width:100vw;
    position:relative;
    top:150vh;
    bottom:0px;
}
.copyright{
     background-color: #28b6e7;
     position:absolute;
     top:50vh;
  }

@media only screen and (max-width: 768px) {
  .footer{
    width:100vw;
    position:absolute;
    top:350vh;
    right: 10px;
    bottom:0px;
}
  .copyright{
     background-color: #28b6e7;
     position:absolute;
     top:175vh;
     left: 10px;
  }
}
</style>
<script lang="ts">
export default {
  name: 'Footer',
    data(){
      return{
        socials: ['SignUp','LogIn','Messenger', 'FacebookLite','Watch','People','Pages','Page   categories','Places','Games','Locations','Marketplace','FacebookPay','Groups','Jobs','Oculus','Portal','Instagram','Local','Fundraisers','Services','Voting Information Centre','About','Create ad' ,'Create Page','Developers','Careers','Privacy','Cookies','AdChoices','Terms','Help'],
        products_label: [
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
      };
    }
};
</script>
