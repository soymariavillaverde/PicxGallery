<template>
  <v-app>
    <PhotoCards/>
  </v-app>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import PhotoCards from '@/components/PhotoCards.vue'


export default {
  name: 'Home',
  components: {
    // HelloWorld,
    PhotoCards,
  },
}
</script>

