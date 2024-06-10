<template>
    <footer>
        <section class="left-sec">
            <button>Sign-up now!</button>
        </section>
        <section class="right-sec">
            <h1>Follow us</h1>
            <div v-for="(icon, index) in socialIcons" :key="index" class="social-icon">
                <img :src="icon.src" :alt="icon.alt">
            </div>
        </section>
    </footer>
</template>

<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            socialIcons: [
                { src: '/src/assets/img/img/footer-facebook.png', alt: 'Facebook' },
                { src: '/src/assets/img/img/footer-periscope.png', alt: 'Periscope' },
                { src: '/src/assets/img/img/footer-pinterest.png', alt: 'Pinterest' },
                { src: '/src/assets/img/img/footer-twitter.png', alt: 'Twitter' },
                { src: '/src/assets/img/img/footer-youtube.png', alt: 'YouTube' }
            ]
        };
    }
}
</script>

<style lang="scss" scoped>

footer {
    background-color: #303030;
    display: flex;
    justify-content: space-between;
    padding: 4rem;
}

button {
    padding: 1rem;
    background-color: #303030;
    border: 3px solid #0282f9;
    color: white;
    text-transform: uppercase;
    font-size: 1.2rem;
}

h1{
    text-transform: uppercase;
    color: #0282f9;
    margin-right: .5rem;
    padding:0.5rem;
}

.right-sec{
    display: flex;
    align-items: center;
}

img{
    margin-right: .5rem;
    width: 100%;
    padding:.5rem
}

</style>