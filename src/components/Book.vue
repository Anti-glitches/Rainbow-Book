<template>
    <div id="book_section">
        <div class="book_left">
            <h3>Read Maryam’s book</h3>
            <blockquote>
                “I’m not a big sister anymore. Now I’m an author.”
            </blockquote>
            <p class="author">Maryam, 4.</p>

            <div class="aside_container">
                <p class="small_title">A bit about the author</p>
                <p>
                    Maryam wrote this book with a bit of help from her dad. A
                    story about a unicorn who overcomes the adversity of its
                    broken horn. Her eye lit up as she saw her imagination come
                    to life.
                </p>
            </div>
        </div>
        <swiper class="mySwiper">
            <swiper-slide v-for="i in 8" :key="i">
                <img :src="`book/page${i}.png`" :alt="`page ${i}`" />
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
    gap: 40px;

    .book_left {
        .author {
            text-align: end;
        }
        .aside_container {
            background: var(--light);
            padding: 2rem;
            border-radius: 25px;

            .small_title {
                font-family: var(--font1);
                font-size: 25px;
                font-weight: 700;
                margin-top: 0;
            }
        }
    }
}

.swiper {
    width: 100%;
    height: 100%;
    border-radius: 15px;
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
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>
