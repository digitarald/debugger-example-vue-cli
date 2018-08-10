<template>
  <div class="hello">
    <h1 v-on:click="reverseMessage">{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: () => {
    return {
      msg: 'Click Me!'
    }
  },
  methods: {
    reverseMessage: function () {
      console.log(this)
      this.msg = this.msg.split('').reverse().join('')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  cursor: pointer;
  text-decoration: underline;
  font-weight: normal;
}
a {
  color: #42b983;
}
</style>
