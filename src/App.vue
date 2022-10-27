<template>
<h1>Hello {{ name }} </h1>

<div v-text="name"></div>
<p v-html="channel"></p>
<h4 v-bind:id="id"> </h4>
<button :disabled="diasable" href="https://www.google.com">
google
</button>
<hr>
<span v-bind:style= "{
  color: highlight,
  'font-size': size + 'px'
}"> 
Mollit eiusmod laboris nulla deserunt et incididunt officia cillum. Eiusmod duis id cupidatat mollit officia pariatur. Sint nostrud esse culpa sunt exercitation veniam sint consequat. Pariatur eu amet cillum reprehenderit mollit cupidatat proident qui aliquip.
</span>


<p v-if="count > 0"> count is greater than 0</p>
<p v-else-if="count == 0"> count is equal  0</p>
<p v-else> count is not greater than 0</p>

<ul v-for="job in jobs" :key="job">
 <li> {{ job }}</li>
</ul>

<div v-for="name in fullnames" :key="name.key">
<h1>
 {{ name.first_name }} {{ name.last_name }}
 <ul v-for="job in name.jobs" :key="job">
 <li v-if="job != 'designer' "> {{ job }}</li>
</ul>
</h1>
</div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      name : 'ali jasim',
      channel: '<h4> app1 </h4>',
      id: 'id',
      diasable: true,
      highlight: 'green',
      size: 25,
      count: 0,
      jobs: ['programming', 'art' , 'digital marketing'],
      fullnames: [
        {
          first_name: 'ali',
          last_name: ' prog',
          jobs: [
            'developer' , 'programmer'
          ],
          key: '@alosh'

        },
        {
          first_name: 'lina',
          last_name: ' prog',
          jobs: [
            'designer' , 'programmer'
          ],
          key: 'llosh'

        },
      ]
    };
   
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
  margin-top: 60px;
}
</style>
