
<script setup>
import ProductCard from '../components/ProductCard.vue'
// import tasSekolah from '../assets/tas-sekolah.jpg'

const daftarProduk = [
  { id: 1, nama: 'BMW-e36', harga: 1300, gambar:
  'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQgfQeRzIggKxrEJmKbgw8lyiHb9jlCsOyVfUxqD3wHUw&s=10',
  imgStyle: { width: '100%', height: '260px', objectFit: 'cover' } },
  { id: 2, nama: 'BMW-e46', harga: 1250, gambar:
  'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQNCXEO-RxvaXFXzNKvhP0elJd39A5Jc9NuNFOz1YN4lQ&s=10',
  imgStyle: { width: '100%', height: '260px', objectFit: 'cover' } },
  { id: 3, nama: 'BMW-m4', harga: 1000, gambar: 
  'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSludwxe_o3kwxKtL4lQuE1CvbuLvYFGqvrzHBjoZbD0g&s=10',
  imgStyle: { width: '100%', height: '260px', objectFit: 'cover' } },
  { id: 4, nama: 'Mercedes Benz AMG GT 2018', harga: 1200, gambar: 
  'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQeftygFBmc5hG2YUBmE8jQ8haFBZYRFsYgir2fO5BnDQ&s=10',
  imgStyle: { width: '100%', height: '260px', objectFit: 'cover' } },
  { id: 5, nama: 'Mercedes-AMG GT 2020', harga: 1550, gambar: 
  ' https://cdn.antaranews.com/cache/1200x800/2020/07/30/mercedes-amg-gt-2020-2.jpg',
  imgStyle: { width: '100%', height: '260px', objectFit: 'cover' } },
  { id: 6, nama: 'Mercedes ', harga: 2250, gambar: 
  ' https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTN6YNvq1ohzHiPtEQ7Fx-2adLszdFEm3yd96uDzB6cog&s=10',
  imgStyle: { width: '100%', height: '260px', objectFit: 'cover' } }
]
</script>

<template>
  <div>
    <!-- Banner Produk Kami -->
    <section class="banner">
      <h1 class="banner-title">Produk Kami</h1>
      <p class="banner-desc">Temukan koleksi mobil pilihan terbaik dari Barss_Shop</p>
    </section>

    <main class="product-main">
      <div class="product-grid">
        <div
          class="product-item"
          v-for="produk in daftarProduk"
          :key="produk.id"
        >
          <ProductCard
            :nama="produk.nama"
            :harga="produk.harga"
            :gambar="produk.gambar"
            :imgStyle="produk.imgStyle"
          />
        </div>
      </div>
    </main>
  </div>
</template>

<style scoped>
.banner {
  background: linear-gradient(
    to bottom right,
    rgba(0, 0, 0, 0.137) 40%,
    rgba(156, 58, 237, 0.286) 60%,
    #2c1414 100%
  );
  color: #fff;
  text-align: center;
  padding: 60px 20px;
}

.banner-title {
  margin: 0 0 8px;
  font-size: 2.2rem;
}

.banner-desc {
  margin: 0;
  font-size: 1rem;
  opacity: 0.9;
}

.product-main {
  padding: 40px 20px;
  max-width: 1100px;
  margin: 0 auto;
}

.product-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 16px;
}

.product-item {
  display: flex;
  justify-content: center;
  width: 100%;
  max-width: 380px;
  flex-basis: calc((100% - 32px) / 3);
  flex-grow: 0;
  flex-shrink: 0;
}

@media (max-width: 700px) {
  .product-item {
    flex-basis: calc((100% - 16px) / 2);
  }
}

@media (max-width: 480px) {
  .product-item {
    flex-basis: 100%;
  }
}
</style>