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
  font-size: 24px;
}
</style>