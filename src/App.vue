<template>
  <div>
    <BaseHeader :menuHeader="menuHeader" />
    <BaseJumbotron />
  </div>
</template>

<script>
import BaseHeader from "./components/BaseHeader.vue";
import BaseJumbotron from "./components/BaseJumbotron.vue";

export default {
  name: 'App',
  components: {
    BaseHeader, 
    BaseJumbotron,
  },
  data() {
    return {
      menuHeader: [ "Home", "Rates", "Testimonials", "Blog", "Contact"]
    }
  }
}
</script>

<style lang="scss">

</style>
