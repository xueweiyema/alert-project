<template>
<div id="app">
  <Alert v-bind:alertShow="as" v-bind:message="msg" v-on:closeAlert="closeAlert"></Alert>
  <button class='btn btn-default' v-on:click='openAlert'>open alert</button>
</div>
</template>

<script>
import Alert from './components/Alert'

export default {
  name: 'app',
  data: function() {
    return {
      msg: 'I am a alert !!!',
      as: true
    }
  },
  methods: {
    openAlert: function() {
      this.as = true;
    },
    closeAlert: function() {
      this.as = false;
    }
  },
  components: {
    Alert
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
</style>
