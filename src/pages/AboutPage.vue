<script setup>
import TeamCard from '../components/TeamCard.vue'

// Data anggota tim -> dipakai oleh v-for di bawah
// Boleh diganti dengan nama asli anggota kelompok kalian
const daftarTim = [
  {
    id: 1,
    nama: 'Muhamad akbar',
    jabatan: 'Pendiri & Owner',
    foto: ''
  },
  {
    id: 2,
    nama: 'Wahdan Jay',
    jabatan: 'Manajer Operasional',
    foto: ''
  },
  {
    id: 3,
    nama: 'Kay',
    jabatan: 'Kurator Produk',
    foto: ''
  }
]
</script>

<template>
  <div class="[font-family:'Poppins',sans-serif] text-[#333333]">
    <!-- Banner Tentang Kami -->
    <section class="bg-gradient-to-br from-black/[0.137] from-[40%] via-[#9c3aed]/[0.286] via-[60%] to-[#2c1414] to-100% text-white text-center px-5 py-[60px]">
      <h1 class="m-0 mb-2 text-[2.2rem]">Short story ℬ𝒶𝓇𝓈𝓈_𝒮𝒽ℴ𝓅 </h1>
      <p class="m-0 text-base opacity-90">Kenali lebih dekat cerita dan orang-orang di balik toko </p>
    </section>

    <!-- Bagian Cerita Kami: 2 kolom (teks & gambar) -->
    <section class="flex max-[700px]:flex-col items-center gap-10 px-10 py-[60px] max-w-[1100px] mx-auto text-white">
      <div class="flex-1">
        <h2 class="mt-0 text-[#782688]">About we</h2>
        <p class="leading-[1.7]">
         Pada tahun 2017 saya merintis toko saya karna saya sedang krisis ekonomi jadi saya mulai belajar untuk membangun usaha kecil-kecilan karna untuk membantu ekonomi keluarga saya, saya merintis dari awal jualan mobil bekas yang suda tua dan sampai sekarang sudah makin maju karna saya terus berjuang untuk membersarkan toko ini dan sekarang sudah memeilik beberapa cabang
         <br>
        
         <br>
            Dan sekarang saya memiliki karyawan yang telah menemani usaha saya dari saat sasya merintis sampai sekarang dan kami dari dulu sampai
          Hari ini, kami tetap berpegang pada nilai yang sama sejak awal:
          jujur soal produk, ramah ke pelanggan, dan selalu berusaha
          menghadirkan pilihan terbaik untuk kalian. <br>
        </p>
      </div>

      <div class="flex-1">
        <img
          src="https://img.magnific.com/vektor-premium/desain-logo-dealer-mobil-teks_1234880-1950.jpg?semt=ais_hybrid&w=740&q=80" alt="Foto toko kami" class="w-full rounded-xl block"
        />
      </div>
    </section>

    <!-- Bagian Tim Kami -->
    <section class="pt-5 px-10 pb-20 max-w-[1100px] mx-auto text-center">
      <h2 class="text-[#691515] mb-[30px]">Tim Kami</h2>
      <div class="flex flex-wrap justify-center gap-6">
        <TeamCard
          v-for="anggota in daftarTim"
          :key="anggota.id"
          :nama="anggota.nama"
          :jabatan="anggota.jabatan"
          :foto="anggota.foto"
        />
      </div>
    </section>
  </div>
</template>