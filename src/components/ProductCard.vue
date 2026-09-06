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
      <div class="btn-grad">
        <button @click="tambahKeKeranjang(nama)">Tambah ke Keranjang</button>
      </div>
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
 width: 100%;
 max-width: 380px;
 margin: 0 auto;
 text-align: center;
 display: flex;
 flex-direction: column;
 align-items: center;

}
.image-box {
 width: 100%;
 max-width: 350px;
 height: 250px;
 margin: 0 auto;
 overflow: hidden;
 border-radius: 6px;
 line-height: 0;
}
.card img {
 display: block;
 width: 100%;
 height: 100%;
 border-radius: 6px;
}
 
.preview-overlay {
  position: fixed; top: 0; left: 0; width: 100%; height: 100%;
  background: rgba(0,0,0,0.7);
  display: flex; 
  align-items: center;
  justify-content: center;
}
.preview-besar { max-width: 80%; max-height: 80%; border-radius: 8px; }
 
.btn-grad {
  background-image: linear-gradient(to right, #1D2B64 0%, #F8CDDA 51%, #1D2B64 100%);
}

.btn-grad {
  margin: 10px;
  padding: 15px 45px;
  text-align: center;
  text-transform: uppercase;
  transition: 0.5s;
  background-size: 200% auto;
  color: white;
  box-shadow: 0 0 20px #130101;
  border-radius: 10px;
  display: block;
  outline: none;
  border: none;
}

.btn-grad:hover {
  background-position: right center;
  color: #140202;
  text-decoration: none;
}
 
</style>