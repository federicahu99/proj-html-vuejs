<template>
  <div>
    <BaseHeader :menuHeader="menuHeader" />
  </div>
</template>

<script>
import BaseHeader from "./components/BaseHeader.vue";

export default {
  name: 'App',
  components: {
    BaseHeader
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
