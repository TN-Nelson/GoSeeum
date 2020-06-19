<template>
  <v-card  color="orange lighten-1">
    <div class="text-center my-3 py-3">
      <h3>Share Your GoSeeking</h3>
    
    
     
         
              
            <v-btn class="mx-3" v-for="card in cards" :key="card.title" x-large color="primary"  :href="card.src">
                <v-icon large class="ma-pa-3">{{card.value}}</v-icon>
                <v-card-text> {{card.text}} </v-card-text>
            </v-btn>
              
                
                    
    </div>      
            
          
    
  </v-card>
</template>

<script>
export default {
  data: () => ({
    cards:[
      {title: 'twitter', value: 'mdi-twitter',text:'Twitter', src: 'https://twitter.com/' },
      {title: 'instagram', value: 'mdi-instagram',text:'Instagram', src: 'https://www.instagram.com/'},
      
    ]
      
  })
};
</script>
