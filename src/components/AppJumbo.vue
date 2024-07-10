<script>
export default {
    name: 'AppJumbo',
}
</script>

<template>
    <section class="jumbotron">
        <img src="../assets/jumbotron.jpg" alt="DC Comics">
    </section>
</template>

<style lang="scss" scoped>
.jumbotron {
    height: 20vw;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: 50% 5%;
    }
}
</style>