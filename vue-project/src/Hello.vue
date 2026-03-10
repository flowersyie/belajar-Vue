<script setup>

</script>

<template>
    <div class="card">
    <img v-bind:src="produk.gambarProduk" width="300px">
    <h1>{{ produk.namaProduk }}</h1>
    <p>{{ produk.harga }}</p>
    <span v-if="produk.diskon" class="diskon">Diskon Tersedia</span>
    <span v-else class="diskon">Diskon Tidak Tersedia</span>
    <br> Tampil dalam desain bergaya Art Deco yang diperkenalkan pada tahun 1934, Alma BB handbag ini dibuat dari material Monogram canvas yang ikonis. Tas ini dilengkapi dengan berbagai detail khas yang memikat, seperti padlock dan kunci berwarna emas, dua handle Toron, serta key bell dari bahan kulit. Tas kecil ini dapat diselempang menggunakan tali yang dapat dilepas dan disesuaikan.</br>
    <p :class="produk.stock > 0 ? 'tersedia' : 'habis'">{{ produk.stock > 0 ? 'Stock Tersedia' : 'Stock Habis' }}</p>
    <a v-bind:href="produk.linkBeli" 
    :style="{
        backgroundColor: produk.stock > 0 ? 'green' : 'red',
        color: 'white',
        padding: '10px 20px',
        textDecoration: 'none',
    }"
    >Beli Sekarang</a>
    </div>
</template>

<script>
export default {

    data() {
        return {
            produk: { 
            namaProduk: 'Louis Vuitton Alma BB Monogram Canvas',
            gambarProduk: 'https://id.louisvuitton.com/images/is/image/lv/1/PP_VP_L/louis-vuitton-alma-bb--M46990_PM1_Side%20view.png?wid=4096&hei=4096',
            harga: "Rp. 33.500.000",
            linkBeli: "https://id.louisvuitton.com/ind-id/products/alma-bb-monogram-nvprod5190086v/M46990",
            stock: 5,
            diskon:true,
            },
            
        }
    },
}
</script>

<style scoped>
.card {
    width: 300px;
    border: 1px solid #444; 
    padding: 20px;
    margin: 20px;
    background-color: black; 
    color: white;            
    border-radius: 10px;
}

.habis {
    color: red;
}
.tersedia {
    color: green;
}
.diskon {
    color: #000;
    background-color: #f1c40f; 
    padding: 5px 10px;
    display: inline-block;
    border-radius: 4px;
    font-weight: bold;
    margin: 10px 0;
}

</style>