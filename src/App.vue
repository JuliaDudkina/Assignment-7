<template>
  <h2>{{ userName }}'s Main Goal is to</h2>
  <h3 v-if='userShowGoal'>{{ userMainGoal }}</h3>
  <button @click='toggleGoal'>Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<script>
// Separate refs approach
import {ref} from 'vue';
export default {
  setup(){
    const uName  = ref('Julia');
    const uMainGoal = ref('learn Vue.js framework');
    const uShowGoal = ref(true);

    function toggleGoal(){
      uShowGoal.value = !uShowGoal.value;
    }
    return{ userName: uName,
            userMainGoal: uMainGoal,
            userShowGoal: uShowGoal,
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