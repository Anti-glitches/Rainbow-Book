<template>
    <div class="cards">
        <div class="card a">1</div>
        <div class="card b">1</div>
        <div class="card c">1</div>
    </div>
</template>

<style lang="scss" scoped>
.cards {
    display: grid;
    grid-template-areas:
        "a a"
        "b c";
}

.card {
    width: 100%;
    height: 100px;
    background: red;
}

.a {
    grid-area: a;
    background: aliceblue;
}
</style>