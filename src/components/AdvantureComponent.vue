<template>
    <div class="container">
        <div class="cards">
            <div class="skils">
                <div class="icon-box">
                    <span><ion-icon name="car-outline"></ion-icon></span>
                </div>
                <div class="text-box">
                    <h4>FREE AND FAST DELIVERY</h4>
                    <p>Free delivery for all orders over $140</p>
                </div>
            </div>
            <div class="skils">
               <div class="icon-box">
                <span><ion-icon name="headset-outline"></ion-icon></span>
               </div>
                <div class="text-box">
                    <h4>24/7 CUSTOMER SERVICE</h4>
                    <p>Friendly 24/7 customer support</p>
                </div>
            </div>
            <div class="skils">
               <div class="icon-box">
                <div class="icon-box">
                    <span><ion-icon name="shield-checkmark-outline"></ion-icon></span>
                </div>
               </div>
                <div class="text-box">
                    <h4>MONEY BACK GUARANTEE</h4>
                    <p>We reurn money within 30 days</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AdvantureComponent',
    components: {
        // 
    }
}
</script>
<style lang="scss" scoped>
.container {
    width: 100%;
    padding: 20px;
    display: flex;
    align-items: center;
    justify-content: center;

    .cards{
        width: 80%;
        display: flex;
        align-items: center;
        justify-content: space-around;
        gap: 20px;

        .skils{
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            row-gap: 20px;
            text-align: center;
            .icon-box{
                width: 100px;
                height: 100px;
                display: flex;
                align-items: center;
                justify-content: center;
                background: var(--grey-color);
                font-size: 45px;
                border-radius: 50%;
                span{
                    width: 80px;
                    height: 80px;
                    border-radius: 50%;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    background: #000000;
                    color: #ffff;
                }
            }
            .text-box{
                display: flex;
                align-items: center;
                justify-content: center;
                flex-direction: column;
                h4{
                    font-size: 20px;
                }
                p{
                    display: inline-block;
                    font-size: 18px;
                }
            }
        }
    }

}
</style>