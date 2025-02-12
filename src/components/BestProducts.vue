<template>
    <div class="container">
        <div class="FlashSales-content">
            <div class="top-part">
                <div class="todays">
                    <div class="border"></div>
                    <span>This Month</span>
                </div>
            </div>
            <div class="FlashSales-nav">
                <div class="hearder">
                    <h1>Best Selling Products</h1>
                </div>
                <div class="btn-carusel">
                    <button class="view-all">View All</button>
                </div>
            </div>
           <div class="cards">
            <ProductCard />
            <ProductCard />
            <ProductCard />
            <ProductCard />
            <ProductCard />
           </div>
        </div>
    </div>
</template>
<script>
import ProductCard from './product-cards/ProductCard.vue';
export default {
    name: 'BestProduct',
    components: {
        ProductCard 
    }
}
</script>
<style lang="scss" scoped>
.container {
    width: 100%;
    margin: 0 auto;
    padding: 20px;
    border-bottom: 2px solid var(--grey-color);

    .cards {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 20px;
    }

    .FlashSales-content {
        width: 90%;
        // padding: 35px 30px;
        display: flex;
        align-items: flex-start;
        justify-content: center;
        flex-direction: column;
        row-gap: 5px;

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
            // width: 80%;
            width: 70%;
            padding: 10px 30px;
            display: flex;
            align-items: center;
            justify-content: space-around;
            gap: 20px;



            .btn-carusel {
                display: flex;
                align-items: center;
                justify-content: center;
                gap: 20px;

                .view-all {
                    position: relative;
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

            }
        }

    }
}
</style>