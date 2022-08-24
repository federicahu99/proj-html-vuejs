<template>
  <div>
    <button type="button">{{ text }}</button>
  </div>
</template>

<script>
export default {
  name: "BaseButton",
  props: { text: String }, // prop for the text inside of the button
};
</script>

<style scoped lang="scss">
@import "../assets/sass/_var.scss";

button {
  font-size: 13px;
  text-transform: capitalize;
  padding: 8px 12px;
  border-radius: 22px;
  border-color: $denim;
  background-color: $denim;
  color: white;
  border: 0px;
  transition: 0.4s;

  &:hover,
  &:active {
    outline: 0;
    border: 2px solid $mercury; // rivedere !!!!!!!!!!!
    color: $mercury;
    font-weight: bold;
    background-color: dodgerblue;
    border: none;
    scale: 104%;
  }
}
</style>