
<template>
    <form>
        <input type="text" v-model="name">
    </form>

    <h1> 
    {{ name }}
    </h1>
</template>

<script>
export default {
    name: 'app',
    data(){
        return {
            name: 'ali'
        }
    },
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
