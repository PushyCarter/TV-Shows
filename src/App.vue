<template>
  <div id="app">
    <Header title="Popular TV Shows"/>
      <Card :showList="shows"/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Card from './components/Card.vue';
import axios from 'axios';

export default {
  name: 'App',
  components: {
    Header,
    Card,
  },
  data(){
    return {
      shows:'',
    }
  },
  mounted()
  {
    axios.get('https://api.themoviedb.org/3/tv/popular?api_key=01266932991fa0f84b8598495a718d52&language=en-US&page=1')
    .then( (response) => {
      this.shows = response.data.results;
    })
  }
}
</script>

<style>
  * {
    margin: 0;
    padding: 0;
  }
</style>

<!-- 01266932991fa0f84b8598495a718d52 -->