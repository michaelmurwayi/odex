<template>
    <v-app class="col-md-10" style="height:150px">
    <v-app-bar
      app
      color="#28b6e7"
      dark
      elevation="0"
      height="60vh"
    >
    
      <v-spacer></v-spacer>
    <div class="mt-5 mr-5">
    <p>Careers</p>

    </div>
    <v-text-field
            name="search"
            label="Search"
            placeholder= "search"
            height="5%"
            background-color="white"
            solo
            prepend-icon= "mdi-magnify" class="shrink"
            style="position:relative; top:15px; right:10px; width:20%; border-radius: 15px 15px 15px 15px;"
          >
    </v-text-field>
    

    <v-toolbar color="white" elevation="0" style="position:absolute; top:60px; left:0px; right:0px; height:18vh">
    <div class="col-md-6">
        <v-img
            width="20vw"
            height="9vh"
            class="col-md-6"
            src= "../assets/logo.png"
            style="position:relative; top:5.5vh;"
    ></v-img>
    </div>
    <div class="col-md-6">

    <v-list class="navigate white">
    <v-row>

        <v-list-item-content>
        <v-list-item ><router-link class="nav"  to="/"> Home </router-link></v-list-item>
        </v-list-item-content>
       
        <v-list-item-content >
        <v-list-item ><router-link class="nav"  to="Products"> Products </router-link></v-list-item>
        </v-list-item-content>

        <v-list-item-content >
        <v-list-item ><router-link class="nav"  to="Services"> Services </router-link></v-list-item>
        </v-list-item-content>
  

        <v-list-item-content >
        <v-list-item ><router-link class="nav"  to="about"> About us </router-link></v-list-item>
        </v-list-item-content>

        <v-list-item-content >
        <v-list-item ><router-link class="nav"  to=""> Contact Us </router-link></v-list-item>
        </v-list-item-content>
          

    </v-row>
    </v-list>
    </div>
    </v-toolbar>
    </v-app-bar>
  </v-app>

</template>

<script lang="ts">
  import Vue from 'vue'

  export default Vue.extend({
    name: 'Navbar',

    data: () => ({
    
    }),
  })
</script>
<style scoped>

.nav {
    color: #28b6e7;
    text-decoration: none;
    width: fit-content  ;
}

.navigate{
    height:100px;
    position:relative;
    right: 10px;
    top:6vh;
    background: Transparent;
}
@media only screen and (max-width: 768px) {
  .navigate{
    height:80px;
    font-size: 10px;;
    position:relative;
    right: 50px;
    top:8vh;
    background: Transparent;
} 
}
</style>
