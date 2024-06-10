<template>
    <header>
        <section class="logo">
            <img src="../assets/img/img/dc-logo.png" alt="logo">
        </section>
        <nav>
            <ul>
                <li v-for="(menuItem, index) in menuItems" :key="index">
                    <a :href="menuItem.url">{{ menuItem.text }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
    data() {
        return {
            menuItems: [
                { text: 'Characters', url: '#'},
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

</style>
