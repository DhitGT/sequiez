<template>
  <div class="fixed bottom-0 left-0  w-full backdrop-blur-md rounded-[10rem]">
    <v-container>
      <div class=" flex mb-5">
        <div class="flex flex-col items-center w-0.5" v-for="(item, i) in items" :key="i">
          <v-icon>{{item.icon}}</v-icon>
          <label style="font-size:0.5em">{{item.title}}</label>
        </div>
      </div>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          'icon' : 'mdi-home-outline',
          'title' : 'Home'
        },
        {
          'icon' : 'mdi-library-outline',
          'title' : 'Library'
        },
        {
          'icon' : 'mdi-play-box-outline',
          'title' : 'Join'
        },
        {
          'icon' : 'mdi-plus-box-outline',
          'title' : 'Create'
        },
        {
          'icon' : 'mdi-account-outline',
          'title' : 'Profile'
        },
      ]
    };
  }
};
</script>
