<template>
  <div class="home">

    <img v-if="showImg" :src="imageUrl" alt="">

    <h3 v-else> sorry no data </h3>

    <button @click="switchImg">Change Poke</button>

    <button @click="showImg = !showImg">Show/Hide image</button>
    
  </div>
</template>

<script>

export default {
  data() {
    return {
      imageUrl: `https://pokeres.bastionbot.org/images/pokemon/5.png`,
      showImg: true,
      randInt: "5"
    }
  },
  methods: {
    switchImg() {
      this.randInt = (1 + Math.floor(Math.random() * 200))
      this.imageUrl = `https://pokeres.bastionbot.org/images/pokemon/${this.randInt}.png`
    }
  }
}

</script>

<style scoped>

  img {
    width: 300px;
  }

</style>
