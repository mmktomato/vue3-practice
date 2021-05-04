<template>
  <Label value="Name" htmlFor="name" />
  <Input v-model:myValue="name" id="name" />
  
  <Button @click="onUpdateClick">
    Update
  </Button>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Input from "./Input.vue";
import Label from "./Label.vue";
import Button from "./Button.vue";

export default defineComponent({
  name: "Profile",
  components: {
    Input,
    Label,
    Button,
  },
  data() {
    return {
      name: "",
    }
  },
  methods: {
    onUpdateClick() {
      console.log(this.name);
    }
  }
});
</script>