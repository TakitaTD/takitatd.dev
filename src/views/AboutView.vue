<template>
  <Content style="top: 0; left: 0">
    <Card style="top: 17%; width: 70%; min-height: 60%">
      <Header>
        <span> About Me <img src @error="headerType" /></span>
      </Header>
      <Description>
        <p>
          My name is Tim, I started coding shitty websites at the age of 8 years
          old. I was interested in becoming a software engineer when I grew up.
        </p>
        <p>
          I started experimenting with Linux on my school chromebook when I was
          9 and a half years old, and was finally able to install nodejs and
          start using libraries like React, Svelte and Vue.js. I finally got a
          good laptop at the age of 11 and started programming in desktop
          languages like c# and c++.
        </p>
        <p>
          I'm half-japanese and enjoy playing videogames, watching Netflix and
          YouTube.
        </p>
      </Description>
    </Card>
  </Content>
  <Content
    :style="
      'bottom: -117%;background-image: url(\'' +
      nord_buildings +
      '\');background-size: 50%;background-repeat: no-repeat;background-position: center, center'
    "
  >
    <Card
      style="
        top: 17%;
        width: 70%;
        min-height: 60%;
        background-color: rgba(255, 255, 255, 0.05);
      "
    >
      <Header>
        <span style="display: flex; flex-direction: column">
          Technologies
          <span
            style="
              font-size: 1rem;
              padding: 0.2rem;
              background-color: rgba(0, 0, 0, 0.5);
              border-radius: 0.1rem;
            "
          >
            These are the technologies I'm comfortable with
          </span>
        </span>
      </Header>
      <Description
        style="
          color: #d8dee9;
          margin-top: 1rem;
          display: flex;
          flex-direction: row;
          justify-content: space-around;
          flex-wrap: wrap;
        "
      >
        <Technology
          v-for="item in technologies"
          :link="item.link"
          :name="item.name"
          :logo="item.image"
          :key="item.name"
        />
      </Description>
    </Card>
  </Content>
</template>

<script>
import CardComponent from "@/components/CardComponent.vue";
import HeaderComponent from "@/components/HeaderComponent.vue";
import DescriptionComponent from "@/components/DescriptionComponent.vue";
import ContentComponent from "@/components/ContentComponent.vue";
import TechnologyComponent from "@/components/TechnologyComponent.vue";

import nord_buildings from "@/assets/nord_buildings.png";
import logo from "@/assets/logo.png";
import reactLogo from "@/assets/react.js.png";
import angularLogo from "@/assets/angular.png";
import nuxtLogo from "@/assets/nuxt.js.svg";
import sassLogo from "@/assets/sass.png";
import cssLogo from "@/assets/css.jpg";
import htmlLogo from "@/assets/html.png";
import svelteLogo from "@/assets/svelte.png";
import solidjsLogo from "@/assets/solid.js.png";

import TypedJS from "typed.js";

export default {
  name: "AboutView",
  components: {
    Card: CardComponent,
    Header: HeaderComponent,
    Description: DescriptionComponent,
    Content: ContentComponent,
    Technology: TechnologyComponent,
  },
  data() {
    return {
      nord_buildings,
      technologies: [
        { name: "Vue.js", link: "https://vuejs.org/", image: logo },
        {
          name: "Next.js",
          link: "https://nextjs.org/",
          image:
            "data:image/png;base64,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",
        },
        {
          name: "React.js",
          link: "https://reactjs.org/",
          image: reactLogo,
        },
        {
          name: "Angular",
          link: "https://angular.io/",
          image: angularLogo,
        },
        {
          name: "Nuxt.js",
          link: "https://nuxtjs.org/",
          image: nuxtLogo,
        },
        {
          name: "Svelte",
          link: "https://svelte.dev/",
          image: svelteLogo,
        },
        {
          name: "Solid.js",
          link: "https://solidjs.com/",
          image: solidjsLogo,
        },
        {
          name: "Sass",
          link: "https://sass-lang.com/",
          image: sassLogo,
        },
        {
          name: "CSS",
          link: "https://www.w3.org/Style/CSS/Overview.en.html",
          image: cssLogo,
        },
        {
          name: "HTML",
          link: "https://www.w3.org/html/",
          image: htmlLogo,
        },
      ],
    };
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
