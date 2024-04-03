## <center>Digiflazz client library</center>

### Instalasi

`npm install lutz-digi`

### Dokumentasi

```js
const Digiflazz = require("lutz-digi");
const digiflazz = new Digiflazz("username", "apikey");
```

#### Buyer Area

##### Cek Saldo

```js
let saldo = await digiflazz.cekSaldo();
```

##### Daftar Harga

```js
let harga = await digiflazz.daftarHarga();
```

##### Tiket Deposit

```js
let deposit = await digiflazz.deposit(nominal, "BANK", "Nama Pemilik Rekening");
```

##### Topup & Status Topup

```js
let deposit = await digiflazz.transaksi("sku", "tujuan", "ref_id");
```

##### Inquiry Pascabayar

```js
let deposit = await digiflazz.transaksi("sku", "tujuan", "ref_id", "CEK");
```

##### Bayar Pascabayar

```js
let deposit = await digiflazz.transaksi("sku", "tujuan", "ref_id", "BAYAR");
```

##### Status Pascabayar

```js
let deposit = await digiflazz.transaksi("sku", "tujuan", "ref_id", "STATUS");
```

##### Webhook

```js
const Digiflazz = require("lutz-digi");
const digiflazz = new Digiflazz("username", "apikey", "webhookkey");

app.post("/hook", Digiflazz.webhook(digiflazz), (req) => {
  // Anda dapat memproses hasilnya disini
  // result webhook dapat diakses di req.digiwebhooks
});
```

### Author

[Lutz Dev](https://lutzdev.tech)
