<template>
  <v-app>
    <Header/>
    <v-main  style="padding-top:150px">
      <router-view/>
    </v-main>
    <Footer/>
  </v-app>
</template>

<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'


export default {
  name: 'App',
    components: {
    Header,
    Footer
  },

  data: () => ({
    //
  }),
};
</script>

<style lang="scss" src="./scss/main.scss"></style>
