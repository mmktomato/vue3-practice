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
@use "../css/variables.scss" as v;

.input {
  border: 1px solid v.$borderColor;
  border-radius: v.$borderRadius;
  line-height: 1.5rem;
  width: 100%;
  padding: 3px 0;
  text-indent: 0.3rem;
}
</style>