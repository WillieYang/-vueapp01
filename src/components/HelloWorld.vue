<template>
  <div class="hello">
    <h1 v-text="msg"></h1>
    <h2>Essential Links</h2>
    <h1>{{ input_val }}</h1>
    <div>
      <div class="col-lg-4 col-sm-4"></div>
      <div class="col-lg-4 col-sm-4">
        <input type="text" class="form-control col col-lg-4" v-model="input_val">
      </div>
      <div class="col-lg-12 col-sm-12"></div>
    </div>
    <ul class="col-lg-12 col-sm-12">
      <li v-for="user in usrs">
        {{ user.firstname }} {{ user.lastname }}
      </li>
    </ul>
    <div>
      <button class="btn btn-primary" v-on:click="counter++">You've clicked this button {{ counter }} times!</button>
    </div>
    <ul>
      <li><a href="https://vuejs.org" target="_blank">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank">Twitter</a></li>
      <br>
      <li><a href="http://vuejs-templates.github.io/webpack/" target="_blank">Docs for This Template</a></li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li><a href="http://router.vuejs.org/" target="_blank">vue-router</a></li>
      <li><a href="http://vuex.vuejs.org/" target="_blank">vuex</a></li>
      <li><a href="http://vue-loader.vuejs.org/" target="_blank">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      usrs: [{firstname: 'Sheng', lastname: 'Yang'},
             {firstname: 'Will', lastname: 'Smith'},
             {firstname: 'Jack', lastname: 'Black'}
           ],
      input_val: '',
      counter: 0
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
