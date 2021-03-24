<template>
    <v-app  style="position:relative; top:-650px; bottom:20vh; width:100%;">
    <div class="Main">
    <v-carousel hide-delimiters :controls="false" :indicators="false" :interval="3000" direction="up" style="height:300px"
    >
    <v-carousel-item
      v-for="(item,i) in slides"
      :key="i"
      :src= "require('../assets/' + item)"
    >
    
    <v-card class="" style=" postion:absolute; top:100px; left:650px; height:15vh; width: fit-content; background-color:#28b6e7; opacity:0.8;">
        <v-card-title class="" style="position:relative; left:0px; top:20px; font-weight:bold; font-size: 8vh;">Products</v-card-title>
    </v-card>
    
    </v-carousel-item>
    </v-carousel>
    </div>
    </v-app>
</template>
<script>
export default {
     data () {
      return {
        slides: [
            'products_intro.jpg',
            
        ],
      
}
     }
     }
</script>

<style scoped>

</style>