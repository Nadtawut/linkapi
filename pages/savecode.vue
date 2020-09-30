<template>
  <v-card
    class="mx-auto purple accent-1"

  >
    <v-toolbar
      color="blue"
    >
      <v-card-text class="text-center"><h1>Detail</h1></v-card-text>
    </v-toolbar>
    <v-container fluid>
      <v-row dense>
        <v-col cols="4">
        <v-card
    class="mx-auto "
  >

    <v-img
      class="white--text align-end"
      height="auto"
      :src="this.manga.img"  
    >
     <v-col
          cols="12"
          md="12"
        >
      <v-card class="orange black--text text-center">{{this.manga.title}}</v-card>
            </v-col>
    </v-img>
  </v-card>
        </v-col>
        <v-col cols="8">
        <v-card
        height="auto"
        class="mx-auto light-blue accent-1">
   <v-col md="6"><v-card>
          <v-card-text class="red--text">Manga : {{this.manga.title}}</v-card-text>
          </v-card>
          </v-col>
  <v-col md="12"><v-card>
          <v-card-text class="pink--text">synopsis :</v-card-text>
          <v-card-text class="orange--text">{{this.manga.info}}</v-card-text>
          </v-card>
          </v-col> 
    <v-col md="12">
          <v-card>
          <v-card-text class="orange--text">Type : {{this.manga.type}}</v-card-text>
          <v-card-text class="orange--text">Chapters : {{this.manga.ep}}</v-card-text>
          <v-card-text class="orange--text">Score : {{this.manga.sc}}</v-card-text>
          <v-card-text class="pink--text">Start-chapter : {{this.manga.str}}</v-card-text>
          <v-card-text class="red--text">end-chapter : {{this.manga.end}}</v-card-text>
          </v-card>
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
  export default {
    data(){
  return{
    manga: this.$route.params,
  }
},

  }
  
</script>