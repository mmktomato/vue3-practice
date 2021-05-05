<template>
  <Header>Profile</Header>

  <div class="body">
    <Label value="Name" htmlFor="name" />
    <Input v-model:myValue="name" id="name" />
  </div>

  <div class="button-row">
    <Button @click="onUpdateClick">
      Update
    </Button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Input from "./Input.vue";
import Label from "./Label.vue";
import Button from "./Button.vue";
import Header from "./Header.vue";

export default defineComponent({
  name: "Profile",
  components: {
    Input,
    Label,
    Button,
    Header,
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

<style lang="scss" scoped>
.body {
  margin: 24px 0;
}

.button-row {
  text-align: right;
}
</style>