<template>
    <div class="conatiner">
        <div class="jbl-contant">
            <div class="text-box">
                <p>Categories</p>
                <h1>Enhance Your <br> Music Experience</h1>
                <div class="time-down">
                    <div class="count">
                        <span>{{ formatTime(timeLeft.days) }}</span>
                        <span>Days</span>
                    </div>
                    <span class="two-dot">:</span>
                    <div class="count">
                        <span>{{ formatTime(timeLeft.hours) }}</span>
                        <span>Hours</span>
                    </div>
                    <span class="two-dot">:</span>
                    <div class="count">
                        <span>{{ formatTime(timeLeft.minutes) }}</span>
                        <span>Minutes</span>
                    </div>
                    <span class="two-dot">:</span>
                    <div class="count">
                        <span>{{ formatTime(timeLeft.seconds) }}</span>
                        <span>Seconds</span>
                    </div>
                </div>
                <button class="btn">Buy Now!</button>
            </div>
            <div class="img-box">
                <img src="./img/jbl.png" alt="">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'JblContent',
    components: {
        // 
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
.conatiner {
    width: 100%;
    padding: 10px 20px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 10px;

    .jbl-contant {
        width: 80%;
        height: 60vh;
        padding: 20px 30px;
        background: #000000;
        display: flex;
        align-items: center;
        justify-content: space-around;
        .text-box{
            display: flex;
            align-items: flex-start;
            justify-content: center;
            flex-direction: column;
            row-gap: 20px;
            color: #fff;
            row-gap: 10px;
            h1{
                font-size: 60px;
            }
            p{
                color: var(--green-color);
            }
            .time-down{
                display: flex;
                align-items: center;
                justify-content: center;
                gap: 10px;
                .count{
                    padding: 7px 8px;
                    width: 64px;
                    height: 64px;
                    background: #fff;
                    border-radius: 50%;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    flex-direction: column;
                    row-gap: 5px;
                    color: #000;
                }
            }

           .btn{
            padding: 20px 40px;
            border: none;
            margin-top: 10px;
            background: var(--green-color);
            color:#fff;
            border-radius: 7px ;
            font-size: 20px;
            cursor: pointer;
           }

        }
        .img-box{
            filter: drop-shadow(0 0 10px var(--grey-color))
        }
    }
}
</style>


