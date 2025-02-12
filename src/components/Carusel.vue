<template>
    <div class="carousel">
      <div class="slide" v-for="(slide, index) in slides" :key="index" v-show="currentSlide === index">
        <img :src="slide.image" alt="Slide Image">
        <div class="content">
          <h2>{{ slide.title }}</h2>
          <p>{{ slide.subtitle }}</p>
          <button>Shop Now →</button>
        </div>
      </div>
      <div class="dots">
        <span v-for="(slide, index) in slides" :key="index" @click="currentSlide = index"
              :class="{ active: currentSlide === index }"></span>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        currentSlide: 0,
        slides: [
        {
          title: "iPhone 14 Series",
          subtitle: "Up to 10% off Voucher",
          image: "https://picsum.photos/800/300?random=1"
        },
        {
          title: "Samsung Galaxy S23",
          subtitle: "Limited Time Offer",
          image: "https://picsum.photos/800/300?random=2"
        },
        {
          title: "Best Laptops",
          subtitle: "Discounts on Top Brands",
          image: "https://picsum.photos/800/300?random=3"
        }
      ]
      };
    },
    mounted() {
      setInterval(() => {
        this.currentSlide = (this.currentSlide + 1) % this.slides.length;
      }, 5000);
    }
  };
  </script>
  
  <style scoped>
  .carousel {
    position: relative;
    width: 70%;
  }
  .slide {
    position: relative;
  }
  img {
    width: 100%;
  }
  .content {
    position: absolute;
    bottom: 20px;
    left: 20px;
    color: white;
  }
  button {
    background: white;
    padding: 10px;
    border: none;
    cursor: pointer;
  }
  .dots {
    display: flex;
    justify-content: center;
    margin-top: 10px;
  }
  .dots span {
    width: 10px;
    height: 10px;
    margin: 5px;
    background: gray;
    border-radius: 50%;
    cursor: pointer;
  }
  .dots .active {
    background: black;
  }
  </style>
  