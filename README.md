# Rekomendasi Lagu Spotify
![image](https://github.com/user-attachments/assets/a993b073-273d-4c31-91ff-3359303b1aae)

## Table of Contents
- [About](#about)
- [Objective](#objective)
- [About Dataset](#about-dataset)
- [Selected Variables for Analysis](#selected-variables-for-analysis)  
- [Methodology](#methodology)
- [The Problem](#the-problem)
- [Our Solution](#our-solution)
- [Dependencies](#dependencies)
- [Results and Insights](#results-and-insights)
- [Team](#team)

### About
Spotify merupakan layanan musik digital, podcast, dan video yang memberikan akses ke jutaan lagu dan konten lain dari kreator di seluruh dunia. Dari dataset ini bisa menjadi rekomendasi bagi penikmat musik yang ingin mendengarkan musik pada aplikasi spotify.

Data ini berasal dari Spotify dan diakses melalui package spotify, yang memudahkan pengambilan data pribadi atau metadata lagu dari API Spotify. Kaylin Pavlik menggunakan package ini untuk mengumpulkan 5000 lagu dari 6 genre utama (EDM, Latin, Pop, R&B, Rap, Rock) dan menganalisis fitur audionya untuk eksplorasi serta klasifikasi lagu. Dataset dapat diakses melalui [github](https://github.com/rfordatascience/tidytuesday/blob/main/data/2020/2020-01-21/readme.md).
### Objective
Proyek ini bertujuan untuk memberikan rekomendasi lagu yang lebih personal bagi pengguna Spotify, dengan menggunakan data yang dikumpulkan dari API Spotify melalui package spotify. Dataset ini mencakup 5000 lagu dari 6 genre utama (EDM, Latin, Pop, R&B, Rap, dan Rock), lengkap dengan metadata seperti genre, durasi, tempo, dan tahun rilis. Dengan menganalisis fitur audio dan metadata tersebut, sistem ini dapat mengklasifikasikan lagu berdasarkan genre dan era musik, sehingga menciptakan rekomendasi yang lebih relevan bagi pengguna. Pengguna dapat memilih genre dan tahun favorit mereka, dan sistem akan memberikan rekomendasi lagu-lagu yang sesuai dengan preferensi tersebut.

Dengan pendekatan ini, Spotify dapat menawarkan pengalaman mendengarkan musik yang lebih personal, di mana pengguna bisa menemukan lagu-lagu baru sesuai dengan selera musik mereka atau bahkan menghidupkan nostalgia dengan lagu-lagu dari era tertentu. Dataset yang digunakan dapat diakses melalui GitHub untuk analisis lebih lanjut, dan proyek ini memberikan kesempatan untuk mengeksplorasi cara-cara baru dalam mengembangkan sistem rekomendasi berbasis genre dan tahun rilis.
### About Dataset
Link Dataset [spotify dataset](https://www.dropbox.com/sh/qj0ueimxot3ltbf/AACzMOHv7sZCJsj3ErjtOG7ya?dl=1)

Deskripsi Spotify

|variable                 |class     |description |
|:---|:---|:-----------|
|track_id                 |character | Song unique ID|
|track_name               |character | Nama Lagu|
|track_artist             |character | Song Artist|
|track_popularity         |double    | Popularitas Lagu dengan indikator (0-100) semakin tinggi nilai nya semakin populer |
|track_album_id           |character | Album unique ID|
|track_album_name         |character | Nama album dari lagu|
|track_album_release_date |character | Tanggal Rilis Album|
|playlist_name            |character | Nama Playlist|
|playlist_id              |character | Playlist ID|
|playlist_genre           |character | Playlist genre |
|playlist_subgenre        |character | Playlist subgenre|
|danceability             |double    |menggambarkan seberapa cocok suatu lagu untuk menari berdasarkan kombinasi elemen musik termasuk tempo, stabilitas ritme, kekuatan ketukan, dan keteraturan secara keseluruhan.|
|energy                   |double    | Energi adalah ukuran dari 0,0 hingga 1,0 dan mewakili ukuran persepsi intensitas dan aktivitas. |
|key                      |double    | Perkiraan key keseluruhan trek. Integer dipetakan ke nada menggunakan notasi Kelas Pitch standar. Misalnya. 0 = C, 1 = C♯/D♭, 2 = D, dan seterusnya. Jika tidak ada key yang terdeteksi, nilainya -1 |
|loudness                 |double    | keseluruhan trek dalam desibel (dB). Nilai kenyaringan dirata-ratakan di seluruh trek dan berguna untuk membandingkan kenyaringan relatif trek.|
|mode                     |double    | Mode menunjukkan modalitas (mayor atau minor) suatu lagu, jenis tangga nada yang menjadi asal isi melodinya. Mayor diwakili oleh 1 dan minor adalah 0.|
|speechiness              |double    |Speechiness mendeteksi keberadaan kata-kata yang diucapkan dalam sebuah trek. |
|acousticness             |double    |Ukuran keyakinan dari 0,0 hingga 1,0 untuk menentukan apakah trek bersifat akustik atau tidak. 1.0 mewakili keyakinan tinggi bahwa trek tersebut bersifat akustik.|
|instrumentalness         |double    |Memprediksi apakah suatu lagu tidak mengandung vokal. Bunyi "Ooh" dan "aah" dianggap instrumental dalam konteks ini. Lagu rap atau kata-kata yang diucapkan jelas bersifat "vokal".|
|liveness                 |double    | Mendeteksi kehadiran penonton dalam rekaman. |
|valence                  |double    | Ukuran dari 0,0 hingga 1,0 yang menggambarkan kepositifan musik yang disampaikan oleh sebuah lagu.|
|tempo                    |double    | Perkiraan tempo keseluruhan trek dalam ketukan per menit (BPM).|
|duration_ms              |double    |Durasi lagu dalam milidetik|

### Selected Variables for Analysis  

| Nama Variabel              | Tipe Data | Deskripsi                                                            |
|----------------------------|-----------|----------------------------------------------------------------------|
| `track_name`                | character | Nama Lagu                                                           |
| `track_artist`              | character | Nama Artis Lagu                                                      |
| `track_popularity`          | double    | Popularitas Lagu dengan indikator (0-100), semakin tinggi semakin populer |
| `track_album_release_date`  | character | Tanggal Rilis Album                                                  |
| `playlist_genre`            | character | Genre Playlist                                                        |

### Methodology  
1. **Menangani Missing Value**  
2. **Exploratory Data Analysis (EDA)**  
3. **Analisis Waktu Popularitas Lagu**  
4. **Penyusunan Wawasan**

### The Problem
Permasalahan utama proyek ini adalah bagaimana menganalisis dan mengeksplorasi data yang sangat beragam dan kaya dari Spotify untuk memahami pola yang ada dalam lagu-lagu, terutama berdasarkan waktu dan subkelompok. Dataset ini berisi informasi rinci tentang lagu, seperti artis, album, genre, subgenre, popularitas, dan nama lagu. Selain itu, ada fitur audio seperti danceability, energy, loudness, tempo, key, mode, dan lainnya. Tujuan dari analisis data ini adalah untuk menemukan hubungan atau pola menarik yang menunjukkan preferensi pengguna, karakteristik musik, dan bagaimana faktor waktu (seperti tahun rilis) dan subkelompok (seperti genre dan subgenre).

Selain itu, ada masalah tambahan tentang bagaimana memasukkan berbagai fitur ini ke dalam analisis yang konsisten dengan mempertimbangkan elemen waktu dan subkelompok. Misalnya, menentukan apakah popularitas lagu berubah seiring waktu atau bagaimana genre tertentu menjadi dominan selama periode waktu tertentu. Selain itu, sangat penting untuk mengeksplorasi hubungan antara subkelompok genre dan fitur musik lainnya, seperti apakah lagu dengan tempo cepat lebih dominan dalam genre tertentu atau bagaimana fitur seperti energi atau danceability berbeda di antara subgenre. Proses EDA membutuhkan pendekatan yang hati-hati untuk menemukan wawasan yang relevan dari data yang besar dan kompleks ini. Selain itu, pola yang mungkin tersembunyi di balik data harus divisualisasikan.

### Our Solution
To address this problem, we have developed a tool called KnowMore. KnowMore is an automated knowledge discovery tool integrated within the SPARC Portal that allows users of the portal to visualize, in just a few clicks, potential similarities, differences, and connections between multiple SPARC datasets of their choice. This simple process for using KnowMore is illustrated in the figure below.

<br/>
<p align="center">
   <img src="https://github.com/user-attachments/assets/7a6cc1cf-9950-48a7-b0e0-1baf96fb5347" alt="knowmore-usage" width="900">



  <br/> 
  <br/> 
  <i> Gambar ilustrasi dalam penyelesaian masalah </i>
  </img>
</p> 
<br/>

### Dependencies
The tutorial has been tested using Python 3.12.0.

Here is the list of all the dependencies that are needed to run this tutorial. These are all the dependencies needed to run the tutorial. The list of dependencies required for each individual section can be found in the `requirements.txt` file inside its folder.

- seaborn, version 0.13.2  
- numpy, version 1.26.4  
- plotly, version 5.24.1  
- pandas, version 2.2.2  
- matplotlib, version 3.8.0  
- python, version 3.12.0

### Results and Insights
#### 1. Genre Dominan

![Genre Dominan](https://github.com/user-attachments/assets/da388bde-eafd-429d-8db6-2204e11ff7ae)
**Deskripsi Analisis:**  
1. **Genre dengan Rata-rata Popularitas Tertinggi**:
   - Genre **Pop** menempati posisi teratas dengan rata-rata popularitas **47.74**, sedikit lebih tinggi dari Latin (**47.03**), yang berada di posisi kedua.

2. **Genre dengan Rata-rata Popularitas Terendah**:
   - Genre **EDM** memiliki rata-rata popularitas terendah, yaitu **34.83**, menunjukkan bahwa genre ini kurang diminati dibandingkan genre lainnya.

#### 2. Jumlah Lagu Berdasarkan Genre
![jumlah lagu](https://github.com/user-attachments/assets/0c129336-6db3-4cc6-9a82-4597459cd103)

**Deskripsi Analisis:** 

1. **Distribusi Jumlah lagu pada genre**


*   **edm** memiliki jumlah lagu sebanyak 6.043 lagu, menjadi genre yang memiliki jumlah lagu terbanyak
*   **rap** memiliki jumlah lagu sebanyak 5.743 lagu, menjadi genre memiliki lagu terbanyak setelah genre edm
*   **pop** memiliki jumlah lagu sebanyak 5.507 lagu, menjadi genre yang di tingkat menengah
*   **r&b** memiliki jumlah lagu sebanyak 5.431 lagu , genre ini niali nya mendekati jumlah dari genre pop
*   **latin** memiliki jumlah lagu sebanyak 5.153 lagu, menjadi genre yang memiliki jumlah lagu sedikit setelah genre rock
*   **rock**  memiliki jumlah lagu sebanyak 4.951 lagu, menjadi genre yang memiliki jumlah lagu sedikit

2. urutan genre

*   Urutan Genre Berdasarkan Jumlah Lagu:

  **EDM** > **Rap** > **Pop** > **R&B** > **Latin** > **Rock**.

*   Genre EDM sangat menonjol dibandingkan genre lainnya, sedangkan genre Rock memiliki jumlah lagu paling sedikit dalam daftar.

#### 3. Missing Value

*   Kolom `track_name`, `track_artist`, `track_album_name`  memiliki missing value karena mungkin terdapat lupa input pada kolom tersebut

#### 4. Analisis Waktu Popularitas Lagu

![Waktu Popularitas Lagu](https://github.com/user-attachments/assets/f4dc7e95-9639-4302-8234-b0360a61b714)

**Deskripsi Analisis:** 

1. **Pola Popularitas Lagu Berdasarkan Tahun Rilis**:
   - **Era Awal (1957-1970)**:
     - Popularitas rata-rata cenderung fluktuatif. Pada tahun-tahun awal, seperti 1957 (**30.0**) dan 1960 (**16.0**), popularitas cenderung lebih rendah.
     - Memasuki pertengahan hingga akhir 1960-an, popularitas meningkat, dengan puncaknya pada 1968 (**58.22**).

   - **Era 1970-an (1971-1980)**:
     - Popularitas rata-rata lebih stabil di kisaran 40-50, meskipun ada penurunan pada tahun tertentu, seperti 1974 (**40.39**).
     - Tahun 1980 menunjukkan peningkatan dengan popularitas rata-rata **52.25**, lebih tinggi dari dekade sebelumnya.

   - **Era 1980-an hingga 1990-an**:
     - Popularitas rata-rata cenderung mengalami penurunan bertahap dari awal 1980-an (sekitar **52.25** di tahun 1980) hingga akhir 1990-an (**41.79** pada 1999).
     - Secara umum, tren menunjukkan penurunan bertahap dalam popularitas.

   - **Era 2000-an hingga 2010-an**:
     - Popularitas rata-rata terus menurun secara signifikan, dengan titik terendah pada tahun 2008 (**27.26**) dan 2009 (**29.05**).
     - Setelah 2010, terjadi sedikit peningkatan hingga mencapai **41.76** pada tahun 2017.

   - **Era Modern (2018-2020)**:
     - Popularitas rata-rata meningkat pesat pada tahun-tahun terakhir, dari **45.88** (2018) hingga **51.40** (2019), sebelum sedikit menurun menjadi **46.46** pada tahun 2020.

2. **Kesimpulan Pola**:
   - Popularitas lagu cenderung tinggi pada akhir 1960-an hingga awal 1980-an, menunjukkan era di mana lagu-lagu klasik mendominasi.
   - Popularitas rata-rata menurun secara bertahap dari pertengahan 1980-an hingga akhir 2000-an, kemungkinan karena perubahan tren musik atau data yang lebih sedikit dari tahun-tahun tersebut.
   - Era modern (2018-2020) menunjukkan peningkatan popularitas rata-rata, yang dapat dikaitkan dengan peningkatan aksesibilitas musik melalui platform digital dan fokus pada lagu-lagu populer dalam dataset.

3. **Hubungan Tahun Rilis dengan Popularitas**:
   - Lagu-lagu yang dirilis pada tahun yang lebih baru (2018-2020) memiliki popularitas yang relatif lebih tinggi dibandingkan dengan dekade sebelumnya, menunjukkan bahwa musik modern lebih banyak didengarkan dan diakui.
   - Lagu-lagu klasik (1960-an hingga awal 1980-an) juga memiliki popularitas tinggi, kemungkinan karena dampaknya yang besar di era tersebut dan apresiasi lintas generasi.


### Team
- [M. Rio Gunawan](https://github.com/rio-gunawan18) (202110370311026) / Analisa Big Data A
- [Muhammad Daffa Nugraha](https://github.com/Daffanugraha) (202110370311335) / Analisa Big Data A
