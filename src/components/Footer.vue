<template>
  <v-app>
    <v-footer dark padless style="width:100vw; position:absolute; top:80vh; bottom:0px;">
    <div class="col-md-12 row" style="background-color:#0074a5;">
      <div class="col-md-3">
        <v-app-bar-title class="ml-3" >Contact Us </v-app-bar-title>
        <div class="col-md-8">
        <p>Odex Chemicals Limited,
          Kyang’ombe Road, Off Mombasa Road,
          Behind Ramtons, Opposite Clique,
          P.O Box 72390 – 00200,
          Nairobi, Kenya.
          Tel: 020-2347131/32
          Mobile: 0713064662
          Email: info@odexchem.co.ke
      </p>
      </div>
      </div>

      <div class="col-md-3">
        <v-app-bar-title class="ml-3" >Product Range </v-app-bar-title>
        <div class="col-md-8" v-for="product in products_label" :key= product style="line-height:0.1px;">
        <p>
          {{ product }}
        </p>
      </div>
      </div>

      <div class="col-md-3">
        <v-app-bar-title class="ml-3" >OTHER LINKS</v-app-bar-title>
        <div class="col-md-8" v-for="link in other_links" :key= link style="line-height:0.1px;">
        <p> {{ link }} </p>
      </div>
      </div>

      <div class="col-md-3">
        <v-app-bar-title class="ml-3" >SUBSCRIBE TO NEWSLETTER </v-app-bar-title>
        <div class="col-md-8">
        <p>Odex Chemicals Limited,
          Kyang’ombe Road, Off Mombasa Road,
          Behind Ramtons, Opposite Clique,
          P.O Box 72390 – 00200,
          Nairobi, Kenya.
          Tel: 020-2347131/32
          Mobile: 0713064662
          Email: info@odexchem.co.ke
      </p>
      </div>
      </div>

    </div>
    <div class="col-md-12 text-center" style="background-color: #28b6e7">
    <p> Copyright © 2020. Odex Chemicals Limited. All Rights Reserved.</p>
        
    </div>
    </v-footer>
    
    
  </v-app>
</template>
<style scoped>

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

