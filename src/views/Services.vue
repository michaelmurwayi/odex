<template>
  <div class="" style="height:100vh;">
    <Navbar/>
    
    <div class="" style="height:50vh; position:relative; top:0px;">
    <Main/>
    </div>

    <Footer/>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Navbar from '@/components/Navbar.vue'; // @ is an alias to /src
import Main from '@/components/servicesMain.vue'
import Footer from '@/components/Footer.vue'


@Component({
  components: {
    Navbar,
    Main,
    Footer
  },
})
export default class Home extends Vue {}
</script>