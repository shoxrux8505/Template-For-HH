<template>
  <div class="content">
    <div class="content-text">
    <p>Summer Sale For All Swim Suits And Free Express Delivery - OFF 50%!</p>
    <a href="#">ShopNow</a>
   </div>
   <div class="lang-selecor">
    <select name="" id="">
        <option value="Eng">English</option>
        <option value="Rus">Russian</option>
        <option value="Uz">Uzbek</option>
    </select>
   </div>
  </div>
</template>

<style lang="scss" scoped>
    .content{
        padding: 20px 30px;
        background: #000000;
        display: flex;
        align-items: center;
        justify-content: space-around;
        gap: 20px;
        .content-text{
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 20px;

            p{
                color: #fff;
            }
            a{
                color: #fff;
                text-decoration: underline;
            }
        }
    }
</style>