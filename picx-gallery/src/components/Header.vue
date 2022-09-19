<template>
<v-app-bar class="backgroundHeader" fluid  app>
      <div wrap class="contentHeader">
          <v-img
            alt="PicxGallery logotype"
            class="shrink"
            src="@/assets/logo.png"
            width="250"
          />
        <div class="views" xs4 lg2>
          <div>
            <router-link to="/"> Pictures </router-link>
          </div>
          <div>|</div>
          <div>
            <router-link to="/favorites"> Favorites </router-link>
          </div>
        </div>
      </div>
    </v-app-bar>
</template>