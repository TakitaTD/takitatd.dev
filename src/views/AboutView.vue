<template>
  <Content style="top: 0;left: 0;">
    <Card style="top: 17%; width: 70%; min-height: 60%">
      <Header>
        <span> About Me <img src @error="headerType" /></span>
      </Header>
      <Description>
        <p>
          My name is Tim, I started coding shitty websites at the age of 8.5
          years old. I was interested in becoming a software engineer when I
          grew up.
        </p>
        <p>
          I started experimenting with Linux on my school chromebook when I was
          9.5 years old, and was finally able to install nodejs and start using
          libraries like React, Svelte and Vue.js. I finally got a good laptop
          at the age of 11 and started programming in desktop languages like c#
          and c++.
        </p>
        <p>
          I'm half-japanese and enjoy playing videogames, watching Netflix and
          YouTube.
        </p>
      </Description>
    </Card>
  </Content>
</template>

<script>
import CardComponent from "@/components/CardComponent.vue";
import HeaderComponent from "@/components/HeaderComponent.vue";
import DescriptionComponent from "@/components/DescriptionComponent.vue";
import ContentComponent from "@/components/ContentComponent.vue";
import TypedJS from "typed.js";

export default {
  name: "AboutView",
  components: {
    Card: CardComponent,
    Header: HeaderComponent,
    Description: DescriptionComponent,
    Content: ContentComponent,
  },
  methods: {
    headerType: (e) => {
      /* Yeah, I know this is not good code, but I'm just trying to get by. (btw how the fuck did you get access to this code? Did I die or something?) */
      /* eslint-disable-next-line no-unused-vars */
      const headerType = new TypedJS(e.target.parentNode, {
        strings: ["", "About Me"],
        typeSpeed: 30,
      });
    },
  },
};
</script>

<style></style>
