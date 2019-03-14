<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <month></month>
  </div>
</template>

<script>
import Month from "./Month";
export default {
  name: 'HelloWorld',
  components: {Month},
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
