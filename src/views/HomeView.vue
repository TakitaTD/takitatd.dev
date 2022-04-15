<template>
  <Card style="top: 17%; width: 70%; min-height: 60%">
    <Header>
      <span>
        Welcome to TakitaTD.dev
        <img src @error="headerType" />
      </span>
    </Header>
    <Description style="margin-top: 2rem">
      <p>
        Hello, World! I am TakitaTD. I enjoy coding, math and science. I started
        programming with JavaScript at the age of 8 years old
      </p>
      <p>
        I like playing videogames and making websites. I aspire to be a game
        developer.
      </p>
    </Description>
  </Card>
</template>

<script>
import TypedJS from "typed.js";

// @ is an alias to /src
import CardComponent from "@/components/CardComponent.vue";
import DescriptionComponent from "@/components/DescriptionComponent.vue";
import HeaderComponent from "@/components/HeaderComponent.vue";

export default {
  name: "HomeView",
  components: {
    Card: CardComponent,
    Description: DescriptionComponent,
    Header: HeaderComponent,
  },
  data() {},
  methods: {
    headerType: (e) => {
      /* eslint-disable-next-line no-unused-vars */
      const headerType = new TypedJS(e.target.parentNode, {
        strings: ["", "Welcome to TakitaTD.dev"],
        typeSpeed: 60,
      });
      e.target.remove();
    },
  },
};
</script>

<style scoped module lang="scss"></style>
