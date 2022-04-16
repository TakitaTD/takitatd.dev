<template>
  <a :href="link" target="_blank">
    <div :class="$style.card">
      <div :class="$style.logo" :style="'background-image: url(\'' + logo + '\''"/>
      <span>
          {{ name }}
      </span>
    </div>
  </a>
</template>

<script>
export default {
  name: "GridItem",
  props: {
    logo: String,
    name: String,
    link: String
  }
}
</script>

<style scoped module lang="scss">

.card {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  width: 4rem;
  height: 4rem;
  padding: 1rem;
  background-color: rgba(255, 255, 255, 0.05);
  border-radius: 3px;
  position: relative;
  margin: 0.2rem;
  transition: all 300ms;
  span {
    position: absolute;
    bottom: 3px;
    font-family: 'Alata', sans-serif;
  }

  .logo {
    width: 100%;
    height: 3rem;
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center center;
  }

}
a {
  text-decoration: none;
  padding: 0;
  margin: 0;
  color: #fff;
}
a:hover .card {
  background-color: rgba(255,255,255,0.8);
  color: #000;
}
</style>