<template>
  <v-app>
    
    <v-content>
      <PopularCategories/>
      <GoSeeker/>
      <PlanAdventure/>
      <LatestNews/>
      <LikedPics/>
      <UploadViews/>
      <PeopleReviews/>
      <AvailableOptions/>
      <ShareYours/>
      <SubscribeGoseek/>
      <ProductContact/>
    </v-content>
    <v-footer app>
    <v-spacer></v-spacer>
    <div class="black--text">&copy; GoSeeum All Rights Reseved{{ new Date().getFullYear() }}</div>
  </v-footer>
   
  </v-app>
</template>

<script>
import PopularCategories from './components/PopularCategories.vue';
import GoSeeker from './components/GoSeeker.vue';
import PlanAdventure from './components/PlanAdventure.vue';
import LatestNews from './components/LatestNews.vue';
import LikedPics from './components/LikedPics.vue';
import UploadViews from './components/UploadViews.vue';
import PeopleReviews from './components/PeopleReviews.vue';
import AvailableOptions from './components/AvailableOptions.vue';
import ShareYours from './components/ShareYours.vue';
import SubscribeGoseek from './components/SubscribeGoseek.vue';
import ProductContact from './components/ProductContact.vue';
export default {
  name: 'App',

  components: {
    PopularCategories, GoSeeker, PlanAdventure, LatestNews, LikedPics, UploadViews, PeopleReviews, AvailableOptions, ShareYours,
    SubscribeGoseek, ProductContact
  },

  data: () => ({
    //
  }),
};
</script>
