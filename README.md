# Analisis Data YouTube Trending
Analisis data YouTube trending ini bertujuan untuk mengetahui informasi terkait faktor yang mempengaruhi tingkat kepopuleran suatu video di YouTube dengan cara mencari perbandingan antar kategori video, korelasi antar atribut data, hubungan antar atribut data, dan perubahan data terhadap waktu. Analisis data dilakukan dengan menggunakan bahasa pemrograman Python. Data YouTube Trending yang digunakan untuk analisis adalah data YouTube Trending Video Statistics di negara Amerika Serikat, yang diambil dari [https://www.kaggle.com/]. 

## Atribut Data
Data yang digunakan memiliki 23 atribut sebagai berikut.
- video_id : seri ID yang unik untuk mengidentifikasi video
- last_trending_date : tanggal terakhir video trending
- publish_date : tanggal video diterbitkan
- publish_hour : waktu video diterbitkan
- category_id : seri ID untuk mengidentifikasi kategori video
- channel_title : judul/nama dari channel YouTube
- views : jumlah penayangan video
- likes : jumlah likes (disukai) pada video
- dislikes : jumlah dislikes (tidak disukai) pada video
- comment_count : jumlah komentar yang terdapat pada video
- comments_disabled : kondisi apakah komentar dinonaktifkan pada video
- ratings_disabled : kondisi apakah rating dinonaktifkan pada video
- tag_appeared_in_title_count : jumlah tag yang terdapat di judul video
- tag_appeared_in_title : kondisi apakah tag terdapat di judul video
- title : judul dari video YouTube
- tags : sebuah keyword tambahan untuk video
- description : keterangan dari suatu video
- trend_day_count :  durasi suatu video memasuki trend
- trend.publish.diff : jarak waktu antara diterbitkannya suatu video dan video tersebut
menjadi trend
- trend_tag_highest : jumlah tag trend tertinggi yang digunakan oleh channel
- trend_tag_total : jumlah tag trend yang digunakan oleh channel
- tags_count : jumlah (angka) tag terdapat di judul video
- subscriber : jumlah pengikut yang terdapat di suatu channel

## Proses Analisis Data
Sebelum data YouTube Trending dianalisis, dilakukan data cleansing untuk melakukan pembersihan data terhadap data yang kosong atau data yang salah menggunakan Python. Data yang kosong diisi dengan nilai rata-rata dari kolom atribut terkait. Data yang telah bersih kemudian dapat digunakan untuk analisis dan visualisasi.
Analisis data dilakukan dengan mencari statistik data, yang meliputi :
- Nilai rata-rata dan standar deviasi
- Percentile (10%, 25%, 50%, 75%, dan 90%)
- Ekstremum (nilai maksimum dan minimum)
- Range setiap atribut
- Distribusi frekuensi nilai
Selanjutnya, visualisasi data dibuat untuk melakukan perbandingan kategori, menampilkan perubahan data terhadap waktu, menampilkan hierarki dan hubungan keseluruhan-bagian, dan plotting relationships. Berikut merupakan visualisasi data yang dibuat beserta insight yang diperoleh.
1. Perbandingan kategori
   - Rata-rata likes, dislikes, dan comments berdasarkan tag appeared in title pada tahun 2018
     Insight : Video dengan tag yang muncul pada judul secara keseluruhan memiliki likes yang lebih banyak, dislikes yang lebih sedikit, dan comments yang lebih sedikit dibandingkan dengan video yang tidak memiliki tag pada judulnya.
   - Rata-rata views dan subscriber tiap category pada November 2017
     Insight : Tiga  category video trending yang umumnya memiliki views tertinggi secara berurutan adalah category Music, Film and Animation, dan Entertainment, sedangkan yang memiliki views terendah adalah category Nonprofits and Activism, Gaming, dan News and Politics. Sementara itu, tiga category video trending yang memiliki subscriber tertinggi secara berurutan adalah Comedy, Sports, dan Entertainment, sedangkan tiga category video trending yang memiliki subscriber terendah adalah category Nonprofits and Activism, Travel and Events, dan Autos and Vehicles.
   - Rata-rata trend tag highest dan tags count berdasarkan comments disabled pada Maret 2018
     Insight : Video dengan comments yang diaktifkan secara keseluruhan memiliki trend tag highest yang lebih tinggi dan jumlah tags yang lebih banyak dibandingkan video dengan comments yang dinonaktifkan.
2. Penampilan perubahan terhadap waktu
   - Perkembangan views channel Vox pada tahun 2017-2018
     Insight : Views channel Vox dari tanggal 13 November 2017 sampai sekitar 27 Februari 2018 banyak mengalami penurunan dan kenaikan yang tidak terlalu signifikan dengan kisaran antara sekitar 0,3 juta sampai 1,2 juta, dengan lonjakan kenaikan yang sangat tinggi sebanyak dua kali, yaitu antara tanggal 22 Desember 2017 sampai 10 Januari 2018 yang mencapai sekitar 2,4 juta, dan pada awal antara tanggal 3 Februari 2018 sampai sekitar 27 Februari 2018 yang mencapai sekitar 2,5 juta. Channel Vox mencapai views tertingginya pada tanggal di antara 3 Februari 2018 dan 27 Februari 2018.
   - Perkembangan likes, dislikes, dan comment count untuk category 24 pada November 2017
     Insight : Perkembangan likes, dislikes, dan comment count dapat dibandingkan. Penurunan dan kenaikan likes, dislikes, dan comment count video dengan category Entertainment pada November 2017 secara keseluruhan saling berhubungan. Ketika likes mengalami penurunan, maka dislikes dan comment count juga mengalami penurunan. Sebaliknya 28 ketika likes mengalami kenaikan, maka dislikes dan comment count juga mengalami kenaikan.
   - Perkembangan rata-rata views berdasarkaan publish hour pada tahun 2018
     Insight : Views video pada tahun 2018 berdasarkan jam video di-publish dari jam 00.00 sampai jam 23.00 banyak mengalami penurunan dan kenaikan yang cukup signifikan. Video yang di-publish pada jam 04.00 memiliki views tertinggi, sementara video yang di-publish pada jam 11.00 memiliki views terendah.
3. Penampilan hierarki dan hubungan keseluruhan-bagian
   - Persentase total views tiap category pada Januari 2018
     Insight : Category dengan total views paling banyak pada Januari 2018 adalah category Music dengan persentase 32,49% dari total views seluruh category pada Januari 2018. Sementara itu, category dengan total views paling sedikit pada Januari 2018 adalah category Shows dengan persentase 0,01% dari total views seluruh category pada Januari 2018.
   - Persentase banyaknya video yang trending berdasarkan category pada tahun 2017
     Insight : Category dengan jumlah video trending paling banyak pada tahun 2017 adalah category Entertainment dengan persentase 25,03% dari total jumlah video yang trending pada tahun 2017. Sementara itu, category dengan jumlah video trending paling sedikit pada tahun 2018 adalah category Shows dengan persentase 0,05% dari total jumlah video yang trending pada tahun 2017.
   - Komposisi likes dan dislikes tiap category pada Februari 2018
     Insight : Secara umum, category video dengan total likes dan dislikes paling banyak adalah category 29, yaitu Nonprofits and Activism, sementara category video dengan total likes dan dislikes paling sedikit adalah category 25, yaitu News and Politics. Category video dengan komposisi likes paling banyak adalah category 10, yaitu Music, sementara category video dengan komposisi likes paling sedikit adalah category 25, yaitu News and Politics. Category video dengan komposisi dislikes paling banyak adalah category 29, yaitu Nonprofits and Activism, sementara category video dengan komposisi dislikes paling sedikit adalah category 15, yaitu Pets and Animals. Selain itu, secara keseluruhan, seluruh category memiliki likes yang lebih banyak dibandingkan dengan dislikes.
4. Plotting relationships
   - Korelasi antara likes dan dislikes untuk catgeory 10 pada Januari 2018
     Insight : Korelasi antara likes dan dislikes video dengan category Music pada Januari 2018 bernilai positif. Titik-titik  korelasi agak tersebar sehingga korelasi antara likes dan dislikes video dengan category Music pada Januari 2018 tidak sempurna, namun korelasinya dapat dikatakan masih tinggi (high positive correlation). Hal ini berarti semakin banyaknya likes berpengaruh besar terhadap semakin tingginya dislikes untuk video dengan category Music pada Januari 2018.
   - Korelasi antara views dan likes pada tahun 2017
     Insight : Korelasi antara views dan likes video pada tahun 2017 bernilai positif. Titik-titik korelasi agak tersebar sehingga korelasi antara views dan likes video pada tahun 2017 tidak sempurna, namun korelasinya dapat dikatakan masih tinggi (high positive correlation). Hal ini berarti semakin banyaknya views berpengaruh besar terhadap semakin banyaknya likes video pada tahun 2017. Selain itu, tags count video tidak memengaruhi views dan likes video pada tahun 2017 tersebut.
