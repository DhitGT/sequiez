<template>
  <div class="my-2">
    <div class="topcard flex items-center">
      <span class="font-bold">Top Authors</span>
      <v-spacer></v-spacer>
      <v-btn plain class="pa-0"
        ><span style="font-size: 0.7em" class="mr-2 text-[#6949ff] font-bold"
          >View All</span
        ><v-icon small dense color="#6949ff">mdi-arrow-right</v-icon>
      </v-btn>
    </div>
    <div class="bodycard overflow-x-auto my-2 ">
      <div class=" flex" style="min-width:fit-content">
        <div class="item mx-1 h-1/2 w-20 " v-for="(item,i) in items" :key="TopAuthor+i">
          <div class="avatar w-full flex flex-col items-center">
            <v-img :src="item.image + i" class="w-16 rounded-full"></v-img>
          </div>
          <div class="truncate text-center my-2">
            <label class="font-bold px-2 text-xs">{{ item.name.slice(0, item.name.indexOf(' ')) }}</label>
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
      items :[
        {
          'name' : 'Lorem Soebarjo',
          'image' : 'https://i.pravatar.cc/150?img='
        },
        {
          'name' : 'AkbarSoebarjo',
          'image' : 'https://i.pravatar.cc/150?img='
        },
        {
          'name' : 'Saeful Soebarjo',
          'image' : 'https://i.pravatar.cc/150?img='
        },
        {
          'name' : 'Ronald Soebarjo',
          'image' : 'https://i.pravatar.cc/150?img='
        },
        {
          'name' : 'Soenandar Soebarjo',
          'image' : 'https://i.pravatar.cc/150?img='
        },
        {
          'name' : 'Soenandar Soebarjo',
          'image' : 'https://i.pravatar.cc/150?img='
        },
        {
          'name' : 'Soenandar Soebarjo',
          'image' : 'https://i.pravatar.cc/150?img='
        },
      ]
    }
  }
};
</script>
