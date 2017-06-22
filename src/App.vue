<template>
  <div>
    <h2>hello world</h2>

    <input type="text" v-model="name">
    <p>Hello, {{name}}!</p>
    <p>{{name.length}}/20</p>
    <p v-if="name.length > 20">20文字以内で入力してください</p>

    <my-profile></my-profile>

    <p>{{msg}}</p>

    <a @click="sample" class="btn">click</a>
  </div>

</template>

<script>

import Profile from "./Profile.vue"

export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      name: 'John Smith'
    }
  },
  components: {
    "my-profile": Profile
  },
  methods: {
      sample(){
          this.msg = "hello, my sample app"
      }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

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
