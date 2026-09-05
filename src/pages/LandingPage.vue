<template>
  <div class="landing-page">
    <!-- HERO SECTION -->
    <section class="bg-gradient-to-br from-black/[0.137] from-[40%] via-[#9c3aed]/[0.286] via-[60%] to-[#2c1414] to-100% text-white text-center px-5 py-20 rounded-[20px]">
      <h1 class="text-4xl font-bold mb-6 leading-snug">Mau Mobil? Beli lah di ℬ𝒶𝓇𝓈𝓈_𝒮𝒽ℴ𝓅</h1>
      <p class="text-lg max-w-[500px] mx-auto mb-10 opacity-90 leading-relaxed">
       Platform untuk mobil-mobil class atass.
      </p>
      <RouterLink
        to="/product"
        class="inline-block bg-white text-teal-700 px-7 py-3 rounded-full font-semibold no-underline transition-all duration-200 ease-in-out hover:-translate-y-1 hover:shadow-lg"
      >
        Lihat Produk
      </RouterLink>
    </section>

    <!-- FEATURE SECTION -->
     <center>
    <video controls width="480" loop>
 <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4" />
 Browser kamu tidak mendukung pemutaran video.
 </video>
 </center>

    <section class="features">
      <CardProps
        v-for="feature in features"
        :key="feature.title"
        :icon="feature.icon"
        :title="feature.title"
        :desc="feature.desc"
      />
    </section>
  </div>
</template>

<script setup>
import CardProps from '../components/CardProps.vue'
const features = [
  {
    icon: '🚀',
    title: 'Cepat & Ringan',
    desc: 'Performa optimal tanpa membebani perangkat pengguna.'
  },
  {
    icon: '🎨',
    title: 'Desain Fleksibel',
    desc: 'Tampilan mudah disesuaikan dengan kebutuhan proyek kalian.'
  },
  {
    icon: '🔒',
    title: 'Aman & Terpercaya',
    desc: 'Data pengguna dikelola dengan standar keamanan yang baik.'
  }
]
</script>

<style scoped>
.landing-page {
  font-family: "Segoe UI", sans-serif;
  color: #222;
}

/* ===== FEATURES ===== */
.features {
  display: flex;
  gap: 24px;
  flex-wrap: wrap;
  justify-content: center;
  padding: 60px 20px;
}

video {
 margin-top: 16px;
 border-radius: 10px;
 display: block;
}
</style>