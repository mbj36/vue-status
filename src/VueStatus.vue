<template>
    <div>
        <slot v-if="isOnline" name="online" />
        <slot v-else name="offline" />
    </div>
</template>

<script>
    const networkEvents = ['online', 'offline'];
    export default {
      name: 'vue-status',
      data() {
        return {
          isOnline: navigator.onLine || false
        };
      },
      created() {
        networkEvents.forEach(event =>
          window.addEventListener(event, this.currentStatus)
        );
      },
      beforeDestroy() {
        networkEvents.forEach(event =>
          window.removeEventListener(event, this.currentStatus)
        );
      },
      methods: {
        currentStatus() {
          this.isOnline = navigator.onLine || false;
          this.$emit('current-status', this.isOnline);
        }
      }
    };
</script>