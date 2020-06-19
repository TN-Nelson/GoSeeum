<template>
  <v-card color="orange lighten-1">
    
      <h3 class="text-center pt-3">Most Liked Pictures</h3>
    
    <v-container fluid>
      <v-row dense>
        <v-col v-for="card in cards" :key="card.title" :cols="card.flex">
          <v-card>
            <v-img
              :src="card.src"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="200px"
            >
              <v-card-title v-text="card.title"></v-card-title>
            </v-img>

            <v-card-actions>
              <v-spacer></v-spacer>
              <v-card-text>Number of Times Liked</v-card-text>
              <v-btn icon>
                <v-icon color="red">mdi-heart</v-icon>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>
<script>
export default {
  data: () => ({
    cards: [
      {
        title: "Picture of the Day",
        src: "https://cdn.vuetifyjs.com/images/cards/docks.jpg",
        flex: 4
      },
      {
        title: "Picture of the Week",
        src: "https://cdn.vuetifyjs.com/images/cards/mountain.jpg",
        flex: 4
      },
      {
        title: "Picture of the Month",
        src: "https://cdn.vuetifyjs.com/images/cards/cooking.png",
        flex: 4
      }
    ]
  })
};
</script>
