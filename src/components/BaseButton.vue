<template>
  <div>
    <button type="button" > {{ text }}</button>
  </div>
</template>

<script>
export default {
    name: "BaseButton",
    props:{ text: String}
}
</script>

<style scoped lang="scss">
@import "../assets/sass/style.scss";

button {
  text-transform: capitalize;
  padding: 10px 15px;
  border-radius: 10px;
  border-color: $denim;
  background-color: $denim;
  color: white;
}
</style>