<template>
    <header :class="$style.header">
      <slot />
    </header>
</template>

<script>
export default {
    name: 'HeaderComponent',
    
}
</script>

<style module scoped lang="scss">
.header {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 2rem;
  color: #fff;
  margin-top: 1rem;
  font-family: "Alata", sans-serif;
}
</style>