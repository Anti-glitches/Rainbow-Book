<template>
    <div id="book_section">
        <h3>Read Maryam’s book</h3>
        <div class="book_left">
            <div class="aside_container">
                <p class="small_title">What was inputted</p>

                <p class="purple_container">One unicorn flied</p>
                <p class="purple_container">She brakes her horn</p>
                <p class="purple_container">
                    And then a tie went in the hole where the horn was
                </p>
                <p class="purple_container">
                    And then a Zipper landed on the tie
                </p>
                <p class="purple_container">
                    Then she ate a cookie and notice she didn’t have a horn
                </p>
                <p class="purple_container">Then she got a new horn</p>
                <p class="purple_container">The end</p>

                <div class="footer">
                    <p>Convert into a storybook</p>
                    <img src="/arrow-right.png" alt="" />
                </div>
            </div>
        </div>

        <swiper class="mySwiper unselectable">
            <swiper-slide v-for="i in 8" :key="i">
                <img :src="`/book/page${i}.png`" :alt="`page ${i}`" />
            </swiper-slide>
            <p class="drag">Drag to read</p>
        </swiper>
    </div>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

// import "./style.css";

export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        return {};
    },
};
</script>

<style lang="scss" scoped>
#book_section {
    display: grid;
    grid-template-columns: 1fr 2fr;
    grid-template-areas:
        "title title"
        "before book";
    gap: 2rem;
    height: min-content;
    align-items: center;
    position: relative;

    h3 {
        grid-area: title;
    }

    .book_left {
        grid-area: before;

        .aside_container {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            width: auto;
            height: max-content;
            box-shadow: 8px 8px var(--primary-purple);
            border: 2px solid var(--primary-purple);

            .small_title {
                font-family: var(--font1);
                font-size: 25px;
                font-weight: 700;
                margin-top: 0;
                text-align: center;
            }

            .purple_container {
                background: var(--primary-purple);
                color: white;
                padding: 10px 20px;
                border-radius: 10px;
                margin: 5px auto;
                width: fit-content;
                text-align: center;
            }

            .footer {
                display: grid;
                grid-template-columns: 1fr 1fr;
                align-items: center;
                gap: 20px;

                p {
                    font-family: var(--font1);
                    font-size: 1.5rem;
                }

                img {
                    width: 100px;
                    height: fit-content;
                    justify-self: end;
                }
            }
        }
    }

    .swiper {
        grid-area: book;
        // width: 100%;
        height: fit-content;
        width: auto;
        border-radius: 10px;
        margin: 0;
        cursor: grab;
        position: relative;

        .drag {
            position: absolute;
            z-index: 999;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            margin: 0;
            color: white;
            background: var(--secondary-purple);
            padding: 5px 20px;
            border-radius: 10px;
            opacity: 0.75;
        }
    }
    .swiper-slide {
        text-align: center;
        font-size: 18px;
        background: #fff;

        /* Center slide text vertically */
        display: -webkit-box;
        display: -ms-flexbox;
        display: -webkit-flex;
        display: flex;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        -webkit-justify-content: center;
        justify-content: center;
        -webkit-box-align: center;
        -ms-flex-align: center;
        -webkit-align-items: center;
        align-items: center;
    }

    .swiper-slide img {
        display: block;
        // width: 100vw;
        // height: auto;
        width: 100%;
        height: auto;
        object-fit: cover;
    }
}

@media (max-width: 992px) {
    #book_section {
        display: flex;
        flex-direction: column;
        align-items: unset;

        h3 {
            text-align: center;
        }

        .book_left {
            .aside_container {
                .footer {
                    img {
                        transform: rotate(90deg);
                        width: 60px;
                        height: fit-content;
                    }
                }
            }
        }
    }
}
</style>
