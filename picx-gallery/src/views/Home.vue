<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <PhotoCard/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import PhotoCard from '@/components/PhotoCard.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    PhotoCard
  },
  /* data() {
    return {
     
    };
  }, */
//methods: {
    //  ----------------------
  // }
}
</script>

