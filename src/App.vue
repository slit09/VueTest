<template>
  <div class="container">
  <h1> Тест Emit и Provide</h1>
    <Card/>
    <div class="rows"></div>
    <button v-on:click="addAnimal" type="button" class="btn btn-primary">Primary</button>
  </div>
</template>

<script>
import Card from './components/card.vue'

export default {
  name: 'App',
  components: {
    Card
  },
  provide:{
    animal:"слон"
  },
  methods:{
    addAnimal(){
      this.animal = 2
    }
  }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
