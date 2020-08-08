<template>
  <div class="home">
    <img alt="logo" src="../assets/virus.png" height="200" width="200">
    <HelloWorld msg="CovidApp v1.0"/>
    <HelloWorld/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
