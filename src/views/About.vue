<template>
  <div class="" >
    <Navbar/>
    
    <Main/>

    <Footer/>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Navbar from '@/components/Navbar.vue'; // @ is an alias to /src
import Footer from '@/components/Footer.vue'
import Main from '@/components/aboutMain.vue'

@Component({
  components: {
    Navbar,
    Main,
    Footer
  },
})
export default class Home extends Vue {}
</script>