<template>
    <nav :class="$style.NavBar">
        <router-link v-for="item in items" :key="item.name" :to="item.link"> {{ item.name }} </router-link>
    </nav>
</template>

<style scoped module lang="scss">
.NavBar {
    display: flex;
    justify-content: space-around;
    position: absolute;
    top: 10%;
    width: 80%;
    height: 7vh;
    z-index: 10;
    a {
        display: flex;
        color: #000;
        text-decoration: none;
        font-family: 'Alata', sans-serif;
        border-radius: 0.1rem;
        background-color: rgba(255,255,255,0.25);
        width: 20%;
        justify-content: center;
        align-items: center;
        text-align: center;
        transition: all .3s
    }
    a:hover {
        background-color: rgba(255,255,255,1);
        box-shadow: .4rem .4rem #d8dee9;
    }
    a:active {
        box-shadow: 0 0 #d8dee9;
        transition: all .2s
    }
}


</style>

<script>
export default {
    props: {
        items: Array
    }
}
</script>