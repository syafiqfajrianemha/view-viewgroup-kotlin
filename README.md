# View and ViewGroup
### Pada dasarnya, semua elemen UI di aplikasi Android dibangun menggunakan dua buah komponen inti, yaitu View dan ViewGroup.
![alt text](https://dicoding-web-img.sgp1.cdn.digitaloceanspaces.com/original/academy/dos:9a62eb3243a3da1dbea094100606c44620221223160840.jpeg?raw=true)
## Rangkuman View and ViewGroup
- **View** merupakan komponen dasar yang tampil di layar dan dapat digunakan untuk berinteraksi dengan pengguna. Contoh komponen turunan dari View adalah TextView, Button, ImageView, RadioButton, Checkbox, dll.
- **ViewGroup** adalah sebuah View spesial yang mewadahi objek-objek View lainnya dan berguna untuk mengatur posisinya.
- **LinearLayout** digunakan untuk menempatkan komponen-komponen di dalamnya secara horizontal atau vertikal.
- **RelativeLayout** digunakan untuk menempatkan masing-masing komponen secara fleksibel dan relatif terhadap komponen yang lainnya. Misalnya komponen A di sebelah kanan komponen B atau komponen A rata tengah dengan parent-nya.
- **FrameLayout** digunakan untuk membuat komponen menjadi menumpuk atau saling menutupi satu dengan yang lainnya.
- **TableLayout** digunakan untuk menyusun komponen dalam baris dan kolom.
- **ConstraintLayout** Merupakan layout default dan direkomendasikan di dalam XML. Dengan ConstraintLayout, Anda dapat menyusun tampilan yang kompleks cukup dengan satu lapis hierarki saja.
Hal ini akan memberikan performa dan proses rendering yang lebih baik daripada penggunaan nested layout (layout di dalam layout). Berikut beberapa fiturnya:
  - **Relative Positioning**: memposisikan komponen secara relatif terhadap komponen yang lain.
  - **Center Positioning & Bias**: untuk menentukan alignment dengan menggunakan persentase, default-nya 50% atau tengah.
  - **Baseline alignment**: untuk membuat text pada suatu komponen sejajar dengan teks pada komponen lain.
  - **Guideline**: untuk membuat garis pembantu yang tidak terlihat oleh user.
  - **Barrier**: sama seperti Guideline, tetapi posisinya dapat mengikuti komponen lainnya.
  - **Chain**: mengatur sekumpulan komponen secara linear.
    - **Spread**: setiap elemen akan menyebar (default style).
    - **Spread inside**: tampilan pertama dan terakhir akan ditempelkan pada batasan di setiap ujung rantai, sedangkan sisanya akan didistribusikan secara merata.
    - **Weighted**: jika beberapa widget disetel ke "match constraint", mereka akan membagi ruang yang tersedia.
    - **Packed**: elemen akan menyatu dan dikemas bersama.
  - **ScrollView** digunakan untuk membuat komponen di dalamnya dapat digeser (scroll) secara vertikal maupun horizontal. Di dalamnya hanya boleh ada satu layout ViewGroup, tidak boleh lebih.
  - Untuk menambahkan gambar ke drawable, copy paste gambar dari explorer ke folder **drawable**. Pilih folder drawable (bukan drawable-v24) untuk mendukung semua versi Android.
  Ingat bahwa nama file yang ada di dalam resource drawable harus menggunakan **huruf kecil** dan **underscore** saja.
  - Untuk mengubah **icon aplikasi**, klik kanan pada folder res dan pilih **New** → **Image Asset**. Pilih Launcher Icons (Adaptive and Legacy) pada Icon Type,
  pilih gambar pada Path, lalu klik Next → Finish sehingga, icon akan tersimpan di folder mipmap dengan berbagai density (mdpi, hdpi, xhdpi, xxhdpi, dan xxxhdpi).
  - **Layout Inspector** digunakan untuk menganalisis hierarki dan properties pada suatu tampilan. 
  - Penggunaan **Start** dan **End** pada margin daripada Right dan Left berfungsi supaya mendukung dua jenis bahasa, baik Left to Right (LTR) seperti bahasa Inggris maupun Right to Left (RTL) seperti bahasa Arab.
![alt text](https://github.com/syafiqfajrianemha/view-viewgroup-kotlin/blob/main/ui-view-viewgroup.png?raw=true)

## Rangkuman Style dan Theme
- **Style** merupakan sebuah kumpulan properti yang dibutuhkan untuk mendefinisikan bagaimana sebuah komponen View ataupun ViewGroup ditampilkan. 
- Pemusatan style cocok digunakan untuk mengumpulkan atribute yang berulang-ulang digunakan di banyak komponen sehingga jika ada perubahan, cukup ubah di satu tempat saja.
- **Style** terdefinisi dalam file xml sendiri. Anda bisa menemukannya di **res** → **values** → **themes.xml**. 
- Semua style yang dibuat harus berada dalam tag resources. Setiap style dibuat menggunakan tag style dan tag item untuk mendefinisikan property-nya.
- Untuk memanggil style pada XML, gunakan property style = “@style/NamaStyle”.
- **Theme** merupakan sebuah style yang diterapkan khusus untuk Activity dan Application pada berkas AndroidManifest.xml.
- **Dark Theme** dapat mengurangi konsumsi energi pada handphone dan membuat aplikasi lebih mudah dibaca walaupun cahaya sedikit.
- **Material Design** merupakan panduan desain yang dibuat oleh Google untuk membuat user interface dan user experience pada Android.
- Untuk membuat theme, gunakan tag style dengan parent berupa Theme, seperti “Theme.MaterialComponents.DayNight.DarkActionBar” yang merupakan tema dengan background putih dan action bar berwarna gelap.
- Beberapa atribut yang dapat dikustomisasi di dalamnya yaitu:
    ![alt text](https://dicoding-web-img.sgp1.cdn.digitaloceanspaces.com/original/academy/dos:1c820bea6c084d80f1b5da7ce0114ed620221223161244.jpeg?raw=true)
  - **colorPrimary**: warna utama aplikasi yang tampil pada Action Bar dan komponen Button.
  - **colorPrimaryVariant**: variasi dari warna utama yang biasanya digunakan pada Status Bar.
  - **colorOnPrimary**: warna yang digunakan ketika ada text/icon di atas warna primary.
  - **colorSecondary**: warna utama sekunder yang tampil pada Action Bar dan komponen EditText.
  - **colorSecondaryVariant**: variasi dari warna sekunder.
  - **colorOnSecondary**: warna yang digunakan ketika ada teks/icon di atas warna sekunder.
  - **android:statusBarColor**: warna yang digunakan untuk status bar.
- Semua variabel warna sebaiknya dimasukkan di dalam berkas **colors.xml**.
