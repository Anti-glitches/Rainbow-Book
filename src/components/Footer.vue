<template>
    <footer>
        <div class="content">
            <div class="content-body">
                <h4>Join our newsletter</h4>
                <p>
                    Promotions, new products and exclusive offers. <br />
                    Directly to your inbox.
                </p>
            </div>
            <div class="inputText">
                <input type="text" placeholder="Your Email" />
                <button class="main_button">Send</button>
            </div>
        </div>
        <div class="footer_bottom">
            <img src="/logo.png" alt="logo" />
            <div class="footer_links">
                <a href="#">Terms of Service</a>
                <a href="#">Refund Policy</a>
                <p>Copyright © 2022, Powered by Unicorn Book</p>
            </div>
        </div>
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
            border-radius: 20px;
            width: 200px;
        }

        // .main_button {
        //     background: var(--primary-purple);
        //     border: none;
        //     color: white;
        //     padding: 15px 50px;
        //     border-radius: 15px;
        //     font-weight: 600;
        //     letter-spacing: 2px;
        //     cursor: pointer;
        // }

        button {
            position: absolute;
            top: 50%;
            right: 5px;
            transform: translate(0, -50%);
            // background: var(--primary-purple);
            // border: none;
            // color: white;
            // padding: 15px 50px;
            // border-radius: 15px;
            // font-weight: 600;
            // letter-spacing: 2px;
            // cursor: pointer;
        }
    }
}

.footer_bottom {
    margin-top: 100px;
    display: flex;
    justify-content: space-between;

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
</style>
