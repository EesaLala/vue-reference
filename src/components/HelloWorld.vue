<template>
  <div class="hello">

    <h2>Hello, {{ firstName }} </h2>

    <label for="nameInput">Enter Your Name: </label>
    <input v-model="firstName" type="text" name="nameInput">

    <br>
    <br>

    <label for="addPoke">Add another poke to list: </label>
    <input v-model="Poke" type="text" name="addPoke">
    <button @click="pokemon.push(Poke)"> Add </button>

    <ul>
      <li v-for="item in pokemon" :key="item">
        {{ item }}
      </li>
    </ul>

    <div></div>

  </div>
</template>

<script>
export default {

  data() {
    return {
      firstName: "",
      pokemon: ["Charizard", "Bulbasaur", "Pikachu"],
      Poke: ""
    }
  },
  mounted: function () {
    console.log('component mounted')
  },
  destroyed: function () {
    console.log('component destroyed')
  }

}

</script>





<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: block;
  margin: 20px;
}
a {
  color: #42b983;
}
</style>
