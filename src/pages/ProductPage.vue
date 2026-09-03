<!-- <script setup>
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
  <main>
    <h1>Produk Kami</h1>
    <div class="grid">
      <ProductCard
        v-for="produk in daftarProduk"
        :key="produk.id"
        :nama="produk.nama"
        :harga="produk.harga"
        :gambar="produk.gambar"
        :imgStyle="produk.imgStyle"
      />
    </div>
  </main>
</template>

<style scoped>
.grid {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
}

.image {
  height: 150px;
  width: 250px;
}
</style> -->

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
  <div class="product-page">
    <!-- Banner Produk Kami -->
    <section class="banner">
      <h1>Produk Kami</h1>
      <p>Temukan koleksi mobil pilihan terbaik dari Barss_Shop</p>
    </section>

    <main>
      <div class="grid">
        <div class="grid-item" v-for="produk in daftarProduk" :key="produk.id">
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
/* Warna banner disamakan dengan About Page */
.banner {
  background: linear-gradient(135deg, rgba(0, 0, 0, 0.137)40%, #9c3aed49)60%, rgb(44, 20, 20)100%;
  color: #ffffff;
  text-align: center;
  padding: 60px 20px;
}

.banner h1 {
  margin: 0 0 8px;
  font-size: 2.2rem;
}

.banner p {
  margin: 0;
  font-size: 1rem;
  opacity: 0.9;
}

main {
  padding: 40px 20px;
  max-width: 1100px;
  margin: 0 auto;
}

.grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 16px;
}

.grid-item {
  flex: 0 0 calc((100% - 32px) / 3);
  display: flex;
  justify-content: center;
}

.image {
  height: 150px;
  width: 250px;
}

/* Responsif: kurangi jumlah kolom di layar sempit */
@media (max-width: 700px) {
  .grid-item {
    flex-basis: calc((100% - 16px) / 2);
  }
}

@media (max-width: 480px) {
  .grid-item {
    flex-basis: 100%;
  }
}
</style>