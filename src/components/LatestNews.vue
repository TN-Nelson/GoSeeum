<template>
  <v-card color="orange lighten-1" >
    <h3 class="text-center pt-3">Latest GoSeeum News</h3>
    <v-container fluid>
      <v-row dense>
        <v-col
          v-for="blog in blogs"
          :key="blog.id"
          :cols="blog.flex"
        >
          <v-card>
            <v-img
              :src="blog.src"
              class="white--text align-end"
              
              height="200px"
            >
              <v-card-title v-text="blog.title"></v-card-title>
            </v-img>

            <v-card-actions>
             <v-btn
        icon
        @click="show = !show"
      >
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
      <v-card-text> {{blog.name}} </v-card-text>
      <v-btn icon>
        <v-icon color="blue">mdi-message</v-icon>
        </v-btn>
        <v-card-text> ( {{blog.count}} )</v-card-text>
            </v-card-actions>
            
    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
        {{blog.text}}
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
      blogs: [
        {id: '1', title: '', src: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg', name:'John Doe', text:'Proident ea labore incididunt occaecat cillum aute do voluptate sunt. Fugiat ullamco ut quis esse ut occaecat amet veniam mollit aute irure excepteur. Dolor commodo ut ex in officia adipisicing duis. Commodo consequat qui cupidatat incididunt commodo do do aliquip occaecat consectetur enim ullamco. Pariatur et irure sint laborum do magna non aliqua ut minim sint et qui consectetur.', count: '4', flex: 4 },
        {id: '2', title: '', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 4},
        {id: '3', title: '', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 4 },
      ],
    }),
  }
</script>