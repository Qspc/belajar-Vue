# Catatan Vue JS & Quasar

# Seputar V-

## V-bind :

- v-bind:title = untuk nyimpen judul yg muncul pas di hover (disimpen di data)
- v-bind:href = bikin link
- v-bind:class = aktif/nonaktif class (disimpen di data)
- v-bind:style = menambahkan komponen css lewat class (disimpen di data)
- penulisan v-bind bisa disingkat. contoh v-bind:key jadi :key

## v-if:

- v-if = bikin fungsi if (disimpen di data)

## v-for

- v-for = bikin looping (disimpen di data)

## v-on

- v-on:click = bikin fungsi after di klik bakal apa (disimpen di method)
- v-on:change = membuat perubahan pada form upload gambar
- v-on:submit.prevent = tidak akan memuat halaman
- v-on:keyup.enter = berfungsi saat pencet enter
- Vue.config.keyCodes.f1 = berfungsi saat tekan f1
- v-on:click.ctrl = berfungsi saat tekan ctrl
- penulisan v-on bisa disingkan. contoh v-con:click jadi @click

## v-model

- v-model = bikin isi teks yg muncul (disimpen di data)
- v-model.lazy = input berubah setelah ditulis (tidak realtime)
- v-model.trim = input yg dimasukan tanpa spasi

# Data

objek yg digunakan pada vue.js. bentuk objeknya bisa berbeda-beda. bisa integer, string, array, boolean dll

# bedanya

- bedanya computed dan method?

# component

- component kalo di laravel mirip2 partial. cara motong2 setiap bagian biar bisa dipisah2. kaya navbar, sidebar, container, footer dll
- untuk menambahkan konten/tulisan pada tag component nya maka tambahkan tag <slot> di bagian component nya
  // contoh bentuk component
  Vue.component('button-counter', {
  data: function () {
  return {
  count: 0
  }
  },
  template: '<button v-on:click="count++">You clicked me {{ count }} times.</button>'
  })

<div id="components-demo">
  <button-counter></button-counter>
</div>

new Vue({ el: '#components-demo' })

# Props

custom atribut yg bisa didaftarkan pada component

## alur component di quasar

- ada dua file utama : index.html dan app.vue. index.html untuk root dari struktur html nya dan app.vue sebagai awal dari semua component yg dipakai
- lalu ada router.js sebagai pusat dari semua link yang dipakai pada websiter kita. isinya ada dua :
  1. root, komponen yg selalu muncul di semua tampilan. ex : navbar, sidebar dll
  2. child, komponen yg berbeda-beda saat masuk ke link lain. ex : main page
- selanjutnya terdapat 5 folder yang dipakai (setidaknya untuk sekarang) :
  1. assets, sebagai tempat penyimpanan aset & gambar2 yg bakal dipakai
  2. boot, kurang tau fungsinya buat apa
  3. css, sebagai root untuk semua komponen css yang akan dipasang
  4. layout, sebagai komponen root pada routes. ya contohnya kaya tempat bikin sidebar dll
  5. pages, berbagai file yg sesuai dengan folder yg dipilih masing2
-

index.html -> id nya q-app
app.vue -> namanya app & tag <router-view />
layout isinya :
header
drawer -> import dari file component juga (yang essential)
footer
page layout -> isinya tag <router-view />
