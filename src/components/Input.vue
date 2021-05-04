<template>
  <input
    class="input"
    :id="id"
    :value="myValue"
    @input="$emit('update:myValue', $event.target.value)"
  />
</template>

<script lang="ts">
import { defineComponent, computed } from 'vue';
export default defineComponent({
  name: "Input",
  props: {
    myValue: String,
    id: String,
  },
  emits: [
    "update:myValue",
  ],
});
</script>

<style lang="scss" scoped>
.input {
  border: 1px solid #6f6f6f;
  border-radius: 3px;
  line-height: 1.5rem;
  width: 100%;
  padding: 0 5px;
}
</style>