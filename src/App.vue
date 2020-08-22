<template>
  <div id="app">
    <Header msg="Neal.fun" />
    <Section text="Spend Bill Gates' Money" />
    <todo-item></todo-item>
  </div>
</template>

<script>
import Section from './components/Section.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header, 
    Section
  }
}
</script>

<style>
#app {
  font-family: Roboto, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #333;
  background-color: #f1f2f6;
  padding: 0;
  margin: 0;
}
body {
  margin: 0;
}
</style>

