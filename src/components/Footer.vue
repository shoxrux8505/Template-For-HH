<template>
    <footer>
        <ul>
            <li>
                <div class="foot-logo">
                    <h3>Exclusive</h3>
                </div>
            </li>
            <li>
                Subscribe
            </li>
            <li>Get 10% off your first order</li>
            <li>
                <div class="input">
                    <input type="email" placeholder="Enter your email">
                    <span> <ion-icon name="send-outline"></ion-icon></span>
                </div>
            </li>
        </ul>
        <ul>
            <li>
                <h3>Support</h3>
            </li>
            <li>111 Bijoy sarani, Dhaka, <br>
                DH 1515, Bangladesh.
            </li>
            <li>
                <a href="#">exclusive@gmail.com</a>
            </li>
            <li><a href="#">+88015-88888-9999</a></li>
        </ul>
        <ul>
            <li>
                <h3>Account</h3>
            </li>
            <li>My Account</li>
            <li>Login / Register</li>
            <li>Cart</li>
            <li>Wishlist</li>
            <li>Shop</li>
        </ul>
        <ul>
            <li>
                <h3>Quick Link</h3>
            </li>
            <li>Privacy Policy</li>
            <li>Terms Of Use</li>
            <li>FAQ</li>
            <li>Contact</li>
        </ul>
        <ul>
            <li>
                <h3>Download App</h3>
            </li>
            <li><small>Save $3 with App New User Only</small></li>
            <li>
                <img src="./img/adds.png" alt="">
            </li>
            <li>
                <div class="icons">
                    <span><a href="#"><ion-icon name="logo-facebook"></ion-icon></a></span>
                    <span><a href="#"><ion-icon name="logo-twitter"></ion-icon></a></span>
                    <span><a href="#"><ion-icon name="logo-instagram"></ion-icon></a></span>
                    <span><a href="#"><ion-icon name="logo-linkedin"></ion-icon></a></span>
                </div>
            </li>

        </ul>
    </footer>
</template>
<style lang="scss" scoped>
footer {
    width: 100%;
    min-height: 40vh;
    padding: 50px 30px;
    background: #000000;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;

    ul {
        list-style: none;
        display: flex;
        align-items: flex-start;
        justify-content: center;
        flex-direction: column;
        row-gap: 25px;

        li {
            a {
                color: #fff;
            }

            .icons {
                display: flex;
                align-items: center;
                justify-content: center;
                gap: 20px;
            }

            cursor: pointer;
            color: #fff;

            .foot-logo {
                font-size: 30px;
            }

            .input {
                padding: 10px 20px;
                border: 2px solid #fff;
                display: flex;
                align-items: center;
                justify-content: center;
                gap: 10px;

                input {
                    background: transparent;
                    font-size: 18px;
                    border: none;
                    outline: 0;
                    color: #fff;
                }

                span {
                    font-size: 20px;
                }
            }
        }
    }
}
</style>