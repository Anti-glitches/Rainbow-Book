<template>
    <div id="book_section">
        <div class="book_left">
            <!-- <h3>Read Maryam’s book</h3> -->

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
        <swiper class="mySwiper">
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
    gap: 2rem;

    .book_left {
        .aside_container {
            background: var(--light);
            padding: 2rem;
            border-radius: 15px;
            width: auto;

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

                img {
                    width: 100px;
                    height: 100%;
                    justify-self: end;
                }
            }
        }
    }
}

@media (max-width: 768px) {
    #book_section {
        display: flex;
        flex-direction: column;

        .book_left {
            .aside_container {
                .footer {
                    img {
                        transform: rotate(90deg);
                    }
                }
            }
        }
    }
}

.swiper {
    // width: 100%;
    // height: 100%;
    width: auto;
    border-radius: 15px;
    margin: 0;
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
    height: 100%;
    object-fit: cover;
}
</style>
