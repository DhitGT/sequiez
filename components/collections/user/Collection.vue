<template>
  <div>
    <div class="topper justify-between flex items-center">
      <label class="font-bold text-lg">23 Collections</label>
      <div class="flex justify-end items-center text-[#6949ff]">
        <label class="text-lg">Newest</label>
        <v-btn icon color="#6949ff">
          <v-icon>mdi-swap-vertical</v-icon>
        </v-btn>
      </div>
    </div>
    <div class="boddy mt-5">
      <div class="grid grid-cols-2 gap-3">
        <div
            class=" grow h-24 rounded-xl"
            id="ini-card-"
            v-for="(item, i) in items"
            :key="collection - i"
          >
            <div
              class=" flex flex-col cover pa-2 h-24 rounded-xl"
              :style="{
                backgroundImage:
                  'linear-gradient(to bottom, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.5)), url(' +
                  item.cover + i +
                  ')',
                backgroundPosition: 'center',
                backgroundSize: 'cover',
              }"
            >
              <span class="w-100 mt-auto font-bold">{{
                item.title.slice(0, item.title.indexOf(" "))
              }}</span>
            </div>
          </div>
      </div>
    </div>
  </div>

</template>
<script>
export default {
  data(){
    return{
      items: [
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
      ]
    }
  }
};
</script>
