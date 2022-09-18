<template>
<v-app>
  <v-container>
    <v-layout wrap>
      <v-flex xs12 >
        <h1>prueba</h1>
        <div class="home">
          <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
          <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
          <PhotoCard/>
        </div>
      </v-flex>
    </v-layout>
  </v-container>
</v-app>

</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import PhotoCard from '@/components/PhotoCard.vue'

export default {
  name: 'Home',
  components: {
    // HelloWorld,
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

