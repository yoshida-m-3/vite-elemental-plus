<template>
  <p>ダッシュボードのインデックス</p>
  <NavMenu />
</template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";
import NavMenu from "./components/NavMenu.vue";
export default defineComponent({
  name: 'Dashboard',
  components: {
    NavMenu,
  },
})
</script>