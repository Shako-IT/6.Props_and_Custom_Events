<template>
  <section>
    <form @submit.prevent="submitData">
      <label>User name</label>
      <input typ="text" placeholder="Your name" v-model="enteredName" />
      <label>Age</label>
      <input typ="text" placeholder="Your age" v-model="enteredAge" />
      <button>Set user data</button>
    </form>
  </section>
</template>

<script>
export default {
  emits: ["set-data"],
  data() {
    return {
      enteredName: "",
      enteredAge: "",
    };
  },
  methods: {
    submitData() {
      this.$emit("set-data", this.enteredName, this.enteredAge);
    },
  },
};
</script>
