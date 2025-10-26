<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/fuzy.gif">
    <HelloWorld msg="Welcome to Katz Airline"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>
