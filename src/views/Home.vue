<template>
  <div class="home">
    <Navbar/>
    <Footer/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Navbar from '@/components/Navbar.vue'; // @ is an alias to /src
import Footer from '@/components/Footer.vue'

@Component({
  components: {
    Navbar,
    Footer
  },
})
export default class Home extends Vue {}
</script>
