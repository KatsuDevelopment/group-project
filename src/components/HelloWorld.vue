<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Good experience with every trip, Be confident in your safety. Fly with us Katz Airline
    </p>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://discord.gg/fudkzGX7jS" target="_blank" rel="noopener">Discord</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-weight: bold;
  margin: 40px 0 20px;
}
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
