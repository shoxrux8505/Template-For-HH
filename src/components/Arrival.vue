<template>
    <div class="container">
        <div class="FlashSales-content">
            <div class="top-part">
                <div class="todays">
                    <div class="border"></div>
                    <span>Featured</span>
                </div>
            </div>
            <div class="FlashSales-nav">
                <div class="hearder">
                    <h1>New Arrival</h1>
                </div>

                <div class="btn-carusel">
                    <div></div>
                </div>
            </div>
            <div class="grid-container">
                <div class="card large">
                    <img src="./img/large.png" alt="PlayStation 5" />
                    <div class="overlay">
                        <h3>PlayStation 5</h3>
                        <p>Black and White version of the PS5 coming out on sale.</p>
                        <a href="#">Shop Now</a>
                    </div>
                </div>
                <div class="card">
                    <img src="./img/woman.png" alt="Women's Collections" />
                    <div class="overlay">
                        <h3>Women's Collections</h3>
                        <p>Featured woman collections that give you another vibe.</p>
                        <a href="#">Shop Now</a>
                    </div>
                </div>
               <div class="cards">
                <div class="card" >
                    <img style="width: 270px; height: 284px;" src="./img/Frame.png" alt="Speakers" />
                    <div class="overlay">
                        <h3>Speakers</h3>
                        <p>Amazon wireless speakers.</p>
                        <a href="#">Shop Now</a>
                    </div>
                </div>
                <div class="card" >
                    <img style="width: 270px; height: 284px;" src="./img/parfume.png" alt="Perfume" />
                    <div class="overlay">
                        <h3>Perfume</h3>
                        <p>GUCCI INTENSE OUD EDP</p>
                        <a href="#">Shop Now</a>
                    </div>
                </div>
               </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Arrival',
    components: {}
}
</script>
<style lang="scss" scoped>
.container {
    width: 100%;
    margin: 0 auto;
    padding: 20px;
    border-bottom: 1px solid var(--grey-color);

    .FlashSales-content {
        width: 100%;
        padding: 35px 30px;
        display: flex;
        align-items: flex-start;
        justify-content: center;
        flex-direction: column;
        row-gap: 5px;

        .grid-container {
            width: 100%;
            display: grid;
            grid-template-columns: 2fr 1fr;
            grid-template-rows: auto auto;
            gap: 16px;
            max-width: 900px;
            margin: auto;
            .cards{
                display: flex;
                align-items: center;
                justify-content: center;
                gap: 20px;
            }
            .card {
                position: relative;
                border-radius: 10px;
                overflow: hidden;
                cursor: pointer;
                background: #000000;
                
                img {
                    width: 100%;
                    height: auto;
                    display: block;
                }

                .overlay {
                    position: relative;
                    bottom: 10px;
                    left: 10px;
                    color: white;
                    display: flex;
                    align-items: flex-start;
                    justify-content: center;
                    flex-direction: column;
                    row-gap: 10px;
                    // background: rgba(0, 0, 0, 0.6);
                    padding: 10px;
                    border-radius: 5px;
                    a{
                        color: #fff;
                        text-decoration: underline;
                    }
                }
            }

            .large {
                grid-row: span 2;
            }
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



            .btn-carusel {
                display: flex;
                align-items: center;
                justify-content: center;
                gap: 20px;


            }
        }

    }
}
</style>