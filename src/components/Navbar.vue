<template>
  <v-container>
    <v-app>
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
            style="position:relative; top:15px; width:20%; border-radius: 15px 15px 15px 15px;"
          >
    </v-text-field>
    
    <v-toolbar color="white" elevation="0" style="position:absolute; top:8vh; left:0px; right:0px; height:20vh">
    <div class="col-md-6">
        <v-img
            width="40vw"
            height="15vh"
            class="col-md-6"
            src= "../assets/logo.png"
            style="position:relative; top:5.5vh;"
    ></v-img>
    </div>
    <div class="col-md-6">

    <v-list style="height:100px; position:relative; top:6vh; background: Transparent;" >
    <v-row align="end">

        <v-list-item-content class="text-black">
        <v-list-item class="text-black"><router-link class="nav"  to=""> Home </router-link></v-list-item>
        </v-list-item-content>
       
        <v-list-item-content class="text-black">
        <v-list-item class="text-black"><router-link class="nav"  to=""> Products </router-link></v-list-item>
        </v-list-item-content>

        <v-list-item-content class="text-black">
        <v-list-item class="text-black"><router-link class="nav"  to=""> Services </router-link></v-list-item>
        </v-list-item-content>

        <v-list-item-content class="text-black">
        <v-list-item class="text-black"><router-link class="nav"  to=""> New & Events </router-link></v-list-item>
        </v-list-item-content>

        <v-list-item-content class="text-black">
        <v-list-item class="text-black"><router-link class="nav"  to=""> About us </router-link></v-list-item>
        </v-list-item-content>

        <v-list-item-content class="text-black">
        <v-list-item class="text-black"><router-link class="nav"  to=""> Contact Us </router-link></v-list-item>
        </v-list-item-content>
          

    </v-row>
    </v-list>
    </div>
    </v-toolbar>
    </v-app-bar>
  </v-app>
  </v-container>
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
    color: black;
    text-decoration: none;
}

</style>
