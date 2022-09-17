<template>
  <div class="content">Este será el template para cada tarjeta de pokemon
    <div v-for="(data, index) in pokemons" :key="index">
      <v-app id="inspire" class="height">
        <v-card
          class="mx-auto"
          max-width="344"
        >
          <v-img
            :src="data.img"
            height="200px"
          ></v-img>

          <v-card-title>
            {{data.name}}
          </v-card-title>

          <v-card-actions>
            <v-btn
              color="orange lighten-2"
              text
            >
              Caption
            </v-btn>

            <v-spacer></v-spacer>
              <v-btn
              icon
              @click="show = !show"
            >
              <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
            </v-btn>
          </v-card-actions>

          <v-expand-transition>
            <div v-show="show">
              <v-divider></v-divider>
              <!-- <v-card-text>
              </v-card-text> -->
            </div>
          </v-expand-transition>
        </v-card>
      </v-app>
    </div>
  </div>
</template>

<script>

import axios from 'axios'

export default {
  name: 'PhotoCard',
  data() {
    return {
      show: false,
      pokemons: [],
    };
  },
/*   methods: {
    // ----------------------
  }, */
  created() {
      for(let i = 0; i <= 50; i++) {
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