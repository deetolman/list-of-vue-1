<template>
  <div id="app">
      <h2>Filter the air in your house with these plants! Pick from the list below.</h2>
    <Plants v-bind:plants="plants"
    v-bind:selected="selected"
    v-bind:onSelect="handleSelect"/>
    <User v-bind:plant="selected"/>
  </div>
</template>

<script>
import Plants from './components/Plants';
import User from './components/User';
import plants from './plant-data';

export default {
    data() {
        return {
            plants,
            selected: null
        };
    },
    components: {
        Plants,
        User
    },
    methods: {
        handleSelect(plant) {
            this.selected = plant;
        }
    }
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color:burlywood;
  margin-top: 60px;
}
h2 {
  text-align: center;
  color:cadetblue;
}
</style>
