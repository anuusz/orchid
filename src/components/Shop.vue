<template>
  <div class="product-cards">
    <div v-for="(product, index) in products" :key="index" class="product-card">
      <img :src="product.image" :alt="product.name" class="product-image">
      <div class="product-details">
        <div class="product-name">{{ product.name }}</div>
        <div class="product-price">{{ product.price }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        { name: "Semangka", image: "../assets/semangka", price: "$10" },
        { name: "Product 2", image: "path/to/image2.jpg", price: "$15" },
        { name: "Product 3", image: "path/to/image3.jpg", price: "$20" },
        { name: "Product 4", image: "path/to/image4.jpg", price: "$25" },
        { name: "Product 5", image: "path/to/image5.jpg", price: "$30" }
      ]
    };
  }
};
</script>

<style scoped>
.product-cards {
  display: flex;
  flex-wrap: wrap;
  padding-top: 6.25rem;
}

.product-card {
  border: 1px solid #ccc;
  border-radius: 8px;
  padding: 20px;
  margin: 10px;
  width: 200px;
}

.product-image {
  width: 100%;
  border-radius: 8px;
}

.product-details {
  margin-top: 10px;
}

.product-name {
  font-weight: bold;
}

.product-price {
  color: darkgreen;
}
</style>
