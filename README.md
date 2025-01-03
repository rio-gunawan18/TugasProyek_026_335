# Rekomendasi Lagu Pada Spotify

## Table of Contents
- [About](#about)
- [Objective](#objective)
- [About Dataset](#about-dataset)
- [The Problem](#the-problem)
- [Our Solution](#our-solution)
- [Dependencies](#dependencies)
- [License](#license)
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
### The Problem
### Our Solution

### Dependencies
The tutorial has been tested using Python 3.12.0.

Here is the list of all the dependencies that are needed to run this tutorial. These are all the dependencies needed to run the tutorial. The list of dependencies required for each individual section can be found in the `requirements.txt` file inside its folder.

- seaborn, version 0.13.2  
- numpy, version 1.26.4  
- plotly, version 5.24.1  
- pandas, version 2.2.2  
- matplotlib, version 3.8.0  
- python, version 3.12.0

### License
### Team
- [M. Rio Gunawan](https://github.com/rio-gunawan18) (202110370311026)
- [Muhammad Daffa Nugraha](https://github.com/Daffanugraha) (202110370311335)
