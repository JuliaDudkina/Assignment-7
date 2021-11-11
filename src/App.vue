<template>
  <h2>{{ user.name }}'s Main Goal is to</h2>
  <h3 v-if='user.showGoal'>{{ user.mainGoal }}</h3>
  <button @click='toggleGoal'>Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<script>
// Ref object approach
import {ref} from 'vue';
export default {
  setup(){
    const user = ref({
      name: 'Julia',
      mainGoal: 'learn Vue.js framework',
      showGoal: true
    })

    function toggleGoal(){
      user.value.showGoal = !user.value.showGoal;
    }
    return{ user: user,
            toggleGoal: toggleGoal
    };
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