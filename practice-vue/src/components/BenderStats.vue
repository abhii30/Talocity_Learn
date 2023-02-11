<script>
export default {
  props: {
    characters: {
      type: Array,
      required: true,
    },
  },
  computed: {
    benderStatistics() {
      const elements = ["air", "water", "earth", "fire"];
      const statistics = {
        air: 0,
        water: 0,
        earth: 0,
        fire: 0,
      };
      this.characters.forEach((character) => {
        elements.forEach((element) => {
          if (character.element.indexOf(element) > -1) {
            statistics[element] += 1;
          }
        });
      });
      return statistics;
    },
  },
};
</script>
<template>
  <h2>Statistics</h2>
  <ul>
    <li v-for="(stat, type) in benderStatistics">{{ type }} : {{ stat }}</li>
  </ul>
</template>

<style scoped> 
h2 {
  color: rgb(36, 52, 46);
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}

</style>
