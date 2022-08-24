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
@import "../assets/sass/style.scss";

button {
  font-size: 13px;
  text-transform: capitalize;
  padding: 8px 12px;
  border-radius: 22px;
  border-color: $denim;
  background-color: $denim;
  color: white;
  border: 0px;

  &:hover,
  &:active {
    border: 2px solid $mercury; // rivedere !!!!!!!!!!!
    color: $mercury;
    background-color: dodgerblue;
    border: none;
  }
}
</style>