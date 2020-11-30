<template>
  <div id="app">
    <Header title="Popular TV Shows"/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import axios from 'axios';

export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style>
  * {
    margin: 0;
    padding: 0;
  }
</style>
