<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br />
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>

    <a href="#" v-bind:class="{ active: menu === 'home' }" v-on:click="gantiMenu('home', $event)">Home</a>
    <a href="#" v-bind:class="{ active: menu === 'about' }" v-on:click="gantiMenu('about', $event)">ABout</a>
    <a href="#" v-bind:class="{ active: menu === 'blog' }" v-on:click="gantiMenu('blog', $event)">Blog</a>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.active {
  background-color: aqua;
  border: 0;
}
h3 {
  margin: 40px 0 0;
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
