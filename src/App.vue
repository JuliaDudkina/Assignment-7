<template>
  <h2>{{ name }}'s Main Goal is to</h2>
  <h3 v-if='showGoal'>{{ mainGoal }}</h3>
  <button @click='toggleGoal'>Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<script>
export default {
  data(){
    return{
      name: 'Julia',
      mainGoal: 'learn Vue.js framework',
      showGoal: true
    }
  },
  methods:{
    toggleGoal(){
      if (this.showGoal) {
        this.showGoal = false;
      } else {
        this.showGoal = true;
      }
    }
  }
}
</script>

<style>
html {
  font-family: sans-serif;
}
body {
  margin: 3rem;
  text-align: center;
}
</style>