<template>
<div v-show='alertShow' class="alert alert-danger alert-dismissible ">
  <span class="close" aria-label="close" v-on:click='closeAlert'>×</span> {{ message }}
</div>
</template>

<script>
export default {
  props: ['message','alertShow'],

  methods: {
    closeAlert: function() {
      this.$emit('closeAlert')
    }
  },
}
</script>

<style>
/*.alert {
    padding: 10px;
    background: #f0f0f0;
  }
  .alert-error {
    background: red;
    color: white;
  }*/
</style>
