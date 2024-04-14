<template>
  <div class="my-2">
    <div class="topcard flex items-center">
      <span class="font-bold">Top Collections</span>
      <v-spacer></v-spacer>
      <v-btn plain class="pa-0"
        ><span style="font-size: 0.7em" class="mr-2 text-[#6949ff] font-bold"
          >View All</span
        ><v-icon small dense color="#6949ff">mdi-arrow-right</v-icon>
      </v-btn>
    </div>
    <div class="bodycard overflow-x-auto pa-2">
      <div class="flex" style="min-width: fit-content">
        <div
          class="w-36 h-24 mx-2 border-b-4 border-b-[#262a35] rounded-xl"
          id="ini-card-"
          v-for="(item, i) in items"
          :key="discover - i"
        >
          <div
            class="red flex flex-col cover pa-2 h-24 rounded-xl"
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
  data() {
    return {
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
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
      ],
    };
  },
};
</script>
