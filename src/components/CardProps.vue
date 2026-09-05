
<template>
  <!-- VARIANT: banner -->
  <section v-if="variant === 'banner'" class="banner">
    <h1>{{ title }}</h1>
    <p v-if="desc">{{ desc }}</p>
  </section>

  <!-- VARIANT: info (item info kontak) -->
  <div v-else-if="variant === 'info'" class="info-item">
    <span class="info-item__ikon">{{ icon }}</span>
    <div>
      <strong>{{ title }}</strong>
      <p>{{ desc }}</p>
    </div>
  </div>

  <!-- VARIANT: feature (default, kartu fitur) -->
  <div v-else class="feature-card">
    <div class="feature-icon">{{ icon }}</div>
    <h3 class="feature-title">{{ title }}</h3>
    <p class="feature-desc">{{ desc }}</p>
  </div>
</template>

<script setup>
defineProps({
  variant: {
    type: String,
    default: 'feature' // 'feature' | 'banner' | 'info'
  },
  icon: {
    type: String,
    default: '⭐'
  },
  title: {
    type: String,
    default: ''
  },
  desc: {
    type: String,
    default: ''
  }
})
</script>

<style scoped>
/* ===== FEATURE CARD ===== */
.feature-card {
  background: linear-gradient(rgb(83, 39, 83) 40%, rgb(68, 26, 68) 60%, black 100%);
  border-radius: 16px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  padding: 32px 24px;
  width: 260px;
  text-align: center;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.feature-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 10px 20px rgba(46, 42, 42, 0.12);
}

.feature-icon {
  font-size: 2rem;
  margin-bottom: 12px;
}

.feature-title {
  font-size: 1.2rem;
  margin-bottom: 8px;
}

.feature-desc {
  font-size: 0.95rem;
  color: #cf73c8;
}

/* ===== BANNER ===== */
.banner {
  background: linear-gradient(135deg, rgba(0, 0, 0, 0.137) 40%, #9c3aed49 60%, rgb(44, 20, 20) 100%);
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
  opacity: 0.9;
}

/* ===== INFO ITEM ===== */
.info-item {
  display: flex;
  gap: 14px;
  align-items: flex-start;
  margin-bottom: 22px;
}

.info-item__ikon {
  font-size: 1.4rem;
}

.info-item strong {
  display: block;
  margin-bottom: 2px;
  color: aliceblue;
}

.info-item p {
  margin: 0;
  color: #666666;
}
</style>