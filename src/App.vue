<template>
  <section>
    <active-user :username="user.name" :userage="user.age"> </active-user>
    <user-data @set-data="setUserData"></user-data>
  </section>
</template>

<script>
export default {
  data() {
    return {
      user: {
        name: "Shalva",
        age: 33,
      },
    };
  },
  methods: {
    setUserData(name, age) {
      this.user = {
        name: name,
        age: +age,
      };
    },
  },
};
</script>
