<template>
  <vue-status>
    <h2 slot="online">You are online</h2>
    <h2 slot="offline">You are offline</h2>
  </vue-status>
</template>

<script>
  import VueStatus from 'vue-status';
  export default {
    components: {
      VueStatus
    }
  };
</script>
