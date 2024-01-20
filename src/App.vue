<template>
<Card
view="true"
 descr="сигма"
foto="https://i.ytimg.com/vi/5A-0vLMDq2Y/maxresdefault.jpg"
 msg="чипи чипи чапа чапа руви руви рава рава бум бум бум"/>
<Card
view="true"
foto="https://i.ytimg.com/vi/5A-0vLMDq2Y/maxresdefault.jpg"
msg="шкиби туалет ор крипер"
descr="сигма близнец"/>
  
</template>

<script>

import Card from './components/Card.vue'

export default {
  name: 'App',
  components: {
    Card
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
