<template>
	<main>
		<!-- HERO SECTION -->
	<section id="hero" class="d-flex align-items-center text-center">
	  <div class="container text-white">
	    <h1 class="fw-bold">Shop the Latest Trends</h1>
	    <p class="lead">Discover new arrivals and top-selling products</p>
	    <button class="btn btn-primary btn-lg mt-3">Shop Now</button>
	  </div>
	</section>

	<!-- CAROUSEL -->
	<div id="bannerCarousel" class="carousel slide mt-5 container" data-bs-ride="carousel">
	  <div class="carousel-inner rounded">
	    <div class="carousel-item active">
	      <img
	        src="https://images.unsplash.com/photo-1512436991641-6745cdb1723f?q=80&w=1200"
	        class="d-block w-100"
	        alt="banner"
	      />
	    </div>
	    <div class="carousel-item">
	      <img
	        src="https://images.unsplash.com/photo-1472851294608-062f824d29cc?q=80&w=1200"
	        class="d-block w-100"
	        alt="banner"
	      />
	    </div>
	    <div class="carousel-item">
	      <img
	        src="https://images.unsplash.com/photo-1503341455253-b2e723bb3dbb?q=80&w=1200"
	        class="d-block w-100"
	        alt="banner"
	      />
	    </div>
	  </div>

	  <button
	    class="carousel-control-prev"
	    type="button"
	    data-bs-target="#bannerCarousel"
	    data-bs-slide="prev"
	  >
	    <span class="carousel-control-prev-icon"></span>
	  </button>

	  <button
	    class="carousel-control-next"
	    type="button"
	    data-bs-target="#bannerCarousel"
	    data-bs-slide="next"
	  >
	    <span class="carousel-control-next-icon"></span>
	  </button>
	</div>

	<!-- HEADING -->
	<div class="container text-center mt-5" id="products">
	  <h2 class="fw-bold text-light">Featured Products</h2>
	  <p>Top items picked just for you</p>
	</div>

	<!-- PRODUCT CARDS -->
	<div class="container mt-4">
	  <div class="row g-4">
	    <div v-for="(product, index) in products" :key="index" class="col-md-3">
	      <div class="card product-card shadow-sm">
	        <img :src="product.img" class="card-img-top" alt="product" />
	        <div class="card-body">
	          <h5 class="card-title">{{ product.title }}</h5>
	          <p class="card-text">₱{{ product.price.toLocaleString('en-PH', {minimumFractionDigits: 2}) }}</p>
	          <button class="btn btn-primary w-100">Buy Now</button>
	        </div>
	      </div>
	    </div>
	  </div>
	</div>
	</main>
	
</template>

<script setup>
	import products from '../data/products.json'
</script>

<style scoped>
	
	#hero {
	  background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
	    url("https://images.unsplash.com/photo-1523275335684-37898b6baf30?q=80&w=1200")
	      center/cover no-repeat;
	  height: 70vh;
	}

	.product-card img {
	  height: 200px;
	  object-fit: cover;
	}
	main {
		background-color: black;
	}

</style>