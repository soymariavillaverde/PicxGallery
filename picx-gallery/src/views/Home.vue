<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
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
  methods: {
    // vinculo aquí la API porquue es la vista que va a recibir las tarjetas
    loadPokeAPI() {
      var url = "https://pokeapi.co/api/v2/pokemon";
      return fetch(url)
        .then((res) => res.json())
        .then((data) => {
          this.characters = data.data;
        });
    },
  },
  created() {
    this.loadPokeAPI();
  },
}
</script>

