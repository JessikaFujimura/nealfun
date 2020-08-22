<template>
  <div class="header">
    <a href="https://neal.fun/">{{ msg }}</a>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a {
    padding-left: 15px;
    font-size: 30px;
    font-weight: bold;
    text-decoration: none;
    color: rgb(51, 51, 51);
    display:block;
    max-width: 1000px;
    margin: auto;
}
a:visited {
    color: rgb(51, 51, 51);
}
.header {
    margin-bottom: 25px;
    background-color: white;
    padding: 30px 0;
    text-align: left;
}
</style>
