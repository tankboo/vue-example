<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
import Home from './pages/Home'
export default {
  name: 'App',
  components:{
    Home
  }
}
</script>

<style>
#app {
  height: 100%;
}
</style>
