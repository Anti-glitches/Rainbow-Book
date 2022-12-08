<template>
    <nav>
        <img src="logo.png" alt="logo" />

        <div class="nav_links">
            <ul>
                <li><a href="#">About</a></li>
                <li><a href="#">Pricing</a></li>
                <li><a href="#">How it works?</a></li>
            </ul>

            <button class="main_button">Get started</button>
        </div>
    </nav>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 0;

    .nav_links {
        display: flex;

        ul {
            list-style: none;
            display: flex;

            gap: 25px;

            margin-right: 25px;
        }
    }
}
</style>