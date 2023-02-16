<script>
import BenderStats from "./components/BenderStats.vue";
import UserCard from "./components/userCard.vue";
import { ref } from "vue";
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'

export default {
  data() {
    return {
      colorChange: "black",
      characterList: [
        { name: "Avatar", element: ["air", "water", "earth", "fire"] },
        { name: "Man", element: ["air", "water"] },
        { name: "Alien", element: ["fire", "earth"] },
        { name: "Sky People", element: ["air"] },
      ],
      userData: {
        name: "Abhi",
        roll: "12016136",
        college: "Nit kurukshetra",
      },
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
  components: { BenderStats, UserCard },
};
</script>

<template>
  <div :class="wrapper">
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
    <UserCard :name="userData.name" :roll="userData.roll" />
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
.button {
  background-color: aqua;
}
h2 {
  color: blue;
}
</style>
