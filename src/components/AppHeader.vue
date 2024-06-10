<template>

    <header>
        <section class="logo">
            <img src="../assets/img/img/dc-logo.png" alt="logo">
        </section>
        <section class="navbar">
            <ul>
                <li v-for="(menuItem, index) in menuItems" :key="index">
                    <a :href="menuItem.url">{{ menuItem.text }}</a>
                </li>
            </ul>
        </section>
    </header>

</template>

<script>

export default {
    data() {
        return {
            menuItems: [
                { text: 'Characters', url: '#' },
                { text: 'Comics', url: '#' },
                { text: 'Movies', url: '#' },
                { text: 'Tv', url: '#' },
                { text: 'Games', url: '#' },
                { text: 'Collectibles', url: '#' },
                { text: 'Videos', url: '#' },
                { text: 'Fans', url: '#' },
                { text: 'News', url: '#' },
                { text: 'Shop', url: '#' }
            ]
        };
    }
};

</script>

<style lang="scss" scoped>
header {
    padding: 2rem;
    display: flex;
    justify-content: space-around;
}

.navbar {
    display: flex;
    justify-content: center;
    align-items: center;
}

ul {
    display: flex;
}

li {
    list-style-type: none;
    margin-right: 2rem;
}

a {
    color: black;
    text-decoration: none;
    text-transform: uppercase;
    font-weight: bolder;
}

a:hover {
    color: #0282f9;

}

li:hover {
    border-bottom: 5px solid #0282f9;
    color: #0282f9;
}
</style>
