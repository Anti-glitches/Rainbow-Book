<script setup>
import HowItWorks from "./components/HowItWorks.vue";
import Book from "./components/Book.vue";
import Footer from "./components/Footer.vue";
import Hero from "./components/Hero.vue";
// import Navbar from "./components/Navbar.vue";
import Pricing from "./components/Pricing.vue";
</script>

<template>
    <div id="app">
        <hero />
        <Book />
        <HowItWorks />
        <Pricing />
        <Footer />
    </div>
</template>

<style lang="scss" scoped>
#app {
    display: flex;
    flex-direction: column;
    gap: 200px;
    max-width: 1400px;
    margin: 0 auto;
}
</style>
