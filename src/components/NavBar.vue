<template>
  <nav>
    <div class="logo">
      Exclusive
    </div>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Contact</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Sing Up</a></li>
    </ul>
    <div class="add-items">
      <div class="search-item">
        <input type="search" placeholder="What are you looking for?" name="search-ietm" id="search">
        <span><ion-icon name="search-outline"></ion-icon></span>
      </div>
      <div class="btns-box">
        <button class="favorite-btn"><ion-icon name="heart-outline"></ion-icon></button>
        <button class="korzinka-btn"><ion-icon name="cart-outline"></ion-icon></button>
      </div>
    </div>
  </nav>
</template>
<script>

</script>

<style lang="scss" scoped>
nav {
  width: 100%;
  padding: 20px 30px;
  display: flex;
  align-items: center;
  justify-content: space-around;
  border-bottom: 1px solid #ccc;
  .logo{
    font-size: 30px;
    font-weight: 700;

  }
  ul {
    list-style: none;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;

    li {
      a {
        color: #000000;
      }
    }
  }

  .add-items {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;
    .search-item{
      padding: 10px 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: var(--grey-color);
      border-radius: 7px;
      span{
        cursor: pointer;
      }
      input{
        border: none;
        outline: 0;
        background: transparent;
      }
    }
    .btns-box {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 20px;
      button{
        width: 50px;
        height: 50px;
        background: transparent;
        font-size: 20px;
        border: none;
        cursor: pointer;
        transition: 0.5s ease;
        border-radius:7px ;
        &:hover{
          background: var(--grey-color);
        }
      }

    }
  }
}
</style>