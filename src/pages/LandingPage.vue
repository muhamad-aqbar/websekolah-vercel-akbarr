 <!-- <template>
 <main>
 <h1>Selamat Datang di Onlineshop Sekolah</h1>
 <p>Belanja gampang, sekolah senang.</p>
 </main>
</template> -->
<template>
  <div class="landing-page">
    <!-- HERO SECTION -->
    <section class="hero">
      <h1 class="hero-title">Mau Mobil? Beli lah di ℬ𝒶𝓇𝓈𝓈_𝒮𝒽ℴ𝓅</h1>
      <p class="hero-subtitle">
       Platform untuk mobil-mobil class atass.
      </p>
      <RouterLink to="/product" class="hero-button">
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

/* ===== HERO ===== */
.hero {
  background: linear-gradient(135deg, rgba(0, 0, 0, 0.137)40%, #9c3aed49)60%, rgb(44, 20, 20)100%;
  color: #fff;
  padding: 80px 20px;
  text-align: center;
  border-radius: 20px;
}

.hero-title {
  font-size: 2.5rem;
  margin-bottom: 16px;
}

.hero-subtitle {
  font-size: 1.1rem;
  max-width: 500px;
  margin: 0 auto 32px;
  opacity: 0.9;
}

.hero-button {
  display: inline-block;
  background: #fff;
  color: #0f766e;
  padding: 12px 28px;
  border-radius: 999px;
  font-weight: 600;
  text-decoration: none;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.hero-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
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
