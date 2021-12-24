<template>
  <p @click="handleClick">
    All of your components {{ fname }} {{ mname }} html goes inside these
    template tags
  </p>
</template>

<script>
// All of your components JS code lives within this section
// we can still do things such as `import lib from 'lib'` should we wish
export default {
  name: "simple-component",
  data() {
    return {
      msg: "My Profile Component",
    };
  },
  props: ["fname", "mname"],
  methods: {
    handleClick() {
      this.$emit("clickFromChildComponent", this.fname, this.mname);
    },
  },
};
</script>

<style scoped>
p {
  background-color: orange;
}
</style>
