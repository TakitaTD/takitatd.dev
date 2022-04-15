<template>
    <div :class="$style.Description">
        <slot />
    </div>
</template>

<style scoped module lang="scss">
.Description {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    height: 60%;
    width: 80%;
    color: #fff;
    font-family: 'Alata', sans-serif;
    font-size: 1.2rem;
}
</style>

<script>

</script>