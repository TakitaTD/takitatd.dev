<template>
    <div :class="$style.Content">
        <slot />
    </div>
</template>

<script>

</script>

<style module scoped lang="scss">
.Content {
    display: flex;
    width: 100%;
    height: 100%;
    position: absolute;
    justify-content: center;
    align-items: center;
}
</style>