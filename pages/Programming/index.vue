<template>
 <v-container mt-50 pt-50>
    <v-row class="white" style="height: auto;">
    <v-col v-for="b in articles" :key="b.slug" cols=auto>

      <v-card
      max-height="400"
      max-width="400"
      min-height="400"
      min-width="400"
      elevation="3"
      class="mx-auto"
      outlined
      :to=b.path
      >

      <v-img
        class="white--text align-end"
        height="200px"
        src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
      >
        <v-card-title>{{b.title}}</v-card-title>
      </v-img>

      <v-card-subtitle class="pb-0">
        {{b.date}}
      </v-card-subtitle>

      <v-card-text class="text--primary">
        <div>{{b.description}}</div>
      </v-card-text>
      </v-card>
      </v-col>
    </v-row>
 </v-container>  
</template>

<script>
export default {
  data(){
    return {
      path : this.$route.path ,
    }
  },
 async asyncData ({ $content }) {
   let query = $content('Programming')
   .sortBy('date', 'desc')
   const articles = await query.fetch() 
   return {
      articles
   }
  }
}
</script>


