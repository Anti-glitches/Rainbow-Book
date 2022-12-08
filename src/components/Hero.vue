<script setup>
import Navbar from "../components/Navbar.vue";
</script>

<template>
    <div id="hero_section">
        <navbar />
        <div class="hero">
            <div>
                <h1>Explore your child limitless imagination</h1>
                <p>Bond with your child to create your own storybook</p>
                <button class="main_button">Create your book</button>
            </div>

            <img src="hero-img.png" alt="hero image" />
        </div>
    </div>
</template>


<style lang="scss" scoped>
#hero_section {
    .hero {
        display: grid;
        grid-template-columns: 1fr 1fr;
        align-items: center;
    }
}
</style>