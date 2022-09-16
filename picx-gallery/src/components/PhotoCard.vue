<template>
    <div>Este será el template para cada tarjeta de pokemon/
     <div class="card" style="width: 18rem;">
            <img class="card-img-top" src="@/assets/prueba.png" alt="Card image cap">
            <div class="card-body">
                <h5 class="card-title font-weight-500">Card title</h5>
                <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
            </div>
        </div>
        <!-- <ul class="list-group">
            <li class="list-group-item d-flex justify-content-between align-items-center">
                <img src="@/assets/prueba.png" class="rounded-4 w-25 h-25"
              alt="imagen" />
                Cras justo odio
                <span class="badge badge-primary badge-pill">14</span>
            </li>
            <li class="list-group-item d-flex justify-content-between align-items-center">
                Dapibus ac facilisis in
                <span class="badge badge-primary badge-pill">2</span>
            </li>
            <li class="list-group-item d-flex justify-content-between align-items-center">
                Morbi leo risus
                <span class="badge badge-primary badge-pill">1</span>
            </li>
        </ul>    -->
    </div>
</template>

<script>

import axios from 'axios'

export default {
  name: 'PhotoCard',
  data() {
    return {
      pokemons: [],
      pokemon: {
        name: "",
        img: ""
      }
    };
  },
/*   methods: {
    // ----------------------
  }, */
  created() {
    axios
      .get('https://pokeapi.co/api/v2/pokemon/1')
      .then((response) => {
        // console.log(response.data);
        this.pokemon.name= response.data.name
        this.pokemon.img= response.data.sprites.front_shiny
        this.pokemons.push(this.pokemon)
      })
      .catch((err) => {
        console.log(err);
      })
        console.log('Arrray con pokemons', this.pokemons);
  },
}
</script>

<style>

</style>