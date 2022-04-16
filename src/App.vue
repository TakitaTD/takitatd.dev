<template>
  <NavBar :items="items" />
  <router-view />
  <div class="custom-shape-divider-bottom-1650015782">
    <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
        <path d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z" class="shape-fill"></path>
    </svg>
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";

export default {
  name: "App",
  components: {
    NavBar,
  },
  data() {
    return {
      items: [{name: "About", link: "/About/"}, { name: "Home", link: "/" }, {name: "Contact Me", link: "/Contact/"}],
    };
  },
};
</script>

<style lang="scss">
#app {
  display: flex;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
  height: 100%;
  justify-content: center;
  align-items: center;
  background-image: linear-gradient(to bottom right, #49bc62, #426fb2);
}
.custom-shape-divider-bottom-1650015782 {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    overflow: hidden;
    line-height: 0;
    transform: rotate(180deg);
}

.custom-shape-divider-bottom-1650015782 svg {
    position: relative;
    display: block;
    width: calc(100% + 1.3px);
    height: 162px;
}

.custom-shape-divider-bottom-1650015782 .shape-fill {
    fill: #2e3440;
}
</style>
