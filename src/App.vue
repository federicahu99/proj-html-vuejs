<template>
  <div>
    <BaseHeader :menuHeader="menuHeader" />
    <BaseJumbotron />
    <AwardSection />
    <ServicesSection fullService="fullService" />
  </div>
</template>

<script>
import BaseHeader from "./components/BaseHeader.vue";
import BaseJumbotron from "./components/BaseJumbotron.vue";
import AwardSection from "./components/AwardSection.vue";
import ServicesSection from "./components/ServicesSection.vue";

export default {
  name: "App",
  components: {
    BaseHeader,
    BaseJumbotron,
    AwardSection,
    ServicesSection,
  },
  data() {
    return {
      menuHeader: [
        // header links
        { name: "Home", link: "#" },
        { name: "Rates", link: "#" },
        { name: "Testimonials", link: "#" },
        { name: "Blog", link: "#" },
        { name: "Contact", link: "#" },
      ],

      menuFooterLeft: [
        { name: "Home", link: "#" },
        { name: "Rates", link: "#" },
        { name: "Testimonials", link: "#" },
        { name: "Blog", link: "#" },
        { name: "Free Quote", link: "#" },
      ],

      menuFooterRight: [
        { name: "Heading out to college?", link: "#" },
        { name: "Moving your business?", link: "#" },
        { name: "Outstainding quality?", link: "#" },
        { name: "Cost of moving?", link: "#" },
        { name: "Best Moving tips?", link: "#" },
      ],

      fullService: [
        // three card service section + three btn
        {
          img: "avada-movers-serviceonephoto-final-400x255.jpg",
          title: "two man lift",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic laboriosam debitis laudantium assumenda quam repellat repellendus praesentium, neque tempore harum aspernatur.",
          btn: "read more",
        },
        {
          img: "avada-movers-servicetwophoto-final-400x255.jpg",
          title: "we do all the lifting",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic laboriosam debitis laudantium assumenda quam repellat repellendus praesentium, neque tempore harum aspernatur.",
          btn: "read more",
        },
        {
          img: "avada-movers-servicethreephoto-final-400x255.jpg",
          title: "coast to coast",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic laboriosam debitis laudantium assumenda quam repellat repellendus praesentium, neque tempore harum aspernatur.",
          btn: "read more",
        },
      ],

      testimonials: [
        //three testimonial + one btn
        {
          img: "avada-movers-janedoe-final-200x200.jpg",
          name: "John Doe",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic laboriosam debitis laudantium assumenda quam repellat repellendus praesentium, neque tempore harum aspernatur.",
        },
        {
          img: "avada-movers-johndoe-final-200x200.jpg",
          name: "Jane Doe",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic laboriosam debitis laudantium assumenda quam repellat repellendus praesentium, neque tempore harum aspernatur.",
        },
        {
          img: "avada-movers-johnsmith-final-200x200.jpg",
          name: "John Smith",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic laboriosam debitis laudantium assumenda quam repellat repellendus praesentium, neque tempore harum aspernatur.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
</style>
