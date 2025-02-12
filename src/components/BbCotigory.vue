<template>
    <div class="container">
        <div class="FlashSales-content">
            <div class="top-part">
                <div class="todays">
                    <div class="border"></div>
                    <span>Categories</span>
                </div>
            </div>
            <div class="FlashSales-nav">
                <div class="hearder">
                    <h1>Browse By Category</h1>
                </div>
                <div class="btn-carusel">
                    <button><ion-icon name="arrow-back-outline"></ion-icon></button>
                    <button><ion-icon name="arrow-forward-outline"></ion-icon></button>
                </div>
            </div>
            <div class="cotigory-type">
                <div class="type">
                    <span><ion-icon name="phone-portrait-outline"></ion-icon></span>
                    <span>Phones</span>
                </div>
                <div class="type">
                    <span><ion-icon name="tv-outline"></ion-icon></span>
                    <span>Computers</span>
                </div>
                <div class="type">
                    <span><ion-icon name="tv-outline"></ion-icon> </span>
                    <span>SmartWatch</span>
                </div>
                <div class="type">
                    <span><ion-icon name="camera-outline"></ion-icon> </span>
                    <span>Camera</span>
                </div>
                <div class="type">
                    <span><ion-icon name="headset-outline"></ion-icon></span>
                    <span>HeadPhone</span>
                </div>
                <div class="type">
                    <span><ion-icon name="game-controller-outline"></ion-icon></span>
                    <span>Gaming</span>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
.container {
    width: 100%;
    margin: 0 auto;
    padding: 20px;
    border-bottom: 1px solid var(--grey-color);

    .cards {
        margin-left: 20px;
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

        .cotigory-type{
            width: 100%;
            display: flex;
            padding: 20px 20px;
            align-items: center;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;

            .type{
                width: 170px;
                height: 145px;
                display: flex;
                align-items: center;
                justify-content: center;
                flex-direction: column;
                row-gap: 5px;
                cursor: pointer;
                border: 1px solid var(--grey-color);
                transition: 0.5s ease;
                span{
                    font-size: 18px;
                    font-weight: 700;
                    &:nth-child(1){
                        font-size: 35px;
                    }
                }
                &:hover{
                    background: var(--red-color);
                    color: #fff;
                }
                
            }
        }


        .view-all {
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