<template>
  <v-app>
    <v-footer dark padless style="width:100vw position:absolute; top:95vh;">
    <div class="col-md-12" style="background-color:#0074a5;">

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
      };
    }
};
</script>

