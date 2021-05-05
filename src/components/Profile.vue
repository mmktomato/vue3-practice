<template>
  <Header>Profile</Header>

  <div class="body">
    <div>
      <Label value="Name" htmlFor="name" />
      <Input v-model:myValue="name" id="name" />
    </div>

    <div>
      <Label value="Nickname" htmlFor="nickname" />
      <Input v-model:myValue="nickname" id="nickname" />
    </div>
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
      nickname: "",
    }
  },
  methods: {
    onUpdateClick() {
      const str = `Name: ${this.name}
Nickname: ${this.nickname}`;

      alert(str);
    }
  }
});
</script>

<style lang="scss" scoped>
.body {
  margin: 24px 0 36px 0;
  display: grid;
  row-gap: 12px;
}

.button-row {
  text-align: right;
}
</style>