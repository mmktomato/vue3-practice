<template>
  <h1 class="header">
    <slot></slot>
  </h1>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: "Header"
})
</script>

<style lang="scss" scoped>
.header {
  margin: 0;
  font-size: 24px;
  border-bottom: 1px solid #1f1f1f;
}
</style>