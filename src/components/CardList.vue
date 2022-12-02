<template>
  <div class="cardlist__container">
    <!-- TITLE  -->
    <div class="text-5xl text-white pt-20 pb-10 font-bold title__cardlist">
      MONSTERS
    </div>

    <div class="w-full mb-10 h-10 search__cardlist">
      <input
        maxlength="50"
        class="px-2 py-3 max-w-4xl h-full w-full rounded shadow shadow-white"
        type="text"
        name="search"
        id="search"
        v-model="searchMonster"
      />
    
    </div>

    <!-- LISTADO  -->
    <div class="grid grid-cols-4 gap-12 cards__cardlist">
      <CardComponent
        v-for="monster in filteredMonsters"
        :key="monster.id"
        :monster="monster"
      />
    </div>
  </div>
</template>

<script>
import CardComponent from "./Card.vue";

export default {
  name: "CardlistComponent",
  components: {
    CardComponent,
  },
  data() {
    return {
      searchMonster: "",
      monsters: [
        {
          id: 1,
          name: "Leanne Graham",
          email: "Sincere@april.biz",
          profile: "https://robohash.org/1?set=set2&size=300x300",
        },
        {
          id: 2,
          name: "Leanne Howell",
          email: "Lucio_Hettinger@annie.ca",
          profile: "https://robohash.org/2?set=set2&size=300x300",
        },
        {
          id: 3,
          name: "Clementine Graham",
          email: "Julianne.OConner@kory.org",
          profile: "https://robohash.org/3?set=set2&size=300x300",
        },
        {
          id: 4,
          name: "Ervin Howell",
          email: "Sincere@april.biz",
          profile: "https://robohash.org/4?set=set2&size=300x300",
        },
        {
          id: 5,
          name: "Clementine Bauch",
          email: "Nathan@yesenia.net",
          profile: "https://robohash.org/5?set=set2&size=300x300",
        },
        {
          id: 6,
          name: "Chelsey Dietrich",
          email: "Shanna@melissa.tv",
          profile: "https://robohash.org/6?set=set2&size=300x300",
        },
        {
          id: 7,
          name: "Mrs. Dennis Schulist",
          email: "Karley_Dach@jasper.info",
          profile: "https://robohash.org/7?set=set2&size=300x300",
        },
        {
          id: 8,
          name: "Nicholas Runolfsdottir V",
          email: "Telly.Hoeger@billy.biz",
          profile: "https://robohash.org/8?set=set2&size=300x300",
        },
        {
          id: 9,
          name: "Glenna Reichert",
          email: "Sherwood@rosamond.me",
          profile: "https://robohash.org/9?set=set2&size=300x300",
        },
        {
          id: 10,
          name: "Clementina DuBuque",
          email: "Chaim_McDermott@dana.io",
          profile: "https://robohash.org/10?set=set2&size=300x300",
        },
      ],
    };
  },
  computed: {
    filteredMonsters() {
      let filteredMonster = this.monsters.filter((monster) =>
        monster.name.toLowerCase().includes(this.searchMonster.toLowerCase())
      );
      
      return filteredMonster;
    },
  },
};
</script>

<style lang="scss" scoped></style>
