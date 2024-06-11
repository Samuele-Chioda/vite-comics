<template>
    <div class="jumbo-section">
        <img :src="imgSrc" alt="jumbo">
    </div>
</template>

<script>
export default {
    name: 'AppJumbo',
    props: {
        imgSrc: {
            type: String,
            required: true
        }
    }
}
</script>

<style scoped>

.jumbo-section img {
    width: 100%;
    height: auto;
}
</style>