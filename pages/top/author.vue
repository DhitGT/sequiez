<template>
  <div>
    <div class="flex appTop">
      <div class="flex items-center gap-2">
        <v-btn icon>
          <v-icon>mdi-arrow-left</v-icon>
        </v-btn>
        <span class="font-bold"> Top Authors </span>
      </div>
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
    </div>
    <div class="appBody mt-3 flex gap-5 flex-col items-center md:items-start">
      <div class="flex w-screen " v-for="(item,i) in items" :key="'author-' + i" style="max-width:100%; cursor:pointer" >
        <div class="w-12 rounded-full overflow-hidden">
          <v-img :src="item.image"></v-img>
        </div>
        <div class="flex flex-col justify-center px-3">
          <span class="font-bold text-sm md:text-lg">{{item.name}}</span>
          <span class="text-xs md:text-md">@{{item.username}}</span>
        </div>
        <div
          class="flex items-center justify-end rounded-lg selection:overflow-hidden"
        >
          <v-btn style="text-transform: none;" rounded="lg" :outlined="item.followed" :small="!isSmallScreen" :x-small="isSmallScreen" color="#6949ff" class="ma-0"> {{ item.followed? 'Following' : 'Follow'}} </v-btn>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          'image' : 'https://placehold.co/300',
          'name' : 'udin suzume',
          'username' : 'szme_din'
        },
        {
          'image' : 'https://placehold.co/300',
          'name' : 'udin suzume',
          'username' : 'szme_din'
        },
        {
          'image' : 'https://placehold.co/300',
          'name' : 'udin suzume',
          'username' : 'szme_din'
        },
        {
          'image' : 'https://placehold.co/300',
          'name' : 'udin suzume',
          'username' : 'szme_din',
          'followed' : true,
        },
        
      ]
    };
  },
  computed: {
    isSmallScreen() {
      // Adjust this breakpoint as per your requirement
      return window.innerWidth < 600; // Example: Apply x-small class when screen width is less than 600px
    },
  },
};
</script>
