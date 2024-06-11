<template>

    <main>
        <div class="black-section">
            <AppImg />
        </div>
        <div class="blue-section">
            <section class="last-photo d-flex" v-for="(info, index) in infos" :key="index">
                <img class="info" :src="info.src" :alt="info.alt">
                <p>{{ info.text }}</p>
            </section>
        </div>
        <div class="center-section">
            <section id="lists">
                <div class="list first-list">
                    <ul>
                        <li v-for="(item, index) in lists[0]" :key="index">
                            {{ item }}
                        </li>
                    </ul>
                </div>
                <div class="list">
                    <ul>
                        <li v-for="(item, index) in listsDue[0]" :key="index">
                            {{ item }}
                        </li>
                    </ul>
                </div>
                <div class="list">
                    <ul>
                        <li v-for="(item, index) in listsTre[0]" :key="index">
                            {{ item }}
                        </li>
                    </ul>
                </div>
            </section>

            <div class="logo-grande">
                <img class="logo-grande" src="../assets/img/img/dc-logo-bg.png" alt="logo-grande">
            </div>
        </div>
    </main>

</template>

<script>

import AppImg from './AppImg.vue'

export default {
    name: 'AppMain',
    data() {
        return {
            infos: [
                { src: '/src/assets/img/img/buy-comics-digital-comics.png', alt: 'Digital Comics', text: 'Digital Comics' },
                { src: '/src/assets/img/img/buy-comics-merchandise.png', alt: 'DC Merchandise', text: 'DC Merchandise' },
                { src: '/src/assets/img/img/buy-comics-shop-locator.png', alt: 'Locator', text: 'Locator' },
                { src: '/src/assets/img/img/buy-comics-subscriptions.png', alt: 'Subscription', text: 'Subscription' },
                { src: '/src/assets/img/img/buy-dc-power-visa.svg', alt: 'Power Visa', text: 'Power Visa' }
            ],
            lists: [
                ["DC Comics", "Characters", "Movies", "Tv", "Games", "Videos", "News", "Shop", "Shop DC", "Shop DC Collectibles"]
            ],
            listsDue: [
                ["DC", "Terms Of Us", "Privacy Policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CSPC Certificates", "Ratings", "Shop Help", "Contact Us"]
            ],
            listsTre: [
                ["Sites", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"]
            ]
        };
    },
    components:{
        AppImg
    }
}

</script>


<style lang="scss" scoped>
.black-section {
    background-color: black;
    height: 25vh;
    display: flex;
    align-items: center;
}

.black-section>h1 {
    color: #ffffff;
    padding-left: 8rem;
}

.center-section {
    background-image: url('../assets/img/img/footer-bg.jpg');
    background-repeat: no-repeat;
}

.blue-section {
    background-color: #0282f9;
    height: 30vh;
    color: #ffffff;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 5rem;
    padding: 5rem;
}

.info {
    width: 25%;
    margin: 1rem;
}

p{
    text-transform: uppercase;
    align-self: center;
}
// da qui comincia la parte centrale del main

.logo-grande {
    width: 50%;
    display: flex;
    justify-content: center;
}

.center-section {
    display: flex;
    justify-content: space-around;
    padding: 2rem;
    color: lightgray;
}

li {
    list-style-type: none;
    margin-bottom: .5rem;
}

#lists {
    width: 50%;
    display: flex;
    justify-content: space-evenly;
}

.logo-grande {
    width: 50%;
}

.list ul li:first-child {
    font-size: 1.5rem;
    font-weight: bold;
    color: #ffffff;
    text-transform: uppercase;
}

.last-photo img:last-child {
    width: 4rem;
}

.first-list ul li:nth-child(8) {
    font-size: 1.5rem;
    font-weight: bold;
    margin-top: 2rem;
    text-transform: uppercase;
}

.last-photo:last-of-type img.info {
    width: 4rem;
}

.d-flex{
    display:flex;
}


</style>