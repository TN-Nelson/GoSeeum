<template>
  <v-card color="orange lighten-1" >
    <h3 class="text-center pt-3">What People Say About Attractive Locations</h3>
    <v-container fluid>
      <v-row dense>
        <v-col
          v-for="review in reviews"
          :key="review.id"
          :cols="review.flex"
        >
          <v-card>
            <v-img
              :src="review.src"
              class="white--text align-end"
              height="100px"
              width="100px"
              >
              
              <v-card-title v-text="review.title"></v-card-title>
            </v-img>

            <v-card-actions>
             <v-btn 
        icon
        @click="show = !show"
      >
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
      <v-card-text> {{review.name}} </v-card-text>
      
        <v-card-text> {{review.date}} </v-card-text>
            </v-card-actions>
            
    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
        {{review.text}}
        </v-card-text>
      </div>
    </v-expand-transition>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
        show: false,
      reviews: [
        {id: '1', title: '', src: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg', name:'John Doe', text:'Proident ea labore incididunt occaecat cillum aute do voluptate sunt. Fugiat ullamco ut quis esse ut occaecat amet veniam mollit aute irure excepteur. Dolor commodo ut ex in officia adipisicing duis. Commodo consequat qui cupidatat incididunt commodo do do aliquip occaecat consectetur enim ullamco. Pariatur et irure sint laborum do magna non aliqua ut minim sint et qui consectetur.', date: '9/20/16', flex: 4 },
        {id: '2', title: '', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg',  flex: 4},
        {id: '3', title: '', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg',  flex: 4 },
      ],
    }),
  }
</script>