<template>
  <button class="button">
    <slot></slot>
  </button>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: "Button",
})
</script>

<style lang="scss" scoped>
@use "../css/variables.scss" as v;

.button {
  padding: 7px 10px;
  color: #f1f1f1;
  background: #2eacdd;
  border: 1px solid v.$borderColor;
  border-radius: v.$borderRadius;

  &:hover {
    opacity: 0.8;
  }

  &:active {
    opacity: 0.6;
  }
}
</style>
