<template>
  <div>
    <div class="topNav flex justify-between">
      <div>
        <v-btn icon>
          <v-icon>mdi-arrow-left</v-icon>
        </v-btn>
      </div>
      <div class="flex justify-end items-center gap-2">
        <v-btn icon small>
          <v-icon>mdi-send-outline</v-icon>
        </v-btn>
        <v-btn icon small>
          <v-icon>mdi-dots-vertical-circle-outline</v-icon>
        </v-btn>
      </div>
    </div>
    <div class="profilBg mt-6 mb-3">
      <div
        class="w-full h-24 border-b-4 border-b-[#262a35] rounded-xl"
        id="ini-card-"
      >
        <div
          class="red cover h-full rounded-xl"
          :style="{
            backgroundImage: 'url(https://placehold.co/200)',
            backgroundPosition: 'center',
            backgroundSize: 'cover',
          }"
        ></div>
      </div>
    </div>
    <div class="userSnack">
      <div class="flex w-screen" style="max-width: 100%; cursor: pointer">
        <div class="w-12 rounded-full overflow-hidden">
          <v-img v-if="user" lazy-src="https://placehold.co/200" :src="user.picture.large ? user.picture.large : 'https://placehold.co/200' "></v-img>

        </div>
        <div class="flex flex-col justify-center px-3" v-if="user">
          <span class="font-bold text-sm md:text-lg">{{user.name.first + ' ' + user.name.last}}</span>
          <span class="text-xs md:text-md">@{{user.name.title + '' + user.name.last}}</span>
        </div>
        <div
          class="flex items-center justify-end rounded-lg selection:overflow-hidden"
        >
          <v-btn
            style="text-transform: none"
            rounded="lg"
            :outlined="false"
            :small="isSmallScreen"
            color="#6949ff"
            class="ma-0"
          >
            {{ false ? "Following" : "Follow" }}
          </v-btn>
        </div>
      </div>
    </div>
    <div class="userDetail ">
      <v-divider class="mt-3"></v-divider>
      <div class="grid grid-cols-3 gap-4">
        <div class="moreInfo flex flex-col items-center my-3">
          <span class="total font-bold text-lg">10</span>
          <label class="label text-xs">Quiez</label>
        </div>
        <div class="moreInfo flex items-center my-3">
          <v-divider vertical></v-divider>
          <div class="flex flex-col items-center justify-center">
            <span class="total font-bold text-lg">9</span>
            <label class="label text-xs">Played</label>
          </div>
          <v-divider vertical></v-divider>
        </div>
        <div class="moreInfo flex flex-col items-center my-3">
          <span class="total font-bold text-lg">348</span>
          <label class="label text-xs">Players</label>
        </div>
      </div>
      <v-divider></v-divider>
      <div class="grid grid-cols-3  gap-4">
        <div class="moreInfo flex flex-col items-center my-3">
          <span class="total font-bold text-lg">23</span>
          <label class="label text-xs">Collections</label>
        </div>
        <div class="moreInfo flex items-center my-3">
          <v-divider vertical></v-divider>
          <div class="flex flex-col items-center justify-center">
            <span class="total font-bold text-lg">596</span>
            <label class="label text-xs">Followers</label>
          </div>
          <v-divider vertical></v-divider>
        </div>
        <div class="moreInfo flex flex-col items-center my-3">
          <span class="total font-bold text-lg">923</span>
          <label class="label text-xs">Following</label>
        </div>
      </div>
      <v-divider></v-divider>
    </div>
    <div class="moreAction my-4 flex gap-3 max-w-full items-center justify-evenly">
      <v-btn color="#6949ff" class="py-2 grow px-4 rounded-xl" :small="isSmallScreen" style="text-transform:none" :outlined="selectedAction != 'quiz'" @click="handleClickAction('quiz')">
        Quiez
      </v-btn>
      <v-btn color="#6949ff" :outlined="selectedAction != 'collections'" class="py-2 grow px-4 rounded-xl" :small="isSmallScreen" style="text-transform:none" @click="handleClickAction('collections')">
        Collection
      </v-btn>
      <v-btn color="#6949ff" :outlined="selectedAction != 'description'" class="py-2 grow px-4 rounded-xl" :small="isSmallScreen" style="text-transform:none" @click="handleClickAction('description')">
        About
      </v-btn>
    </div>
    <div class="moreActionSpace my-3">
      <collections-user-quiz-collection v-if="selectedAction == 'quiz'"></collections-user-quiz-collection>
      <collections-user-collection v-else-if="selectedAction == 'collections'"></collections-user-collection>
      <collections-user-description v-else-if="selectedAction == 'description'"></collections-user-description>
    </div>
  </div>

</template>
<script>
export default {
  created(){
    this.getUser()
  },
  computed: {
    isSmallScreen() {
      // Adjust this breakpoint as per your requirement
      return window.innerWidth < 600; // Example: Apply x-small class when screen width is less than 600px
    },
  },
  data(){
    return{
      selectedAction : 'quiz',
      user : null
    }
  },
  methods:{
    handleClickAction(name) {
      this.selectedAction = name
    },
    async getUser() {
    try {
        const res = await this.$axios.get('https://randomuser.me/api/');
        this.user = res.data.results[0]; // Assuming you want the first result
        console.log(this.user);
    } catch (error) {
        console.error('Error fetching user:', error);
    }
}

  }
};
</script>
