<template>
  <div class="">
    <div class="topHeader flex justify-between w-screen">
      <v-btn fab plain icon small>
        <v-icon>mdi-close</v-icon>
      </v-btn>
      <v-spacer></v-spacer>
      <div class="flex items-center justify-end w-100 pa-0">
        <v-btn fab plain icon small>
          <v-icon>mdi-star-outline</v-icon>
        </v-btn>
        <v-btn fab plain icon small>
          <v-icon>mdi-dots-horizontal-circle-outline</v-icon>
        </v-btn>
      </div>
    </div>
    <div class="detailQuiz">
      <div class="cover my-4">
        <v-img
          src="https://picsum.photos/300?random=39"
          height="10rem"
          class="rounded-xl"
        >
        </v-img>
      </div>
      <div class="infoQuiz">
        <label class="font-bold">Lorem ipsum dolor sit amet.</label>
        <v-divider class="mt-3"></v-divider>
        <div class="moreInfo flex my-3">
          <div class="flex flex-col items-center">
            <span class="total font-bold text-lg">10</span>
            <label class="label text-xs">Question</label>
          </div>
          <v-divider vertical></v-divider>
          <div class="flex flex-col items-center">
            <span class="total font-bold text-lg">9</span>
            <label class="label text-xs">Played</label>
          </div>
          <v-divider vertical></v-divider>
          <div class="flex flex-col items-center">
            <span class="total font-bold text-lg">923</span>
            <label class="label text-xs">Favorited</label>
          </div>
          <v-divider vertical></v-divider>
          <div class="flex flex-col items-center">
            <span class="total font-bold text-lg">32</span>
            <label class="label text-xs">Shared</label>
          </div>
        </div>
        <v-divider></v-divider>
      </div>
      <div class="authorInfo flex items-center my-4">
        <div class="profile w-12">
          <v-img
            src="https://i.pravatar.cc/150?img=5"
            class="rounded-full"
          ></v-img>
        </div>
        <div class="nameInfo flex flex-col justify-evenly mb-1 ms-3">
          <label class="text-md font-bold">Abdul Kiyotaka</label>
          <label class="text-xs">@kytk_abdl</label>
        </div>
        <v-btn class="py-3 rounded-xl" x-small color="#6949ff">Follow</v-btn>
      </div>
      <div class="description my-3">
        <label class="text-lg font-bold">Description</label>
        <p class="text-xs my-2">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Non, aliquid
          nobis inventore enim fuga deserunt voluptates, corporis doloremque,
          quo illum facere ipsam adipisci incidunt? Architecto accusantium
          molestiae vel dolores quo!
        </p>
      </div>
      <div class="questionPreview">
        <div
          v-if="isQuestionDisabled"
          class="card border-gray-600 border-2 rounded-xl py-4 px-2 flex flex-col items-center gap-2"
        >
          <v-icon class="opacity-50">mdi-eye-off-outline</v-icon>
          <span class="text-xs opacity-50"
            >Question content is hidden by the creator</span
          >
        </div>
        <div v-else>
          <div class="topcard flex items-center">
            <span class="font-bold">Question (10)</span>
            <v-spacer></v-spacer>
            <v-btn plain class="pa-0"
              ><span
                style="font-size: 0.7em"
                class="mr-2 text-[#6949ff] font-bold"
                >View All</span
              ><v-icon small dense color="#6949ff">mdi-arrow-right</v-icon>
            </v-btn>
          </div>
          <div
            class="rounded-lg flex my-4 h-24 overflow-hidden bg-[#1f222a] border-[0.4px] border-gray-600" v-for="(item,i) in items" :key="'question-' + i"
          >
            <div class="w-2/5 rounded-s-lg h-24">
              <v-img
                class="rounded-s-lg h-24"
                :src="item.image"
              ></v-img>
            </div>
            <div class="flex flex-col pa-3 justify-evenly">
              <span class="font-bold text-lg">{{i+1}} - {{item.type}}</span>
              <div
              class="overflow-hidden"
              style="
                -webkit-line-clamp: 2;
                display: -webkit-box;
                -webkit-box-orient: vertical;
                line-height: 1.1em;
              "
            >
              <span class="w-100 text-sm">{{item.question}}</span>
            </div>
            </div>
          </div>
        </div>
      </div>
      <v-divider class="my-4"></v-divider>
      <div class="actionQuiz flex items-center gap-3 justify-evenly">
        <div class="rounded-xl w-2/4 border-b-4 border-b-[#262933]">
          <v-btn
            small
            color="#35383f"
            width="100%"
            class="rounded-xl py-6 px-auto"
            elevation="0"
          >
            Play Solo
          </v-btn>
        </div>
        <div class="rounded-xl border-b-4 w-3/4 border-b-[#543acc]">
          <v-btn
            small
            color="#6949ff"
            width="100%"
            class="rounded-xl py-6 px-auto"
            elevation="0"
          >
            Play With Friends
          </v-btn>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isQuestionDisabled: false,
      items:[
        {
          'image' : 'https://placehold.co/400',
          'type' : 'Quiz',
          'question' : 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sequi assumenda laborum nemo ratione ullam! '
        },

      ]
    };
  },
};
</script>
