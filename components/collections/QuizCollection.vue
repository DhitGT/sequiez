<template>
  <div class="my-2">
    <div class="topcard flex items-center">
      <span class="font-bold">{{ collectionName }}</span>
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
          class="w-36 h-40 mx-2 border-b-4 border-b-[#262a35] rounded-xl"
          id="ini-card-"
          v-for="(item, i) in items"
          :key="discover - i"
        >
          <div
            class="red cover h-1/2 rounded-t-xl"
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
          <div
            class="detail rounded-b-xl bg-[#1f222a] flex flex-col justify-between h-1/2 pa-2"
          >
            <div
              class="overflow-hidden"
              style="
                -webkit-line-clamp: 2;
                display: -webkit-box;
                -webkit-box-orient: vertical;
                line-height: 1.1em;
              "
            >
              <span class="w-100 font-bold">{{ item.title }} </span>
            </div>
            <div class="flex items-center gap-2 pa-0 max-h-5">
              <div class="w-5 rounded-full">
                <v-img class="rounded-full" :src="item.author.image + (i + Math.floor(Math.random() * 10))">
                </v-img>
              </div>
              <label class="text-xs truncate">{{ item.author.name }}</label>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    collectionName: {
      type: String,
      // other optional configurations
    },
  },

  data() {
    return {
      items: [
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
        {
          cover: "https://picsum.photos/300?random=",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          author: {
            image: "https://i.pravatar.cc/150?img=",
            name: "Akbar Kitamura lorem",
          },
        },
      ],
    };
  },
};
</script>
