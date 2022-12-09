<script setup>
import Navbar from "../components/Navbar.vue";
</script>

<template>
    <div id="hero_section">
        <navbar />
        <div class="hero">
            <div class="hero_left">
                <h1>“I’m not a big sister anymore. Now I’m an author.”</h1>
                <p class="subhead">
                    Discover your child's boundless creativity and create a book
                    with them.
                </p>
                <button class="main_button">Create your book</button>
            </div>

            <img src="/hero-img.png" alt="hero image" />
        </div>
    </div>
</template>


<style lang="scss" scoped>
#hero_section {
    .hero {
        display: grid;
        grid-template-columns: 1fr 1fr;
        align-items: center;
        justify-items: end;
        margin-top: 2rem;

        .hero_left {
            .subhead {
                font-size: 1.5rem;
            }
        }
    }
}

@media (max-width: 1200px) {
    #hero_section {
        .hero {
            .hero_left {
                h1 {
                    font-size: 3.5rem;
                }

                button {
                    margin-top: 1.5rem;
                }
            }

            img {
                width: 50vw;
            }
        }
    }
}

@media (max-width: 768px) {
    #hero_section {
        .hero {
            display: flex;
            flex-direction: column;

            .hero_left {
                order: 2;
                display: flex;
                flex-direction: column;
                margin-top: 2rem;

                h1 {
                    font-size: 3rem;
                }

                button {
                    align-self: center;
                    margin-top: 1.5rem;
                }
            }

            img {
                order: 1;
                width: 100%;
            }
        }
    }
}

@media (max-width: 576px) {
    #hero_section {
        .hero {
            .hero_left {
                h1 {
                    font-size: 2.8rem;
                }

                p.subhead {
                    font-size: 1.3rem;
                }

                button {
                    width: 100%;
                }
            }

            img {
                width: 90vw;
            }
        }
    }
}
</style>