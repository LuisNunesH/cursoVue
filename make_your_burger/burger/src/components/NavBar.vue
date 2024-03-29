<template>
    <nav>
        <RouterLink to="/">
            <img :alt="alt" :src="logo" id="logo" />
        </RouterLink>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/pedidos">Pedidos</RouterLink>
    </nav>
</template>
<script>
    export default {
        name: 'NavBar',
        props: ["logo", "alt"]
    }
</script>
<style scoped>
    #nav {
        background-color: 
    }
</style>