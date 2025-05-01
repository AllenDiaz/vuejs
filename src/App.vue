<script>
export default {
  data() {
    return {
      name: 'Allen Diaz',
      status: 'active',
      task: ['Task One', 'Task Two', 'Task Three'],
      link: 'https:/google.com',
    };
  },
  methods: {
    toggleStatus() {
      if(this.status === 'active') {
        this.status = 'pending';
      } else if(this.status === 'pending') {
        this.status = 'inactive';
      } else {
        this.status = 'active';
      }
    }
   }
};

</script>

<template>
  <h1>{{ name }}</h1>
  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else="status === 'inactive'">User is inactive</p>

  <h3>Task:</h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task  }}</li>
  </ul>
  <a :href="link">Click on google</a>
  <br>
  <!-- <button v-on:click="toggleStatus">Click me</button> -->
  <button @click="toggleStatus">Change me</button>
</template>

<!-- <style scope>

</style> -->