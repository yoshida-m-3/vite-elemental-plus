<template>
    <el-button type="primary" @click="drawer = true">Open</el-button>
    <el-drawer
      v-model="drawer"
      direction="ltr"
    />
</template>

<script lang="ts">import { defineComponent, ref } from "@vue/runtime-core";

export default defineComponent({
    name: 'Drawer',
    setup: () => {
        const drawer = ref(false);

        return {
            drawer
        };
    },
})
</script>