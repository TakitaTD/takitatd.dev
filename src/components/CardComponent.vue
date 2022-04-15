<template>
    <div :class="$style.Content">
        <slot />
    </div>
</template>

<style scoped module lang="scss">
.Content {
    position: absolute;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    margin-top: 2rem;
    border-radius: .3rem;
    background-color: rgba(255,255,255,0.15);
    border: #d8dee9 solid 3px;
    z-index: 5;
}
.Content::after {
    content: '';
    display: flex;
    position: absolute;
    bottom: -25%;
    height: 25%;
    width: 100%;
}
</style>

<script>

</script>