<template>
    <div id="how_section">
        <h2>How it works</h2>
        <div class="container_body">
            <div class="content_container" v-for="i in 4" :key="i">
                <div class="content_body">
                    <span class="number_styling">{{ i }}</span>
                    <h3>Answer a few questions</h3>
                    <p>
                        Guiding your child along a few question to help them
                        build their stories
                    </p>
                </div>
                <img :src="`/how/how${i}.png`" alt="image" />
            </div>
        </div>
        <button class="main_button">Start your story</button>
    </div>
</template>

<style scoped lang="scss">
#how_section {
    display: flex;
    flex-direction: column;

    h2 {
        text-align: center;
    }

    button {
        align-self: center;
        margin-top: 40px;
    }
}
.container_body {
    display: flex;
    flex-direction: column;
    row-gap: 80px;

    .content_container:nth-child(2),
    .content_container:nth-child(4) {
        .content_body {
            order: 1;
        }
    }

    .content_container {
        display: flex;
        align-items: center;
        justify-content: space-between;

        img {
            width: 300px;
        }

        .content_body {
            .number_styling {
                display: flex;
                width: 50px;
                height: 50px;
                justify-content: center;
                align-items: center;
                color: white;
                background: var(--primary-purple);
                border: 10px solid var(--secondary-purple);
                border-radius: 100%;
                font-size: 25px;
                font-weight: 700;
            }

            p {
                font-size: 20px;
            }
        }
    }
}
</style>
