<template>
  <v-app>
    <v-footer dark padless inset fluid class="footer">
    <div class="col-md-12 row" style="background-color:rgba(66, 26, 76); position:relative; left:12px">
      <div class="col-md-4">
        <v-app-bar-title class="ml-3" style="font-size:4vh;">Contact Us </v-app-bar-title>
        <div class="col-md-8" style="line-height: 2.0em;">
        <p style="font-size:2vh; color:#28b6e7;">
          MEDILAB AND ALLIED PRODUCTS (K)LTD,
          GENERAL WARUINGE ROAD,
          OLD RACE COURSE, STAREHE COURT 7638 (2),
          P.O BOX 14705-00400,
          NAIROBI, KENYA
        </p>
        <p>
          <strong> Tel: </strong>
          <ul>
          <li>
          <a href="tel:http://+254721811499" style="color:white;">+254721811499</a>, 
          </li>

          <li>
          <a href="tel:http://+254 734 768110" style="color:white;">+254 734 768110</a>,
          </li>

          <li>
          <a href="tel:http://+254 020 4401525" style="color:white;">+254 020 4401525</a>
          </li>
          </ul>
        </p>
          <p> <strong>Email:</strong></p>
          <ul>
          <li>

          <a href="mailto:http://sales@medilaballied.com" style="color:white;">sales@medilaballied.com</a>
          </li>
          <li>

          <a href="mailto:http://medilab.alliedproductsltd@gmail.com" style="color:white;">medilab.alliedproductsltd@gmail.com</a>
          </li>
          </ul>
      </div>
      </div>

      <div class="col-md-4">
        <v-app-bar-title class="ml-3" style="font-size:4vh;">Product Range </v-app-bar-title>
        <div class="col-md-8" v-for="product in products_label" :key= product style="line-height:0.05em;">
        <p style="font-size:1.5vh; color:#28b6e7">
          {{ product }}
        </p>
      </div>
      </div>

      <div class="col-md-4">
        <v-app-bar-title class="ml-3" style="font-size:4vh;">OTHER LINKS</v-app-bar-title>
        <div class="col-md-8" v-for="link in other_links" :key= link style="line-height:0.1em;">
        <p style="font-size:1.5vh; color:#28b6e7"> {{ link }} </p>
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
    height: fit-content;
    top:700px;
    font-family: cursive;
}
.copyright{
     background-color: black;
     position:absolute;
     top: 65vh;
  }
  .links{
  color: white;
}
a{
  color: black;
}

@media only screen and (max-width: 768px) {
  .footer{
    width:100vw;
    position:absolute;
    top: 1500px;
    right: 10px;
    bottom:0px;
    font-family: cursive;
}
  .copyright{
     background-color: black;
     position:absolute;
     top: 1140px;
     left: 10px;
  }
  .links{
  color: white;
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
