<script>
import BenderStats from "./components/BenderStats.vue";
import { ref } from "vue";
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
const colorChange = ref("black");

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
  methods: {
    favoriteCharacter(character) {
      this.favoriteList.push(character);
    },
    addNewCharacter() {
      this.characterList.push(this.newCharacter);
      this.newCharacter = { name: "" };
    },
  },
  components: { BenderStats },
};
</script>

<template>
  <div>
    <h2>{{ colorChange }}</h2>
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
    <BenderStats :characters="characterList" />
  </div>
</template>

<style>
html {
  padding: 2rem;
  box-sizing: border-box;
  background-color: bisque;
}
h2 {
  color: blue;
}
</style>
