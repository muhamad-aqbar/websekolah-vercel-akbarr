<template>
  <div class="landing-page">
    <!-- HERO SECTION -->
    <section class="hero">
        <center>
        <h1 class="hero-title">Mau Mobil? Beli lah di ℬ𝒶𝓇𝓈𝓈_𝒮𝒽ℴ𝓅</h1>
        <p class="hero-desc">
          Platform untuk mobil-mobil class atass.
        </p>
      </center>
      <RouterLink
        to="/product"
        class="hero-btn"
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
    icon: '🚘',
    title: 'Layanan kami',
    desc: 'Kami menyediakan mobil mobil berkualitas.'
  },
  {
    icon: '',
    title: 'Ulasan shop ',
    desc: 'Tampilan mudah disesuaikan dengan kebutuhan proyek kalian.'
  },
  {
    icon: '🔒',
    title: 'Terpercaya',
    desc: 'Kami juga menyediakan pelayanan yang terpercaya untuk para customer kami .'
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
  background: linear-gradient(
    to bottom right,
    rgba(0, 0, 0, 0.137) 40%,
    rgba(156, 58, 237, 0.286) 60%,
    #2c1414 100%
  );
  color: #fff;
  text-align: center;
  padding: 80px 20px;
  border-radius: 20px;
}

.hero-title {
  font-size: 2.25rem;
  font-weight: 700;
  margin-bottom: 24px;
  line-height: 1.375;
  text-align: center;
}

.hero-desc {
  font-size: 1.125rem;
  max-width: 500px;
  margin: 0 auto 40px;
  opacity: 0.9;
  line-height: 1.625;
}

.hero-btn {
  display: inline-block;
  background:rgb(95, 17, 158);
  color: #0f766e;
  padding: 12px 28px;
  border-radius: 9999px;
  font-weight: 600;
  text-decoration: none;
  transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
}

.hero-btn:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
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