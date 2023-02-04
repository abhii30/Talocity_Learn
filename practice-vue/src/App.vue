<script>
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
export default {
  data() {
    return {
      characterList: [
        { name: "Avatar", element: ["air", "water", "earth", "fire"] },
        { name: "Man", element: ["air", "water"] },
        { name: "Alien", element: ["fire", "earth"] },
        { name: "Sky People", element: ["air"] },
      ],
      favoriteList: [],
      newCharacter: {
        name: "",
      },
    };
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
      this.characterList.forEach((character) => {
        elements.forEach((element) => {
          if (character.element.indexOf(element) > -1) {
            statistics[element] += 1;
          }
        });
      });
      return statistics;
    },
  },
  methods: {
    favoriteCharacter(character) {
      this.favoriteList.push(character);
    },
    addNewCharacter() {
      this.characterList.push(this.newCharacter);
      this.newCharacter = { name: "" };
    },
  },
};
</script>

<template>
  <p v-if="characterList.length === 0">There are no characters</p>
  <ul v-else>
    <div>
      <h2>Characters</h2>
      <li
        v-for="(character, index) in characterList"
        :key="`character-${index}`"
      >
        <p>{{ character.name }}</p>
        <button @click="favoriteCharacter(character.name)">⭐Favorite</button>
        <!--Parameter should be same for passing (character) -->
        <!-- create a button-->
      </li>
    </div>
    <h2>Statistics</h2>
    <ul>
      <li v-for="(stat, type) in benderStatistics">{{ type }} : {{ stat }}</li>
    </ul>
  </ul>
  <h2>Favorite Character</h2>
  <ul v-if="favoriteList.length > 0">
    <li
      v-for="(character, index) in favoriteList"
      :key="`character-fav-${index}`"
    >
      {{ character }}
    </li>
  </ul>
  <p v-else>No favorite character</p>
  <h2>New Character</h2>
  <pre>{{ newCharacter }} </pre>
  <label for="newCharacter">Add a new character: </label>
  <input
    type="text"
    v-model="newCharacter.name"
    @keyup.enter="addNewCharacter"
  />
</template>
