<template>
  <v-container fluid>
    <v-row wrap >
      <v-col v-for="(data, index) in pokemons" :key="index" :cols="data.flex" class="content cardsWrapper" xs12 md4 lg3>
        <v-card class="cardContent">
          <v-img :src="data.img" class="pokemonPic"/>

          <div class="pokemonData">
            <div class="pokemonName">
              <v-card-title>
                <h4>{{data.name}}</h4>
              </v-card-title>

              <v-btn icon @click="favorite = !favorite">
                <v-icon color="red">{{ favorite ? "mdi-heart" : "mdi-heart-outline" }}</v-icon>
              </v-btn>
            </div>

            <div class="pokemonDescription">
              <div>
                <h5>Caption</h5>
                  <v-card-text>
                  Foto del primer {{data.name}} que encontré en mi ruta.
                </v-card-text>
              </div>
            </div>
          </div>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>

import axios from 'axios'

export default {
  name: 'PhotoCards',
  data() {
    return {
      show: false,
      favorite: false,
      pokemons: [],
    };
  },
/*   methods: {
    // ----------------------
  }, */
  created() {
      for(let i = 0; i <= 35; i++) {
        axios
          .get(`https://pokeapi.co/api/v2/pokemon/${i + 1}`)
          .then((response) => {
            //console.log('Todos los datos', response);
            
            let pokemon = {
              name: response.data.name,
              img: response.data.sprites.front_default,
            }
            this.pokemons.push(pokemon)
          })
          .catch((err) => {
            console.log(err);
          })
            // console.log('Arrray con pokemons', this.pokemons);
      }
  },
}
</script>

<style>
.height{
  height: 600 px;
}
</style>