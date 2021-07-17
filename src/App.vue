<template>
  <Dashboard />
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Dashboard from './views/Dashboard/Index.vue'

export default defineComponent({
  name: 'App',
  components: {
    Dashboard
  }
})
</script>

<style>
</style>
