<template>
  <h2>{{ user.name }}'s Main Goal is to</h2>
  <h3>{{ user.mainGoal }}</h3>
  <!-- Task 2: Toggle (show/ hide) the goal with help of the button  -->
  <button>Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<script>
import {reactive} from 'vue';
export default {
  setup(){
    const user = reactive({
      name: 'Julia',
      mainGoal: 'learn Vue.js framework'
    })

    return{ user: user};
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