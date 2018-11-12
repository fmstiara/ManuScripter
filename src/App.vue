<template>
  <div id="app">
    <el-header><h1>ManuScripter</h1></el-header>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

header {
  height: 60px;
  line-height: 60px;
  background-color: #2c3e50;
  color: aliceblue;
}

body {
  height: 100vh;
}

#app {
  font-family: Helvetica, Arial, sans-serif;
  font-weight: normal;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  height: 100%;
}
</style>
