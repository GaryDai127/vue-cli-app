<template>
  <div id="app">
    <text-field
      :label="'First Name'"
      v-model="firstName"
      :textLimit="15"
    ></text-field>
    <text-field
      :label="'Last Name'"
      v-model="lastName"
      :textLimit="15"
    ></text-field>
    <div>{{ getFullName }}</div>
  </div>
</template>

<script>
import TextField from "./components/TextField";

export default {
  name: "app",
  data() {
    return {
      firstName: "",
      lastName: ""
    };
  },
  components: {
    TextField
  },
  computed: {
    getFullName() {
      return this.firstName + " " + this.lastName;
    }
  }
};
</script>

<style></style>
