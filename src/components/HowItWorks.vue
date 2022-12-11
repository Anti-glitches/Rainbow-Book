<script>
export default {
    methods: {
        redirect(event) {
            window.location.href =
                "https://sfd1jmu87ts.typeform.com/to/YsFn0h1h";
        },
    },
};
</script>

<template>
    <div id="how_section">
        <h2>How it works</h2>
        <div class="container_body">
            <div class="content_container">
                <div class="content_body">
                    <span class="number_styling">1</span>
                    <h3>Answer a few questions</h3>
                    <p>
                        Guiding your child along a few question to help them
                        build their stories
                    </p>
                </div>
                <img src="/how/how1.png" alt="image" />
            </div>
            <div class="content_container">
                <div class="content_body">
                    <span class="number_styling">2</span>
                    <h3>AI generated page</h3>
                    <p>Our AI generates illustrations for each page</p>
                </div>
                <img src="/how/how2.png" alt="image" />
            </div>
            <div class="content_container">
                <div class="content_body">
                    <span class="number_styling">3</span>
                    <h3>Pick the best illustration</h3>
                    <p>
                        You and your child pick your favourite illustrations for
                        each page
                    </p>
                </div>
                <img src="/how/how3.png" alt="image" />
            </div>
            <div class="content_container">
                <div class="content_body">
                    <span class="number_styling">4</span>
                    <h3>Get a storybook</h3>
                    <p>We make the final book and send it to you!</p>
                </div>
                <img src="/how/how4.png" alt="image" />
            </div>
        </div>
        <button @click="redirect" class="main_button">Start your story</button>
    </div>
</template>

<style scoped lang="scss">
#how_section {
    display: flex;
    flex-direction: column;

    h2 {
        text-align: center;
        margin-bottom: 4rem;
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
            width: 400px;
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

@media (max-width: 768px) {
    #how_section {
        // background: #000;

        .container_body {
            .content_container {
                display: flex;
                flex-direction: column;
                text-align: center;

                .content_body {
                    order: 2;
                    display: flex;
                    flex-direction: column;
                    align-items: center;

                    .number_styling {
                        margin-bottom: 1.5rem;
                    }
                }

                img {
                    order: 1;
                    width: 300px;
                }
            }
        }
    }
}
</style>
