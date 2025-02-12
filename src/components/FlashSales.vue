<template>
    <div class="container">
        <div class="FlashSales-content">
            <div class="top-part">
                <div class="todays">
                    <div class="border"></div>
                    <span>Today's</span>
                </div>
            </div>
            <div class="FlashSales-nav">
                <div class="hearder">
                    <h1>Flash Sales</h1>
                </div>
                <div class="time-down">
                    <div class="count">
                        <span>Days</span>
                        <span>{{ formatTime(timeLeft.days) }}</span>
                    </div>
                    <span class="two-dot">:</span>
                    <div class="count">
                        <span>Hours</span>
                        <span>{{ formatTime(timeLeft.hours) }}</span>
                    </div>
                    <span class="two-dot">:</span>
                    <div class="count">
                        <span>Minutes</span>
                        <span>{{ formatTime(timeLeft.minutes) }}</span>
                    </div>
                    <span class="two-dot">:</span>
                    <div class="count">
                        <span>Seconds</span>
                        <span>{{ formatTime(timeLeft.seconds) }}</span>
                    </div>
                </div>
                <div class="btn-carusel">
                    <button><ion-icon name="arrow-back-outline"></ion-icon></button>
                    <button><ion-icon name="arrow-forward-outline"></ion-icon></button>
                </div>
            </div>
            <div class="cards">
                <ProductCard />
                <ProductCard />
                <ProductCard />
                <ProductCard />
                <ProductCard />
            </div>
            <button class="view-all">View All Products</button>
        </div>
    </div>
</template>
<script>
import ProductCard from './product-cards/ProductCard.vue';
export default {
    name: 'FlashSales',
    components: {
        ProductCard
    },
    data() {
        return {
            timeLeft: { days: 3, hours: 23, minutes: 19, seconds: 56 },
            products: [
                { name: "HAVIT HV-G92 Gamepad", price: 120, oldPrice: 160, discount: 40, rating: 88, image: "https://tse3.mm.bing.net/th?id=OIP.PN5kWetxWmRcFvYwnA0pEAHaHa&pid=Api" },
                { name: "AK-900 Wired Keyboard", price: 960, oldPrice: 1160, discount: 35, rating: 75, image: "https://tse1.mm.bing.net/th?id=OIP.Q_60MPM9sK3sZfEJOjk7CQHaH2&pid=Api" },
                { name: "IPS LCD Gaming Monitor", price: 370, oldPrice: 400, discount: 30, rating: 99, image: "https://tse1.mm.bing.net/th?id=OIP.DzoNwWjR5Fyctob0g_ICMQHaGk&pid=Api" },
                { name: "S-Series Comfort Chair", price: 375, oldPrice: 400, discount: 25, rating: 99, image: "https://tse4.mm.bing.net/th?id=OIP.4fQqEL8HvylBX2pjcrW1ygAAAA&pid=Api" }
            ],
            currentIndex: 0,
            productsPerPage: 3
        };
    },
    computed: {
        visibleProducts() {
            return this.products.slice(this.currentIndex, this.currentIndex + this.productsPerPage);
        }
    },
    methods: {
        formatTime(value) {
            return value < 10 ? `0${value}` : value;
        },
        nextSlide() {
            if (this.currentIndex + this.productsPerPage < this.products.length) {
                this.currentIndex++;
            }
        },
        prevSlide() {
            if (this.currentIndex > 0) {
                this.currentIndex--;
            }
        },
        countdown() {
            setInterval(() => {
                if (this.timeLeft.seconds > 0) {
                    this.timeLeft.seconds--;
                } else {
                    this.timeLeft.seconds = 59;
                    if (this.timeLeft.minutes > 0) {
                        this.timeLeft.minutes--;
                    } else {
                        this.timeLeft.minutes = 59;
                        if (this.timeLeft.hours > 0) {
                            this.timeLeft.hours--;
                        } else {
                            this.timeLeft.hours = 23;
                            if (this.timeLeft.days > 0) {
                                this.timeLeft.days--;
                            }
                        }
                    }
                }
            }, 1000);
        }
    },
    mounted() {
        this.countdown();
    }
};

</script>
<style lang="scss" scoped>
.container {
    width: 100%;
    margin: 0 auto;
    padding: 20px;
    border-bottom: 1px solid var(--grey-color);

    .cards {
        // margin-left: 20px;  
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 20px;
    }

    .FlashSales-content {
        width: 100%;
        padding: 35px 30px;
        display: flex;
        align-items: flex-start;
        justify-content: center;
        flex-direction: column;
        row-gap: 5px;
        .view-all{
            padding: 15px 40px;
            border-radius: 7px;
            background: var(--red-color);
            color: #fff;
            border: none;
            text-align: center;
            position: relative;
            left: 700px;
            top: 20px;
            cursor: pointer;
        }
        .top-part {
            .todays {
                display: flex;
                align-items: center;
                justify-content: center;
                gap: 20px;
                padding: 5px 7px;
                color: var(--red-color);

                .border {
                    width: 30px;
                    height: 60px;
                    background: var(--red-color);
                    border-radius: 7px;
                }

                span {
                    font-size: 20px;
                    font-weight: 700;
                }
            }
        }

        .FlashSales-nav {
            width: 100%;
            padding: 20px 30px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 20px;

            .time-down {
                display: flex;
                align-items: center;
                justify-content: center;
                gap: 20px;

                .two-dot {
                    font-size: 20px;
                    color: var(--two-dot);
                }

                .count {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    flex-direction: column;
                    row-gap: 5px;

                    span {

                        &:nth-child(2) {
                            font-size: 25px;
                            font-weight: 700;
                        }
                    }
                }
            }

            .btn-carusel {
                display: flex;
                align-items: center;
                justify-content: center;
                gap: 20px;

                button {
                    width: 40px;
                    height: 40px;
                    background: var(--grey-color);
                    border: none;
                    border-radius: 50%;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    font-size: 20px;
                    transition: 0.5s ease;
                    cursor: pointer;

                    &:hover {
                        border: 1px solid var(--red-color);
                    }
                }
            }
        }

    }
}
</style>