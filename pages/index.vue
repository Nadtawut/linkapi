<template>
<div>
   <div>
  <v-card>
    <v-toolbar color="blue" dark flat>
      <v-text-field
        class="mx-4"
        flat
        hide-details
        label="Manga Name"
        prepend-inner-icon="mdi-magnify"
        solo-inverted
        v-model="textSearch">
         </v-text-field>
         <v-btn depressed large color="error" @click="searchData()">Search</v-btn>
    </v-toolbar>
  </v-card>
  </div>
  <br>
      <v-card
    class="mx-auto blue accent-1"
  >
    <v-app-bar
      color="pink"
   >
 <h1>Manga List</h1>
    </v-app-bar>
    <v-container>
      <v-row dense >
        
        <v-col cols="12" v-for="data in List" 
    :key="data.mal_id">
    
          <v-card>
          <v-img
      class="white--text align-end"
      height="300px"
      :src="data.image_url"
    >
    <v-col
          cols="12"
          md="3"
        >
      <v-card class="orange black--text text-center">{{data.title}}</v-card>
            </v-col>
    </v-img>
    <v-col
          cols="12"
          md="1"
        >
            <v-card class="pink text-center">Sample</v-card>
              </v-col>
            <v-card-text class="text--primary">
            <div class="blue--text">Type  : {{data.type}}</div>
            <div class="cyan--text">Score : {{data.score}}</div>
             </v-card-text>
            <v-card-actions >
              <nuxt-link :to="{name:'manga-detail',
              params: { title:data.title, 
                        img:data.image_url ,
                        info:data.synopsis,
                        type:data.type,
                        ep:data.chapters,
                        sc:data.score,
                        str:data.start_date,
                        end:data.end_date
              }} ">
              <v-btn depressed large color="pink" text>Details</v-btn></nuxt-link>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</div>
</template>
<script>
import axios from "axios";
  export default {
    data () {
      return {
        List: null,
        tabs: null,
        textSearch: "",
      }; 
      
    },
    methods: {
    searchData() {
      axios
       .get("https://api.jikan.moe/v3/search/manga?q="+this.textSearch+"&limit=15")
        .then((response) => {
          this.List = response.data.results;
        })
        .catch((err) => {
          console.log(err);
        });

    },
  },
  }
</script>