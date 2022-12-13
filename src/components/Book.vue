<template>
    <div id="book_section">
        <h3>Maryam’s book</h3>
        <!-- <p>
            Maryam told this story (effortlessly) to her dad and he typed it in (on the left). Unicorny created a beautifully illustrated book from her story (right).
        </p> -->
        <div class="book_left">
            <div class="aside_container">
                <p class="small_title">Maryam's story (as she told it)</p>

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
                    <p>Maryam's story got converted into this book</p>
                    <img src="/arrow-right.png" alt="" />
                </div>
            </div>
        </div>

        <swiper
            class="mySwiper unselectable"
            :pagination="{
                type: 'progressbar',
            }"
            :navigation="true"
            :effect="'cards'"
            :grabCursor="true"
            :modules="modules"
        >
            <swiper-slide v-for="i in 8" :key="i">
                <img :src="`/book/page${i}.png`" :alt="`page ${i}`" />
            </swiper-slide>
        </swiper>
    </div>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "swiper/css/pagination";
import "swiper/css/navigation";
import "swiper/css/effect-cards";

import "../style.css";

// import required modules
import { Pagination, Navigation, EffectCards } from "swiper";

export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        return {
            modules: [Pagination, Navigation, EffectCards],
        };
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
    gap: 5rem;
    height: min-content;
    align-items: center;
    position: relative;
    overflow: hidden;

    h3 {
        grid-area: title;
    }

    .book_left {
        grid-area: before;
        z-index: 999;
        padding-right: 8px;

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
        // height: fit-content;
        // width: auto;
        // max-height: 100%;
        // max-width: 100%;

        max-width: 50vw;
        // width: 100%;
        // overflow: hidden;
        width: fit-content;

        border-radius: 10px;
        margin: 0;
        cursor: grab;
    }
    .swiper-slide {
        text-align: center;
        font-size: 18px;
        background: #fef9f3;
        max-height: 100%;

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
        max-width: 100%;
        height: auto;
        object-fit: cover;
        border-radius: 5px;
    }
}

@media (max-width: 992px) {
    #book_section {
        display: flex;
        flex-direction: column;
        align-items: center;
        // justify-content: center;
        overflow: hidden;

        h3 {
            text-align: center;
        }

        .swiper {
            max-width: 72vw;

            // padding: 0 10vw;
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

@media (min-width: 1400px) {
    #book_section {
        .swiper {
            max-width: 750px;
        }
    }
}
</style>
