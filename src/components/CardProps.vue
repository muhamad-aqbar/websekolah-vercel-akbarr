<!-- <template>
  <div class="card">
    <h2>{{ nama }}</h2>
    <p>Umur: {{ umur }}</p>
  </div>
</template>

<script setup>
defineProps({
  nama: String,
  umur: Number
})
</script> -->
<template>
  <div class="feature-card">
    <div class="feature-icon">{{ icon }}</div>
    <h3 class="feature-title">{{ title }}</h3>
    <p class="feature-desc">{{ desc }}</p>
  </div>
</template>

<script setup>
defineProps({
  icon: {
    type: String,
    default: '⭐'
  },
  title: {
    type: String,
    required: true
  },
  desc: {
    type: String,
    default: ''
  }
})
</script>

<style scoped>
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
</style>