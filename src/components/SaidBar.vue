<template>
    <div class="sidebar">
      <ul>
        <li v-for="(category, index) in categories" :key="index">
          {{ category }}
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        categories: [
          "Woman's Fashion",
          "Men's Fashion",
          "Electronics",
          "Home & Lifestyle",
          "Medicine",
          "Sports & Outdoor",
          "Baby's & Toys",
          "Groceries & Pets",
          "Health & Beauty"
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  .sidebar {
    width: 30%;
    padding: 10px;
    border-right: 1px solid #ddd;
  }
  ul {
    list-style: none;
    padding: 0;
  }
  li {
    padding: 10px;
    cursor: pointer;
  }
  li:hover {
    background: #f5f5f5;
  }
  </style>
  