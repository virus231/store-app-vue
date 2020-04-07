<template>
  <div id="app">
    <h1>Hello Vue</h1>
    <vMainWrapper></vMainWrapper>
  </div>
</template>



<script>
import vMainWrapper from './components/v-main-wrapper'


export default {
  name: 'app',
  components: {
    vMainWrapper
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
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
