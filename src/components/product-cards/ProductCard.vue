<template>
    <div class="product-card">
        <div class="product-item" style="
        display: flex;
        align-items: center;
        justify-content: center;
        ">
            <span class="discount-badge">-40%</span>
            <div class="wish" style="
            position: relative;
            left:100px;
            top: 100px;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            row-gap: 20px;
            cursor: pointer;
            ">
                <span><ion-icon name="heart-outline"></ion-icon></span>
                <span><ion-icon name="eye-outline"></ion-icon></span>
            </div>
        </div>
        <img src="./img/game.png" alt="HAVIT HV-G92 Gamepad" class="product-image">
        <h3 class="product-title">HAVIT HV-G92 Gamepad</h3>
        <div class="price">
            <span>$120</span>
            <span class="old-price">$160</span>
        </div>
        <div class="rating">
            <span class="star">★</span>
            <span class="star">★</span>
            <span class="star">★</span>
            <span class="star">★</span>
            <span class="star">☆</span>
            (88)
        </div>
        <div class="add-to-cart">Add To Cart</div>
    </div>

</template>
<script>
import '../product-cards/productCard.css'
export default {
    name: 'ProductCard',
    components: {
        // 
    }

}
</script>
<style lang="scss" scoped>
.wish {
    span {
        padding: 5px 7px;
        font-size: 25px;
        background: #fff;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
    }
}
</style>