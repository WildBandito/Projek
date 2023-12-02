<template>
    <div class="container">
        <div class="row">
            <div class="mr40 mt20">
                <router-link to="/list-voucher">
                    <img src="../../assets/icons/back.svg">
                </router-link>
            </div>
            <div>
                <h1 class="m0">Edit Voucher</h1>
                <p class="mt5 mb20 tc-green">Make your customers shop using vouchers</p>
            </div>
        </div>
        <hr class="uline-grey">
        <div class="flex mt50">
            <label class="form-label">Voucher Image</label>
            <div class="fixed-button-container">
         <div class="left-button">
    <button class="bt-submit-green">+ Tambahkan foto</button>
</div>
</div>

        <div class="mt50 row">
            <div class="w20">
                <label class="form-label">Voucher Code</label>
            </div>
            <div class="w80">
                <input
                    class="form-text"
                    type="int"
                    placeholder="Masukkan Kode Voucher"
                >
            </div>
        </div>
        <div class="mt30 row">
            <div class="w20">
                <label class="form-label">Voucher Name</label>
            </div>
            <div class="w80">
                <input
                    class="form-text"
                    type="text"
                    placeholder="Masukan Voucher Name"
                >
            </div>
        </div>
        <div class="mt30 row">
            <div class="w20">
                <label class="form-label">Description</label>
            </div>
            <div class="w70">
                <input
                    class="text-description "
                    type="text"
                    placeholder="Masukan Voucher Desription "
                >
            </div>
        </div>
        <div class="mt30 row">
            <div class="w20">
                <label class="form-label">Type</label>
            </div>
            <div class="w80">
                <select class="form-select">
                    <option disabled selected>--- Type ---</option>
                    <option value="1">Total</option>
                    <option value="2">Grand Total</option>
                    <option value="3">Ongkos Kirim</option>
                </select>
            </div>
        </div>
        <div class="mt30 row">
            <div class="w20">
                <label class="form-label">Min. Transaction</label>
            </div>
            <div class="w80">
                <input
                    class="form-text"
                    type="text"
                    placeholder="Masukkan minimal transaction"
                >
            </div>
        </div>
        <div class="mt30 row">
            <div class="w20">
                <label class="form-label">Amount</label>
            </div>
            <div class="w80">
                <input
                    class="form-text"
                    type="text"
                    placeholder="Masukan Amount"
                >
            </div>
        </div>
        <div class="mt30 row">
            <div class="w20">
                <label class="form-label">Valid From</label>
                
            </div>
            <div class="w80">
                <input
                    class="form-text"
                    type="text"
                    placeholder="Valid From"
                >
            </div>
        </div>
        <div class="mt30 row">
            <div class="w20">
                <label class="form-label">Valid Untill</label>
            </div>
            <div class="w80">
                <input
                    class="form-text"
                    type="text"
                    placeholder="Valid Untill"
                >
            </div>
        </div>
        <div class="flex mt30">
            <router-link to="/list-voucher">
                <button class="bt-submit-green">Update Voucher</button>
            </router-link>
        </div>
    </div>
</div>
</template>

<script>
export default {
name: 'add-voucher'
}


</script>

<style>

/*.bt-submit-green {

position: fixed;
padding: 10px 10px; /* Sesuaikan padding sesuai kebutuhan */
/* padding-bottom: 40px;
border: 2px solid #4caf50; /* Warna batas tombol */
/* background-color: transparent; /* Warna latar belakang transparan */
/*color: #4caf50; /* Warna teks tombol */
/*border-radius: 10px; /* Sudut lengkungan */
/*cursor: pointer;
transition: background-color 0.5s ease;
/*}
.fixed-button:hover{
background-color: #4caf50;  
}
.left-button {
position: fixed;
left: 550px;
top: 20%;
transform: translateY(-50%);
cursor: pointers;
}
.bt-submit-green:hover {
background-color: #4caf50; /* Warna latar belakang saat tombol dihover */
/*  color: #fff; /* Warna teks saat tombol dihover */

.fixed-button-container {
position: absolute;
top: 22%; /* Sesuaikan dengan tinggi yang diinginkan */
left: 550px; /* Sesuaikan dengan posisi yang diinginkan */
display: flex;
align-items: center;
}

left-button {
margin-left: 10px; /* Sesuaikan margin sesuai kebutuhan */
position: relative;
/* You can adjust the values below as needed */
top: 10px;
left: 10px;
}

.bt-submit-green {
padding: 10px 10px; /* Sesuaikan padding sesuai kebutuhan */
border: 2px solid #4caf50; /* Warna batas tombol */
background-color: transparent; /* Warna latar belakang transparan */
color: #4caf50; /* Warna teks tombol */
border-radius: 10px; /* Sudut lengkungan */
cursor: pointer;
transition: background-color 0.5s ease;
}

.bt-submit-green:hover {
background-color: #4caf50;
}
.w70 {
width: 10%; /* Sesuaikan lebar kolom sesuai kebutuhan */
}

.text-description {
width: 800%; /* Lebar input sesuai dengan parentnya */
height: 200px; /* Tinggi input, sesuaikan sesuai kebutuhan */
/* atau Anda dapat menggunakan properti max-height agar input dapat tumbuh jika kontennya melebihi tinggi tertentu */
/* max-height: 100px; */
box-sizing: border-box; /* Memastikan bahwa padding dan border tidak menambah lebar atau tinggi elemen */
}


</style>
