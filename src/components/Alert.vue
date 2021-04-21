<template>
  <div class="alert" :class="mode" role="alert">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "Alert",
  props: ["mode"],
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.alert {
  position: relative;
  padding: 1rem 1rem;
  margin-bottom: 1rem;
  border: 1px solid transparent;
  border-radius: 10px;
}
.success {
  color: #fff;
  background-color: #1abb72;
  border-color: #1abb72;
}
.danger {
  color: #fff;
  background-color: #b50f0f;
  border-color: #badbcc;
}
.primary {
  color: #fff;
  background-color: #d3d3d4;
  border-color: #d3d3d4;
}
</style>
