<template>
    <footer id="footer_section">
        <!-- <div class="content">
            <div class="content-body">
                <h4>Join our newsletter</h4>
                <p>
                    Promotions, new products and exclusive offers. Directly to
                    your inbox.
                </p>
            </div>
            <div class="inputText">
                <input type="text" placeholder="Your Email" />
                <button class="main_button">Send</button>
            </div>
        </div> -->
        <div class="footer_bottom">
            <img src="/logo.svg" alt="logo" />
            <div class="footer_links">
                <!-- <a href="#">Terms of Service</a> -->
                <!-- <a href="#">Refund Policy</a> -->
                <p>Copyright © by CommerceOwl Inc.</p>
            </div>
        </div>

        <img
            id="waves-bg"
            class="unselectable"
            src="/waves-bg.png"
            alt="bg image"
        />
    </footer>
</template>
<style lang="scss" scoped>
.content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    column-gap: 100px;

    .content-body {
        h2 {
            font-size: 30px;
        }

        p {
            font-size: 20px;
        }
    }
    .inputText {
        min-width: 370px;
        width: fit-content;
        height: fit-content;
        position: relative;

        input {
            border: none;
            padding: 20px;
            padding-right: 150px;
            background: var(--light);
            border-radius: 15px;
            width: 200px;
        }

        button {
            position: absolute;
            top: 50%;
            right: 5px;
            transform: translate(0, -50%);
        }
    }
}

.footer_bottom {
    margin-top: 50px;
    // margin-bottom: 150px;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;

    img {
        height: min-content;
    }

    .footer_links {
        text-align: right;

        :first-child {
            margin-right: 20px;
        }
    }
}

#waves-bg {
    position: absolute;
    left: 0;
    right: 0;
    z-index: -999;
    margin-top: -28vw; /* This works suprisingly well because it adjust based on viewport */
    width: 100%;
}

@media (max-width: 768px) {
    #footer_section {
        .content {
            display: flex;
            flex-direction: column;
            align-items: flex-start;
        }

        .footer_bottom {
            display: flex;
            flex-direction: column;
            align-items: center;

            img {
                // margin-bottom: 2rem;
                height: 100%;
                width: min-content;
            }

            .footer_links {
                text-align: center;
            }
        }
    }
}
</style>
