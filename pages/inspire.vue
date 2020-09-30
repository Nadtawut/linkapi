<template>
  <v-card
    class="mx-auto purple accent-1"

  >
    <v-toolbar
      color="blue"
    >
      <v-card-text class="text-center"><h1>Credit</h1></v-card-text>
    </v-toolbar>
    <v-container fluid>
      <v-row dense>
           <v-col cols="4">
        <v-card
        height="auto"
        class="mx-auto light-blue accent-1">
   <v-col md="12">
     <v-card>
          <v-img
      class="white--text align-end"
      height="200px"
     src="https://camo.githubusercontent.com/e923fa8162042f10df9bdee9190edff5f103658c/687474703a2f2f692e696d6775722e636f6d2f63746f4a334a702e706e67" 
    >
     <v-col
          cols="12"
          md="12"
        >
      <v-card class="orange black--text text-center">Anime API</v-card>
            </v-col>
    </v-img>
          </v-card>
          </v-col>
    <v-col md="12">
           <v-col cols="12 " align="center">
    <a href="https://jikan.docs.apiary.io/#reference" target="_blank">
   <v-btn
      class="ma-2"
      outlined
      color="indigo"
    >
      jikan api
    </v-btn>
    </a>
        </v-col>
          </v-col>
  </v-card>
        </v-col>
        <v-col cols="4">
        <v-card
        height="auto"
        class="mx-auto light-blue accent-1">
   <v-col md="12">
     <v-card>
          <v-img
      class="white--text align-end"
      height="200px"
     src="https://mindphp.com/images/knowledge/122560/vue.jpg" 
    >
     <v-col
          cols="12"
          md="12"
        >
      <v-card class="orange black--text text-center">Vuejs</v-card>
            </v-col>
    </v-img>
          </v-card>
          </v-col>
    <v-col md="12">
          <v-col cols="12 " align="center">
     <a href="https://vuejs.org/" target="_blank">
   <v-btn
      class="ma-2"
      outlined
      color="indigo"
    >
      Vuejs
    </v-btn></a>
        </v-col>
          </v-col>
  </v-card>
        </v-col>
             <v-col cols="4">
        <v-card
        height="auto"
        class="mx-auto light-blue accent-1">
   <v-col md="12">
     <v-card>
          <v-img
      class="white--text align-end"
      height="200px"
     src="https://madewithnetwork.ams3.cdn.digitaloceanspaces.com/spatie-space-production/3075/nuxtjs-2.jpg" 
    >
     <v-col
          cols="12"
          md="12"
        >
      <v-card class="orange black--text text-center">Nuxtjs</v-card>
            </v-col>
    </v-img>
          </v-card>
          </v-col>
    <v-col md="12">
          <v-col cols="12 " align="center">
     <a href="https://nuxtjs.org/" target="_blank">
   <v-btn
      class="ma-2"
      outlined
      color="indigo"
    >
      nuxtjs
    </v-btn></a>
        </v-col>
          </v-col>
  </v-card>
        </v-col>
      </v-row>
    </v-container>
       <v-col cols="12 " align="center">
     <nuxt-link :to="{name:'index'}">
   <v-btn
      class="ma-2"
      outlined
      color="indigo"
    >
      Manga Search
    </v-btn></nuxt-link>
        </v-col>
  </v-card>
</template>

<script>
</script>