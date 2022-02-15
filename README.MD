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
