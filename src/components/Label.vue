<template>
  <label class="label" :for="htmlFor">{{ value }}</label>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: "Label",
  props: {
    value: String,
    htmlFor: String,
  }
})
</script>

<style lang="scss" scoped>
.label {
  color: #4e4e4e;
  font-weight: 600;
}
</style>