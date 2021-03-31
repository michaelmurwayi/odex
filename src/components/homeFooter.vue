<template>
  <v-app>
    <v-footer dark padless inset fluid class="footer">
    <div class="col-md-12 row" style="background-color:#0074a5; position:relative; left:12px">
      <div class="col-md-3">
        <v-app-bar-title class="ml-3" >Contact Us </v-app-bar-title>
        <div class="col-md-8">
        <p>Lower Kabete Road
          Nairobi
          Kenya
          Telephone:+254 722 511 646 
          Email: info@medilab.co.ke
          Website: www.medilab.co.ke
      </p>
      </div>
      </div>

      <div class="col-md-3">
        <v-app-bar-title class="ml-3" >Product Range </v-app-bar-title>
        <div class="col-md-8" v-for="product in products_label" :key= product style="line-height:0.1em;">
        <p>
          {{ product }}
        </p>
      </div>
      </div>

      <div class="col-md-3">
        <v-app-bar-title class="ml-3" >OTHER LINKS</v-app-bar-title>
        <div class="col-md-8" v-for="link in other_links" :key= link style="line-height:0.1em;">
        <p> {{ link }} </p>
      </div>
      </div>

      <div class="col-md-3">
        <v-app-bar-title class="ml-3" >SUBSCRIBE TO NEWSLETTER </v-app-bar-title>
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
        <v-btn style="background-color:white; text-color:black;" aria-placeholder="SUBSCRIBE" class="white">SUBSCRIBE</v-btn>

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
    position:absolute;
    top:70vh;
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
    top:300vh;
    right: 10px;
    bottom:0px;
}
  .copyright{
     background-color: #28b6e7;
     position:absolute;
     top:163vh;
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
