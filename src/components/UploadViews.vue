<template>
  <v-card class="text-center pt-3">
    

    <v-container fluid>
      <v-row dense>
        <v-col
          v-for="card in cards"
          :key="card.title"
          :cols="card.flex"
          
        >
          <v-card :color="card.color" class="text-center ma-3 pa-3">
          
            <h3> {{card.title}} </h3>
             <p class="white--text"> {{card.amount}} </p>
            
          
            
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
        { title: 'Uploaded Content', color: 'orange lighten-1', amount: '275', flex: 6 },
        { title: 'Daily Views', color: 'blue', amount: '39', flex: 6 },
      ]
    }),
  }
</script>