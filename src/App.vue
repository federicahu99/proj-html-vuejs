<template>
  <div>
    <BaseHeader :menuHeader="menuHeader" />
    <BaseJumbotron />
    <AwardSection />
  </div>
</template>

<script>
import BaseHeader from "./components/BaseHeader.vue";
import BaseJumbotron from "./components/BaseJumbotron.vue";
import AwardSection from "./components/AwardSection.vue";

export default {
  name: 'App',
  components: {
    BaseHeader, 
    BaseJumbotron,
    AwardSection,
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
