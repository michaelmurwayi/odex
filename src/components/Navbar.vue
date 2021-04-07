<template>
    <v-app class="col-md-10" style="height:150px">
    <v-app-bar
      app
      color="#28b6e7"
      dark
      elevation="10"
      height="50vh"
    >
    
      <v-spacer></v-spacer>
    <v-toolbar color="white" elevation="0" style="position:absolute; top:50px; left:0px; right:0px; height:15vh">
    <div class="col-md-6">
        <v-img
            width="30vw"
            height="8vh"
            class="logo col-md-6"
            src= "../assets/logo.png"
    ></v-img>
    </div>
    <div class="col-md-6">

    <v-list class="navigate white">
    <v-flex class="subnav-content">
        <div class="nav-content">
          <div class="navlinks"><router-link to="/">Home</router-link></div>
          <div class="navlinks"><router-link to="products"> Products</router-link></div>
          <div class="navlinks"><router-link to="services"> Services</router-link></div>
          <div class="navlinks"><router-link to="about"> About Us</router-link></div>
        </div>
      </v-flex>
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
    width: 15px;
}
.logo{
  position:relative;
  top:4vh;
}
.search {
  position:relative;
  top:15px;
  right:10px;
  width:20%;
  border-radius: 15px 15px 15px 15px;
}
.v-text-field{
      width: 1px;
}
.navigate{
    height:100px;
    position:relative;
    right: 10px;
    top:4vh;
    background: Transparent;
}
#subnav {
  width: 100vw;
  background: white;
  height: 120px;
  display: flex;
  align-items: flex-end;
  position: relative;
  right: 10px;
  justify-content: center;
}
.subnav-content {
  color: #fff;
  /* padding: 10px 35px; */
  position: relative;
  text-align: center;
  border-bottom: 3px solid transparent;
  display: flex;

  margin-right: 0;
  right: 0px;
  margin-left: 00px;
}
.nav-content {
  color: #fff;
  padding: 10px 20px;
  position: relative;
  text-align: center;
  border-bottom: 3px solid transparent;
  display: flex;
  left: 0;
  padding: auto;
}
.navlinks {
  color: #fff;
  padding: 1px 20px;
  position: relative;
  text-align: center;
  border-bottom: 1px solid transparent;
  display: flex;
  float: right;
  transition: width 4.4s;
}
a {
  text-decoration: none;
  color: blue;
}
.navlinks.active,
a:hover,
.navlinks:hover {
  color: #00aeff;
  border-bottom-color: #00aeff;
  transition: width 2.4s linear;
  transition-property: border-bottom;
}

@media only screen and (max-width: 768px) {
  .logo{
  position:relative;
  top:2vh;
}
  .navigate{
    height:30px;
    width: 100vw;
    font-size: 2.5vw;
    position:relative;
    right: 150px;
    padding-left: px;
    top:8vh;
    
}
  .nav{
    position: relative;
    right: 10px;
  }

.nav-content {
  color: #fff;
  padding: 10px 20px;
  position: relative;
  text-align: center;
  border-bottom: 3px solid transparent;
  display: flex;
  right: 150px;
  padding: auto;
}

}
</style>
