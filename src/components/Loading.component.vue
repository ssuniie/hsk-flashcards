<template>
  <div v-if="store.getters.isLoading" class="loading">
    <font-awesome-icon icon="circle-notch" class="spinner" size="5x" />
  </div>
</template>

<script lang='ts' setup>
import { useStore } from "vuex";

const store = useStore()
</script>

<style scoped>
.loading {
  position: fixed;
  top: 0;
  height: 100vh;
  width: 100vw;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  z-index: 99999;

  @apply bg-green-800;
  color: white;
}

.loading .spinner {
  @apply animate-spin;
}
</style>
