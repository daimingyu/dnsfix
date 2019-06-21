<template>
  <div id="wrapper">
    <Tabs />
  </div>
</template>

<script>
  import Tabs from './Tabs/Tabs'

  export default {
    name: 'landing-page',
    components: { Tabs },
    methods: {}
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body { font-family: 'Source Sans Pro', sans-serif; }

  #wrapper {
    background: #fafafa;
    height: 100vh;
    padding: 20px;
    width: 100vw;
    display: flex;
  }
</style>
