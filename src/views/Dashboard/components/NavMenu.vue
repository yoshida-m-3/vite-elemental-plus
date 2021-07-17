<template>
    <el-radio-group v-model="isCollapse" style="margin-bottom: 20px;">
      <el-radio-button :label="false">expand</el-radio-button>
      <el-radio-button :label="true">collapse</el-radio-button>
    </el-radio-group>

    <el-menu
      default-active="2"
      class="el-menu-vertical-demo"
      :collapse="isCollapse"
      @open="handleOpen"
      @close="handleClose">
      <el-submenu index="1">
        <template #title>
          <i class="el-icon-location"></i>
          <span>Navigator One</span>
        </template>
        <el-menu-item-group title="Group One">
          <el-menu-item index="1-1">item one</el-menu-item>
          <el-menu-item index="1-2">item one</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group title="Group Two">
          <el-menu-item index="1-3">item three</el-menu-item>
        </el-menu-item-group>
        <el-submenu index="1-4">
          <template #title>item four</template>
          <el-menu-item index="1-4-1">item one</el-menu-item>
        </el-submenu>
      </el-submenu>
      <el-submenu index="2">
        <template #title>
          <i class="el-icon-menu"></i>
          <span>Navigator Two</span>
        </template>
          <el-menu-item index="2-1">item one</el-menu-item>
          <el-menu-item index="2-2">item one</el-menu-item>
      </el-submenu>
    </el-menu>
</template>

<script lang="ts">import { defineComponent, ref } from "@vue/runtime-core";

export default defineComponent({
    name: 'NavMenu',
    setup: () => {
      const isCollapse = ref(true);
      const handleOpen = (key: number, keyPath: string) => {
        console.log(key, keyPath);
      };
      const handleClose = (key: number, keyPath: string) => {
        console.log(key, keyPath);
      };
      return {
        isCollapse,
        handleOpen,
        handleClose,
      };
    },
})
</script>