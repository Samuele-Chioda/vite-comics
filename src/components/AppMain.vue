<template>

    <main>
        <div class="black-section">
            <h1>
                --> Content goes here <-- </h1>
        </div>
        <div class="center-section">
            <section class="lists">
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
                ["DC Comics", "Characters", "Movies", "Tv", "Games", "Videos", "News"]
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

// da qui comincia la parte centrale del main

.logo-grande {
    width: 50%;
}

.center-section{
    display: flex;
    justify-content: space-around;
    padding: 2rem;
    color: lightgray;
}

li{
    list-style-type: none;
}

.list{
    width: 50%;
    display: flex;
    
}

.logo-grande{
    width: 50%;
}

</style>