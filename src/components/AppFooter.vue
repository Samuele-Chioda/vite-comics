<template>
    <footer>
        <section class="left-sec">
            <button>Sign-up now!</button>
        </section>
        <section class="right-sec">
            <h1>
                Follow us
            </h1>
            <img src="../assets/img/img/footer-facebook.png" alt="">
            <img src="../assets/img/img/footer-periscope.png" alt="">
            <img src="../assets/img/img/footer-pinterest.png" alt="">
            <img src="../assets/img/img/footer-twitter.png" alt="">
            <img src="../assets/img/img/footer-youtube.png" alt="">
        </section>
    </footer>
</template>

<script>
export default {
    name: 'AppFooter'
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
}

img{
    margin-right: .5rem;
    width: 100%;
    padding:.5rem
}

</style>