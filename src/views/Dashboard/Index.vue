<template>
  <p>ダッシュボードのインデックス</p>
  <Drawer />
</template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";
import Drawer from "./components/Drawer.vue";
export default defineComponent({
  name: 'Dashboard',
  components: {
    Drawer,
  },
})
</script>