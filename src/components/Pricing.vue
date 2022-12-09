<template>
    <div class="cards_container">
        <div class="card why_info">
            <h4>Create memorable moments</h4>
            <p>
                Bond with your child and explore their limitless imagination,
                becoming the author of their own fiction.
            </p>
            <p>
                Watch them create stories with generated illustrations to see
                their creativity come to life. With your help, your child could
                be an author too.
            </p>
            <img src="/child-reading.png" alt="a child reading" />
        </div>
        <div class="card card_pricing pricing_digital">
            <div class="pricing_title">
                <h4>Digital</h4>
                <span class="price">$29.99</span>
            </div>
            <p>
                Lorem ipsum dolor sit amet consectetur. Amet tincidunt convallis
                pretium nulla in.
            </p>

            <p class="small_title">What you'll get:</p>
            <ul>
                <li>Lorem ipsum dolor sit amet consectetur.</li>
                <li>Lorem ipsum dolor sit amet consectetur.</li>
                <li>Lorem ipsum dolor sit amet consectetur.</li>
                <li>Lorem ipsum dolor sit amet consectetur.</li>
            </ul>

            <div class="pricing_footer">
                <a href="#">View detail example</a>
                <button class="main_button">Let's start</button>
            </div>
        </div>
        <div class="card card_pricing pricing_physical">
            <div class="pricing_title">
                <h4>Physical</h4>
                <span class="price">$99.99</span>
            </div>
            <p>
                Lorem ipsum dolor sit amet consectetur. Amet tincidunt convallis
                pretium nulla in.
            </p>

            <p class="small_title">What you'll get:</p>
            <ul>
                <li>Lorem ipsum dolor sit amet consectetur.</li>
                <li>Lorem ipsum dolor sit amet consectetur.</li>
                <li>Lorem ipsum dolor sit amet consectetur.</li>
                <li>Lorem ipsum dolor sit amet consectetur.</li>
            </ul>

            <div class="pricing_footer">
                <a href="#">View detail example</a>
                <button class="main_button">Let's start</button>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.cards_container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    column-gap: 40px;

    .card {
        border-radius: 25px;
        background: aliceblue;
        padding: 3rem 2.5rem;
        font-size: 19px;
        font-weight: 500;
        max-width: 400px;
    }

    .card_pricing {
        height: fit-content;

        .pricing_title {
            display: flex;
            justify-content: space-between;
            align-items: center;
            .price {
                font-size: 25px;
            }
        }

        .small_title {
            margin-top: 40px;
            font-size: 20px;
            font-weight: 800;
        }

        ul {
            li {
                font-family: var(--font2);
                font-size: 18px;
            }
        }

        .pricing_footer {
            margin-top: 60px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            gap: 10px;
            a {
                font-size: 14px;
            }

            button {
                font-size: 20px;
            }
        }
    }

    .pricing_physical {
        background: var(--primary-purple);
        color: white;

        a {
            color: white;
        }

        button {
            background: var(--light);
            color: black;
        }
    }

    .pricing_digital {
        background: var(--light);
    }

    .why_info {
        background: var(--secondary-purple);
        color: white;
        display: flex;
        flex-direction: column;

        img {
            margin-top: 3rem;
            align-self: center;
        }
    }
}

@media (max-width: 1200px) {
    .cards_container {
        grid-template-areas:
            "info info"
            "digital physical";
        grid-template-columns: 1fr 1fr;
        column-gap: 2rem;
        row-gap: 2rem;

        .card {
            max-width: none;
        }

        .why_info {
            grid-area: info;
        }

        .pricing_digital {
            grid-area: digital;
        }

        .pricing_physical {
            grid-area: physical;
        }
    }
}

@media (max-width: 768px) {
    .cards_container {
        display: flex;
        flex-direction: column;
        row-gap: 2rem;

        .card {
            max-width: 100%;
        }
    }
}
</style>