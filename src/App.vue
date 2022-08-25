<template>
  <div>
    <BaseHeader :menuHeader="menuHeader" />
    <BaseJumbotron />
    <AwardSection />
    <ServiceSection :fullService="fullService" />
    <SloganSection />
    <TestimonialSection :testimonials="testimonials" />
    <FreeQuoteSection />
    <BaseFooter
      :menuFooterLeft="menuFooterLeft"
      :menuFooterRight="menuFooterRight"
      :menuFooterBottom="menuFooterBottom"
    />
  </div>
</template>

<script>
import BaseHeader from "./components/BaseHeader.vue";
import BaseJumbotron from "./components/BaseJumbotron.vue";
import AwardSection from "./components/AwardSection.vue";
import ServiceSection from "./components/ServiceSection.vue";
import SloganSection from "./components/SloganSection.vue";
import TestimonialSection from "./components/TestimonialSection.vue";
import FreeQuoteSection from "./components/FreeQuoteSection.vue";
import BaseFooter from "./components/BaseFooter.vue";

export default {
  name: "App",
  components: {
    BaseHeader,
    BaseJumbotron,
    AwardSection,
    ServiceSection,
    SloganSection,
    TestimonialSection,
    FreeQuoteSection,
    BaseFooter,
  },
  data() {
    return {
      menuHeader: [
        // header links
        { link: "Home", url: "#" },
        { link: "Rates", url: "#" },
        { link: "Testimonials", url: "#" },
        { link: "Blog", url: "#" },
        { link: "Contact", url: "#" },
      ],

      menuFooterLeft: [
        { link: "Home", url: "#" },
        { link: "Rates", url: "#" },
        { link: "Testimonials", url: "#" },
        { link: "Blog", url: "#" },
        { link: "Free Quote", url: "#" },
      ],

      menuFooterRight: [
        { link: "Heading out to college?", url: "#" },
        { link: "Moving your business?", url: "#" },
        { link: "Outstainding quality?", url: "#" },
        { link: "Cost of moving?", url: "#" },
        { link: "Best Moving tips?", url: "#" },
      ],

      menuFooterBottom: [
        { link: "Copyright 2012 - 2020", url: "#" },
        { link: "Avada Theme by ThemeFusion", url: "#" },
        { link: "All Right Reserved", url: "#" },
        { link: "Powered by WordPress", url: "#" },
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
          title: "we do all the lift",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic laboriosam debitis laudantium assumenda quam, neque tempore harum aspernatur.",
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
          nameLastname: "jane doe",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic laboriosam debitis laudantium assumenda quam repellat repellendus praesentium, neque tempore harum aspernatur.",
        },
        {
          img: "avada-movers-johndoe-final-200x200.jpg",
          nameLastname: "john doe",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic laboriosam debitis laudantium assumenda quam repellat repellendus praesentium, neque tempore harum aspernatur.",
        },
        {
          img: "avada-movers-johnsmith-final-200x200.jpg",
          nameLastname: "john smith",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic laboriosam debitis laudantium assumenda quam repellat repellendus praesentium, neque tempore harum aspernatur.",
        },
      ],
    };
  },
};
</script>

