<script>
import Counter from "./components/Counter.vue";
export default {
  components: {
    Counter,
  },
  data() {
    return {
      message: "Hello it works!",
      listOfnumbers: [
        {
          name: 1,
          id: "2aa00583-335f-4773-8ba3-11d89357244d",
          list: [1, 2, 3],
        },
        {
          name: 2,
          id: "851ed2b8-3744-4e78-a0ab-35de688dc1d8",
          list: [1, 2, 3],
        },
        {
          name: 3,
          id: "820a758a-e0d3-4228-8acc-58a6beba42f2",
          list: [1, 2, 3],
        },
        {
          name: 4,
          id: "3ddabf05-5c4f-47d4-a870-a2608a6b002e",
          list: [1, 2, 3],
        },
        {
          name: 5,
          id: "c8da694c-b1ef-4d94-87ba-fcf36b89a948",
          list: [1, 2, 3],
        },
      ],
    };
  },

  // about managing darta, triggering actions
};
</script>

<template>
  <Counter />
  <hr />
  <p v-if="message.length % 2 === 0">Even : {{ message.toUpperCase() }}</p>
  <p v-else>Odd :{{ message }}</p>
  <ul v-for="(item, index) in listOfnumbers" :key="`item-${index}`">
    <li>{{ item.id }}</li>
    <ul>
      <li v-for="(number, index) in item.list" :key="`number-${index}`">
        {{ number }}
      </li>
    </ul>
  </ul>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
