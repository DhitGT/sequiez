<template>
  <div>
    <div class="topper justify-between flex items-center">
      <label class="font-bold text-lg">10 Quiez</label>
      <div class="flex justify-end items-center text-[#6949ff]">
        <label class="text-lg">Newest</label>
        <v-btn icon color="#6949ff">
          <v-icon>mdi-swap-vertical</v-icon>
        </v-btn>
      </div>
    </div>
    <div class="bodycard mt-3 overflow-x-auto">
      <div class="flex flex-col gap-3" style="min-width: fit-content">
        <div
          class="w-100 border-[0.1em] border-gray-600 rounded-lg overflow-hidden flex gap-1"
          v-for="(item, i) in items"
          :key="i"
        >
          <div
            class="cover w-3/4"
            :style="{
              backgroundImage:
                'url(' +
                item.cover +
                (i + Math.floor(Math.random() * 10)) +
                ')',

              backgroundPosition: 'center',
              backgroundSize: 'cover',
            }"
          ></div>
          <div class="flex pa-2 flex-col justify-center">
            <div
              class="overflow-hidden "
              style="
                -webkit-line-clamp: 2;
                display: -webkit-box;
                -webkit-box-orient: vertical;
                line-height: 1.1em;
              "
            >
              <label class="leading-[0.1rem] text-sm font-bold">
                {{ item.title }}
              </label>
            </div>
            <div class="flex text-[0.6em] mt-2 gap-1 items-center">
              <span>
                {{ item.release }}
              </span>
              <v-divider vertical></v-divider>
              <span>
                {{ item.player }}
              </span>
            </div>
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
          release: "2 days ago",
          player: "1.4k",
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          release: "2 days ago",
          player: "1.4k",
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          release: "2 days ago",
          player: "1.4k",
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          release: "2 days ago",
          player: "1.4k",
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          release: "2 days ago",
          player: "1.4k",
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          release: "2 days ago",
          player: "1.4k",
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          release: "2 days ago",
          player: "1.4k",
        },
      ],
    };
  },
};
</script>
