# Flask Exercises

![Purwadhika](https://static.wixstatic.com/media/2e6af2_f69a4271c3534ae1869a7ed63e278b2b~mv2.png/v1/fill/w_246,h_39,al_c,usm_0.66_1.00_0.01/2e6af2_f69a4271c3534ae1869a7ed63e278b2b~mv2.png)

#

<img src='https://img.pokemondb.net/sprites/sun-moon/icon/pikachu.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/bulbasaur.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/charmander.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/squirtle.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/caterpie.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/pidgey.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/rattata.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/clefairy.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/poliwhirl.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/jigglypuff.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/growlithe.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/nidoran-m.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/nidoran-f.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/psyduck.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/machop.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/bellsprout.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/haunter.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/krabby.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/magikarp.png' alt='lintang' style='height:13px; width:18px'/>

### **Soal 1 - Pokemon Battle**

Disediakan __beberapa dataset__ seputar data spesies Pokemon beserta history pertandingan antar Pokemon. File **_pokemon.csv_** berisi data lengkap 800 spesies Pokemon, sedangkan file _**combats.csv**_ berisi data historis duel Pokemon beserta pemenangnya. Unduh dataset langsung dari sumbernya: [klik sini](https://www.kaggle.com/sekarmg/pokemon).

Dengan dataset tersebut, buatlah sebuah __aplikasi Flask__ berisi model machine learning (model bebas) yang dapat memprediksi pemenang dari duel Pokemon. Aplikasi yang dibuat harus memenuhi syarat minimal berikut:

1. Server aplikasi akan berjalan di __localhost:5000__ dan ketika user melakukan GET request via browser akan tampil sebuah halaman __HTML__ sederhana yang memuat __2 buah text input__ dan __1 buah button__. Desain tampilan HTML tidak harus sama seperti contoh soal, utamakan fitur!

    ![poke_1](./a.png)

2. User dapat memasukkan nama Pokemon yang akan dipertandingkan ke dalam text input yang tersedia. Saat user menekan tombol button __'Battle!'__, aplikasi akan memproses data yang telah diinputkan oleh user.

    ![poke_2](./b.png)

3. Jika data sukses diproses, maka user akan di-_redirect_ ke __localhost:5000/hasil__ berisi halaman __HTML__ yang menampilkan: 
    
    - __Gambar Pokemon__
        - gunakan __Poke API__ ([_klik sini_](https://pokeapi.co/))
        - __GET__ ke https://pokeapi.co/api/v2/pokemon/{nama_Pokemon}

    - __Grafik perbandingan skill Pokemon__ (dari dataset): 
        - HP, 
        - Attack 
        - Defense 
        - Special Attack
        - Special Defense 
        - Speed

    - __Kemungkinan pemenang__ beserta __% probabilitasnya__

    Halaman ini juga dilengkapi __1 buah button__ untuk kembali ke halaman awal. Desain tampilan HTML tidak harus sama seperti contoh soal, utamakan fitur! Contoh:

    -  <img src='https://img.pokemondb.net/sprites/sun-moon/icon/charmander.png' alt='lintang' style='height:13px; width:18px'/> __Charmander vs Bulbasaur__ <img src='https://img.pokemondb.net/sprites/sun-moon/icon/bulbasaur.png' alt='lintang' style='height:13px; width:18px'/>

        ![poke_3](./c.png)

    -  <img src='https://img.pokemondb.net/sprites/sun-moon/icon/pikachu.png' alt='lintang' style='height:13px; width:18px'/> __Pikachu vs Charizard__ <img src='https://img.pokemondb.net/sprites/sun-moon/icon/charizard.png' alt='lintang' style='height:13px; width:18px'/>

        ![poke_3](./d.png)

    -  <img src='https://img.pokemondb.net/sprites/sun-moon/icon/mewtwo.png' alt='lintang' style='height:13px; width:18px'/> __Mewtwo vs Mew__ <img src='https://img.pokemondb.net/sprites/sun-moon/icon/mew.png' alt='lintang' style='height:13px; width:18px'/>

        ![poke_3](./e.png)
    
4. Namun jika data tidak ditemukan, tidak ada di dalam dataset atau user masuk ke url yang tidak tersedia, maka user akan di-redirect ke halaman __HTML__ yang memberikan informasi bahwa data tidak ditemukan, __error 404__. Halaman ini juga dilengkapi __1 buah button__ untuk kembali ke halaman awal. Desain tampilan HTML tidak harus sama seperti contoh soal, utamakan fitur!

    ![poke_4](https://raw.githubusercontent.com/LintangWisesa/Ujian_Fundamental_JCDS04/master/poke_4.png)


_**Catatan:**_ _Lampiran jawaban dalam bentuk folder Battle_Pokemon yang sudah diupload_

#

## **Soal 2 - Pokemon Recommendation**

Disediakan sebuah dataset Pokemon: [unduh di sini](https://www.kaggle.com/abcsds/pokemon), beserta Pokemon API: [akses di sini](https://pokeapi.co/). Buatlah sebuah __*content-based filtering recommender system*__ dengan menggunakan __Flask__, yang dapat memfasilitasi user untuk menyebutkan Pokemon favoritnya & menyajikan rekomendasi __6 Pokemon__ berdasarkan feature: __Type 1__, __Generation__ & __Legendary__ Pokemon. Aplikasi yang dibuat harus memenuhi syarat minimal berikut:

1. Server aplikasi akan berjalan di __localhost:5000__ dan ketika user melakukan GET request via browser akan tampil sebuah halaman __HTML__ sederhana yang memuat __1 buah text input__ dan __1 buah button__. Desain tampilan HTML tidak harus sama seperti contoh soal, utamakan fitur!

    ![poke_1](./soal2a.png)

2. User dapat memasukkan nama Pokemon favoritnya ke dalam text input yang sudah disediakan. Saat user menekan tombol __"Cari Pokemon"__, jika data ditemukan, maka user akan di-redirect ke __localhost:5000/hasil__ yang berisi halaman __HTML__, yang menampilkan data seputar Pokemon favorit user, disertai dengan data __6 Pokemon__ yang direkomendasikan berdasarkan __type__, __generasi__ & __legend__. Data yang ditampilkan untuk tiap Pokemon minimal: _nama_, _gambar_, _tipe_, _generasi_ & _legendary_. Gambar Pokemon tidak terdapat pada dataset, tapi dapat diambil dari [Pokemon API](https://pokeapi.co/). Halaman ini juga dilengkapi __1 buah button__ untuk kembali ke halaman awal. Desain tampilan HTML tidak harus sama seperti contoh soal, utamakan fitur!

    - Contoh jika user memfavoritkan __Pikachu__ <img src='https://img.pokemondb.net/sprites/sun-moon/icon/pikachu.png' alt='lintang' style='height:13px; width:18px'/>:
    
        ![poke_2](./soal2b.png)

        ![poke_3](./soal2c.png)

    - Contoh jika user memfavoritkan __Pidgeotto__ <img src='https://img.pokemondb.net/sprites/sun-moon/icon/pidgey.png' alt='lintang' style='height:13px; width:18px'/>:

        ![poke_4](./soal2d.png)

        ![poke_5](./soal2e.png)

4. Namun jika Pokemon favorit user tidak ditemukan, maka user akan di-redirect ke halaman __HTML__ yang memberikan informasi bahwa data tidak ditemukan. Halaman ini juga dilengkapi __1 buah button__ untuk kembali ke halaman awal. Desain tampilan HTML tidak harus sama seperti contoh soal, utamakan fitur!

    ![poke_6](./soal2f.png)


_**Catatan:**_ _Lampiran jawaban dalam bentuk folder Pokemon_Recommend yang sudah diupload_

<img src='https://img.pokemondb.net/sprites/sun-moon/icon/raichu.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/venusaur.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/charizard.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/blastoise.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/butterfree.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/pidgeot.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/raticate.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/clefable.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/poliwrath.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/wigglytuff.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/arcanine.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/nidoking.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/nidoqueen.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/golduck.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/machamp.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/victreebel.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/gengar.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/kingler.png' alt='lintang' style='height:13px; width:18px'/> <img src='https://img.pokemondb.net/sprites/sun-moon/icon/gyarados.png' alt='lintang' style='height:13px; width:18px'/>

#

<img src='http://digidb.io/images/dot/dot050.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot151.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot303.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot343.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot348.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot307.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot096.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot081.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot361.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot114.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot392.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot706.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot707.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot090.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot055.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot701.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot391.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot389.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot758.png' alt='lintang' style='height:13px; width:18px'/>
<img src='http://digidb.io/images/dot/dot697.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot020.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot708.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot009.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot112.png' alt='lintang' style='height:13px; width:18px'/>

## **Soal 3 - Scraping Digimon to JSON**

Tersedia data lengkap __341 Digimon__ di laman [__DigiDB.io__](http://digidb.io/digimon-list/). Buatlah sebuah file __python (.py)__ dan gunakan teknik _web scraping_ untuk mengekstrak data di laman tersebut, kemudian _export_ semua data sebagai file __JSON (digimon.json)__ dengan struktur data sebagai berikut:

```javascript
...,
{
    "no": 46,
    "digimon": "Patamon",
    "image": "http://digidb.io/images/dot/dot096.png",
    "stage": "Rookie",
    "type": "Data",
    "attribute": "Wind",
    "memory": 4,
    "equip slots": 1,
    "hp": 880,
    "sp": 93,
    "atk": 79,
    "def": 74,
    "int": 92,
    "spd": 90
},
...
```

Ilustrasi dari proses yang diharapkan:

![soal2](./soal3.png)

_**Catatan:**_ _Lampiran jawaban dalam bentuk folder Digimon_Scraping yang sudah diupload_

#

## **Soal 4 - Digimon Recommendation**

Dengan memanfaatkan file output __digimon.json__ dari _Soal 3_ di atas, buatlah sebuah __*content-based filtering recommender system*__ dengan menggunakan __aplikasi Flask__, yang dapat memfasilitasi user untuk menyebutkan Digimon favoritnya & menyajikan rekomendasi __6 Digimon__ berdasarkan feature: __stage__, __type__ & __attribute__ Digimon. Aplikasi yang dibuat harus memenuhi syarat minimal berikut:

1. Server aplikasi akan berjalan di __localhost:5000__ dan ketika user melakukan GET request via browser akan tampil sebuah halaman __HTML__ sederhana yang memuat __1 buah text input__ dan __1 buah button__. Desain tampilan HTML tidak harus sama seperti contoh soal, utamakan fitur!

    ![digi_1](./soal3a.png)

2. User dapat memasukkan nama Digimon favoritnya ke dalam text input yang sudah disediakan. Saat user menekan tombol __"Submit"__, aplikasi akan mengambil data Digimon favorit user di file __digimon.json__. Jika data ditemukan, maka user akan di-redirect ke __localhost:5000/hasil__ yang berisi halaman __HTML__, yang menampilkan data seputar Digimon favorit user, disertai dengan data __6 Digimon__ yang direkomendasikan berdasarkan __stage__, __type__ & __attribute__-nya. Data yang ditampilkan untuk tiap Digimon minimal hanya: _nama_, _gambar_, _stage_, _type_ & _attribute Digimon_. Halaman ini juga dilengkapi __1 buah button__ untuk kembali ke halaman awal. Desain tampilan HTML tidak harus sama seperti contoh soal, utamakan fitur!

    - Contoh jika user memfavoritkan __Agumon__ <img src='http://digidb.io/images/dot/dot050.png' alt='lintang' style='height:13px; width:18px'/>:
    
        ![digi_2](./soal3b.png)

        ![digi_3](./soal3c.png)

    - Contoh jika user memfavoritkan __Wargreymon__ <img src='http://digidb.io/images/dot/dot027.png' alt='lintang' style='height:13px; width:18px'/>:

        ![digi_4](./soal3d.png)

        ![digi_5](./soal3e.png)

4. Namun jika Digimon favorit user tidak ditemukan atau tidak ada di dalam file __digimon.json__, maka user akan di-redirect ke halaman __HTML__ yang memberikan informasi bahwa data tidak ditemukan. Halaman ini juga dilengkapi __1 buah button__ untuk kembali ke halaman awal. Desain tampilan HTML tidak harus sama seperti contoh soal, utamakan fitur!

    ![digi_6](./soal3f.png)

_**Catatan:**_ _Lampiran jawaban dalam bentuk folder Digimon_Recommend yang sudah diupload_

<img src='http://digidb.io/images/dot/dot326.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot012.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot304.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot344.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot349.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot308.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot087.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot093.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot148.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot365.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot091.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot015.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot711.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot078.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot068.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot710.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot395.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot904.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot901.png' alt='lintang' style='height:13px; width:18px'/>
<img src='http://digidb.io/images/dot/dot105.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot420.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot779.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot080.png' alt='lintang' style='height:13px; width:18px'/> <img src='http://digidb.io/images/dot/dot135.png' alt='lintang' style='height:13px; width:18px'/>

#
