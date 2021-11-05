<template>
  <div class="home">
    <PkmnPreview
      v-for="pokemon in pokemons"
      :key="pokemon"
      :pokemon="pokemon"
    ></PkmnPreview>
  </div>
</template>

<script>
// @ is an alias to /src

import PkmnPreview from "@/components/PkmnPreview.vue";

export default {
  //options API
  name: "Home",
  components: {
    PkmnPreview,
  },
  data() {
    return {
      pokemons: [],
    };
  },
  created: function () {
    this.fetchData();
  },
  methods: {
    fetchData: async function () {
      try {
        const response = await fetch(
          "https://pokeapi.co/api/v2/pokemon?limit=151&offset=0"
        );
        const data = await response.json();
        this.pokemons = data.results;
      } catch (error) {
        console.log(error);
      }
    },
  },
};
</script>
