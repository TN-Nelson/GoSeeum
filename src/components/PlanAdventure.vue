<template>
  <v-card color="orange lighten-1">
    
      <h3 class="text-center pt-3">Plan Your GoSeeum Adventure</h3>
    
    <v-container >
     <v-row dense>
       <v-col v-for="card in cards" :key="card.title"  :cols="card.flex">
         <v-hover v-slot:default="{ hover }">
          <v-card align="center" :elevation="hover ? 12 : 2">
            <v-icon class= "text-center pa-3" large color="blue">{{card.value}}</v-icon>
            <p>{{card.text}}</p>
            <v-card-actions></v-card-actions>
          </v-card>
         </v-hover>
       </v-col>
     </v-row>
    </v-container>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    cards:[
      {title: 'map-marker', value: 'mdi-map-marker',text:'Suggested Locations', flex:4},
      {title: 'email', value: 'mdi-email',text:'Make a Reservation Inside of GoSeeum', flex:4},
      {title: 'account', value: 'mdi-account',text:'Create Your GoSeeum Tour List', flex:4},
    ]
      
  })
};
</script>

