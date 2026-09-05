src/components/ProductCard.vue (dikembangkan — lengkapi bagian bergaris)
<script setup>
import { ref } from 'vue'
 
const props = defineProps({
  nama: String,
  harga: Number,
  gambar: String,
  imgStyle: {
    type: Object,
    default: () => ({ width: '100%', height: '180px', objectFit: 'cover' })
  }
})
 
const gambarDipilih = ref(null)
 
function bukaPreview(src) {
  gambarDipilih.value = src // isi: src gambar yang diklik
}
 
function tutupPreview() {
  gambarDipilih.value = null
}
 
// --- bagian baru: efek suara ---
function tambahKeKeranjang(nama) {
 const suara = new Audio('nikin-pop-up-something-160353.mp3')
 suara.play()
 alert(`${nama} ditambahkan ke keranjang!`)
}
</script>
 
<template>
  <div class="card">
    <div class="image-box">
      <img :src="gambar" :alt="nama" :style="imgStyle" @click="bukaPreview(gambar)" />
    </div>
    <h3>{{ nama }}</h3>
    <p>$ {{ harga.toLocaleString('id-ID') }}</p>
    <button @click="tambahKeKeranjang(nama)">Tambah ke Keranjang</button>
  </div>
 
  <div v-if="gambarDipilih" class="preview-overlay" @click="tutupPreview">
    <img :src="gambarDipilih" class="preview-besar" />
</div>
</template>
 
<style scoped>
.card {
 border: 1px solid #410469;
 border-radius: 10px;
 padding: 14px;
 width: 380px;
 text-align: center;
 display: flexbox;
 
}
.image-box {
 width: 350px;
 height: 250px;
 overflow: hidden;
 border-radius: 6px;
 line-height: 0;
}
.card img {
 display: block;
 width: 100%;
 border-radius: 6px;
}
 
.preview-overlay {
  position: fixed; top: 0; left: 0; width: 100%; height: 100%;
  background: rgba(0,0,0,0.7);
  display: flex; align-items: center; justify-content: center;
}
.preview-besar { max-width: 80%; max-height: 80%; border-radius: 8px; }
 
button {
 margin-top: 8px;
 padding: 6px 12px;
 border: none;
 border-radius: 6px;
 background: #c7206e49;
 color: white;
 cursor: pointer;
}
button:hover { background: #68265f; }
 
</style>
