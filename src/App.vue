<template>
  <div>
  <div id="app">
   中国石油大学（华东）通讯录
  
  </div>
  <HelloWorld/>
</div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
export default {
  name: 'App',
  components: {
    HelloWorld

  }
}
</script>

<style>
/*#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}*/
#app
{
  background-color: #4169E1;
  font-weight: 100px;
  margin: 0;
  font-size: 20px;
  text-align: center;
  color: white;
  padding-top: 6%;
  padding-bottom: 6%;
  border: none;
}
</style>
