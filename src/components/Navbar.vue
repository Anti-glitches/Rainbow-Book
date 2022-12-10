<template>
    <nav>
        <img src="/logo.svg" alt="logo" />

        <div class="nav_links">
            <ul>
                <li><a href="#book_section">Example</a></li>
                <li><a href="#how_section">How it works?</a></li>
                <li><a href="#pricing_section">Pricing</a></li>
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

@media (max-width: 768px) {
    nav {
        justify-content: center;
        .nav_links {
            display: none;
        }
    }
}
</style>