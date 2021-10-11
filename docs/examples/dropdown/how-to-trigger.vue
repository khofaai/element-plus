<template>
  <el-row class="block-col-2">
    <el-col :span="6">
      <span class="demonstration">hover to trigger</span>
      <el-dropdown>
        <span class="el-dropdown-link">
          Dropdown List<i class="el-icon-arrow-down el-icon--right"></i>
        </span>
        <template #dropdown>
          <el-dropdown-menu>
            <el-dropdown-item icon="el-icon-plus">Action 1</el-dropdown-item>
            <el-dropdown-item icon="el-icon-circle-plus"
              >Action 2</el-dropdown-item
            >
            <el-dropdown-item icon="el-icon-circle-plus-outline"
              >Action 3</el-dropdown-item
            >
            <el-dropdown-item icon="el-icon-check">Action 4</el-dropdown-item>
            <el-dropdown-item icon="el-icon-circle-check"
              >Action 5</el-dropdown-item
            >
          </el-dropdown-menu>
        </template>
      </el-dropdown>
    </el-col>
    <el-col :span="6">
      <span class="demonstration">click to trigger</span>
      <el-dropdown trigger="click">
        <span class="el-dropdown-link">
          Dropdown List<i class="el-icon-arrow-down el-icon--right"></i>
        </span>
        <template #dropdown>
          <el-dropdown-menu>
            <el-dropdown-item icon="el-icon-plus">Action 1</el-dropdown-item>
            <el-dropdown-item icon="el-icon-circle-plus"
              >Action 2</el-dropdown-item
            >
            <el-dropdown-item icon="el-icon-circle-plus-outline"
              >Action 3</el-dropdown-item
            >
            <el-dropdown-item icon="el-icon-check">Action 4</el-dropdown-item>
            <el-dropdown-item icon="el-icon-circle-check"
              >Action 5</el-dropdown-item
            >
          </el-dropdown-menu>
        </template>
      </el-dropdown>
    </el-col>
    <el-col :span="6">
      <span class="demonstration">right click to trigger</span>
      <el-dropdown trigger="contextmenu">
        <span class="el-dropdown-link">
          Dropdown List<i class="el-icon-arrow-down el-icon--right"></i>
        </span>
        <template #dropdown>
          <el-dropdown-menu>
            <el-dropdown-item icon="el-icon-plus">Action 1</el-dropdown-item>
            <el-dropdown-item icon="el-icon-circle-plus"
              >Action 2</el-dropdown-item
            >
            <el-dropdown-item icon="el-icon-circle-plus-outline"
              >Action 3</el-dropdown-item
            >
            <el-dropdown-item icon="el-icon-check">Action 4</el-dropdown-item>
            <el-dropdown-item icon="el-icon-circle-check"
              >Action 5</el-dropdown-item
            >
          </el-dropdown-menu>
        </template>
      </el-dropdown>
    </el-col>
    <el-col :span="6">
      <span class="demonstration">custom trigger</span>
      <el-dropdown v-model:visibility="visibility" trigger="custom">
        <span class="el-dropdown-link" @click="handleToggle">
          Dropdown List<i class="el-icon-arrow-down el-icon--right"></i>
        </span>
        <template #dropdown>
          <el-dropdown-menu>
            <el-dropdown-item icon="el-icon-plus">Action 1</el-dropdown-item>
            <el-dropdown-item icon="el-icon-circle-plus"
              >Action 2</el-dropdown-item
            >
            <el-dropdown-item icon="el-icon-circle-plus-outline"
              >Action 3</el-dropdown-item
            >
            <el-dropdown-item icon="el-icon-check">Action 4</el-dropdown-item>
            <el-dropdown-item icon="el-icon-circle-check"
              >Action 5</el-dropdown-item
            >
          </el-dropdown-menu>
        </template>
      </el-dropdown>
    </el-col>
  </el-row>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const visibility = ref(false)

const handleToggle = () => {
  visibility.value = !visibility.value
}
</script>

<style>
.el-dropdown-link {
  cursor: pointer;
  color: #409eff;
}
.el-icon-arrow-down {
  font-size: 12px;
}
.demonstration {
  display: block;
  color: var(--el-text-color-secondary);
  font-size: 14px;
  margin-bottom: 20px;
}
</style>
