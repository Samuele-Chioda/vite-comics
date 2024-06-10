<template>

    <main>
        <div class="black-section">
            <h1>
                --> Content goes here <-- </h1>
        </div>
        <div class="blue-section">
            
            <section>
                <img class="info" src="../assets/img/img/buy-comics-digital-comics.png" alt="">
                <p>Digital Comics</p>
            </section>
            <section>
                <img class="info" src="../assets/img/img/buy-comics-merchandise.png" alt="">
                <p>DC merchandise</p>
            </section>
            <section>
                <img class="info" src="../assets/img/img/buy-comics-shop-locator.png" alt="">
                <p>Locator</p>
            </section>
            <section>
                <img class="info" src="../assets/img/img/buy-comics-subscriptions.png" alt="">
                <p>Subscription</p>
            </section>
            <section>
                <img class="info" src="../assets/img/img/buy-dc-power-visa.svg" alt="">
                <p>Power Visa</p>
            </section>
        </div>
        <div class="center-section">
            <section id="lists">
                <div class="list">
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
export default {
    name: 'AppMain',
    data() {
        return {
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
    color: white;
    padding-left: 8rem;
}

.center-section {
    background-image: url('../assets/img/img/footer-bg.jpg');
    background-repeat: no-repeat;
}

.blue-section {
    background-color: #0282f9;
    height: 30vh;
    color: white;
    display: flex;
    justify-content: space-around;
    align-items: center;
}

.info{
    width: 50%;
}

// da qui comincia la parte centrale del main

.logo-grande {
    width: 50%;
}

.center-section {
    display: flex;
    justify-content: space-around;
    padding: 2rem;
    color: lightgray;
}

li {
    list-style-type: none;
}

#lists {
    width: 50%;
    display: flex;
    justify-content: space-evenly;

}

.logo-grande {
    width: 50%;
}
</style>