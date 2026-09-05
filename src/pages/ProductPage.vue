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
    <section class="bg-gradient-to-br from-black/[0.137] from-[40%] via-[#9c3aed]/[0.286] via-[60%] to-[#2c1414] to-100% text-white text-center px-5 py-[60px]">
      <h1 class="m-0 mb-2 text-[2.2rem]">Produk Kami</h1>
      <p class="m-0 text-base opacity-90">Temukan koleksi mobil pilihan terbaik dari Barss_Shop</p>
    </section>

    <main class="px-5 py-10 max-w-[1100px] mx-auto">
      <div class="flex flex-wrap justify-center gap-4">
        <div
          class="flex justify-center basis-[calc((100%-32px)/3)] grow-0 shrink-0 max-[700px]:basis-[calc((100%-16px)/2)] max-[480px]:basis-full"
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