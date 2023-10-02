
<h1 align="center"><img src="screenshots\header.png"></h1>

[Sekilas Tentang](##sekilas-tentang) | [Instalasi](#instalasi) | [Cara Pemakaian](#cara-pemakaian) | [Pembahasan](#pembahasan) | [Referensi](#referensi)
:---:|:---:|:---:|:---:|:---:


# Sekilas Tentang
[`^ kembali ke atas ^`](#)

**Planka** adalah aplikasi manajemen proyek dan kolaborasi tim berbasis Open Source yang serupa dengan Trello. Planka menyediakan platform dimana tim dapat mengatur dan mengelola tugas atau proyek mereka pada visual board, seperti metodologi Kanban. Pengguna dapat membuat card yang mewakili tugas, memindahkannya melalui kolom atau tahap berbeda untuk melacak progress, dan berkolaborasi dengan anggota tim dalam berbagai proyek.


# Instalasi
[`^ kembali ke atas ^`](#)

**Instalasi dengan Docker :**


Login ke ssh terlebih dahulu:
```bash
ssh [username]@[ipaddresvps]
```
Setelah itu buat folder terlebih dahulu
```bash
mkdir planka
```
Masuk ke folder planka
```bash
cd planka
```

Download file docker-compose.yml dari sumber:
```bash
curl -L https://raw.githubusercontent.com/plankanban/planka/master/docker-compose.yml -o docker-compose.yml
```

Sesuaikan portnya dengan port yang anda buka di vps, buka file docker compose:
```bash
nano docker-compose.yml
```
Port yang kami gunakan adalah port 80, edit di  bagian:

<img src="screenshots\port3000.png">

menjadi: 

<img src="screenshots\port8000.png">

Jalankan dockernya, program akan berjalan di port 80 ip address anda:

```bash
sudo docker-compose up
```

# Cara Pemakaian
[`^ kembali ke atas ^`](#)

Cara pemakaian **Planka** ini sangat mudah, karena aplikasi ini telah menyediakan *interface* yang mudah dimengerti. Berikut untuk lebih jelasnya :

1. Melakukan login sebagai Admin pada halaman website
<img src="screenshots\planka1.png">
 

2. Setelah melakukan login, pengguna akan dialihkan ke halaman utama yang berisi project-project yang telah dibuat sebelumnya
<img src="screenshots\planka2.png">

3. Menu **Create Project** digunakan untuk menambah project baru sesuai dengan nama project yang dimasukkan pengguna
<img src="screenshots\planka3.png">

4. Pengguna dapat menekan project untuk melihat detail dari project. Sebuah Project berisi list card yang dibuat oleh pengguna. Ini adalah contoh project kelompok yang telah dibuat sebelumnya. Sebuah project terdiri dari beberapa Board yang terdiri dari sejumlah List. Sebuah List memiliki sejumlah Card yang berisi informasi tugas dari pengguna. 
<img src="screenshots\planka4.png">

5. Menu **Add another list** menambahkan sebuah list baru ke dalam suatu board. Di sini pengguna akan menambahkan list baru dengan nama “Done”. Urutan List dalam Board dapat diubah dengan cara drag and drop.
<img src="screenshots\planka5.png">

6. Menu **Add another card** menambahkan sebuah card baru ke dalam suatu list. Di sini pengguna menambahkan card baru ke dalam list “To-Do’s”
<img src="screenshots\planka6.png">
<img src="screenshots\planka6_1.png">

7. Untuk memberi informasi tambahan pada Card yang telah dibuat, pengguna dapat menekan card untuk melakukan edit. Secara general, pengguna dapat menambahkan deskripsi card, deskripsi tugas, dan mengomentari actions. Dalam submenu Add to card pengguna dapat mengatur detail card seperti menambahkan member ke dalam card, memberikan label, menambahkan due date, mengatur stopwatch, dan melampirkan file dari perangkat pengguna. Selain itu, terdapat submenu Actions yang berisi aksi subscribe, memindahkan card, dan menghapus card.
<img src="screenshots\planka7.png">
<img src="screenshots\planka7_1.png">

8. Selain dengan cara di atas, pengguna dapat melakukan edit pada card dengan menekan icon edit yang terdapat pada pojok kanan atas card.
<img src="screenshots\planka8.png">

9. Pengguna juga dapat memindahkan Card dari suatu List ke List lain dengan drag and drop. Di sini pengguna memindahkan 2 card yang terdapat di list “Projek” ke list lain
<img src="screenshots\planka9.png">

10. Pengguna dapat menambahkan Board baru dengan menekan tanda + yang terletak pada Board yang sudah ada
<img src="screenshots\planka10.png">

11. Selain itu pada pojok kanan atas website terdapat fitur tambahan yaitu melakukan manajemen user, mengecek notifikasi, mengedit informasi akun, dan log out.
<img src="screenshots\planka11_1.png">
**Manajemen User**
<img src="screenshots\planka11_2.png">
**Notifikasi**
<img src="screenshots\planka11_3.png">
**Edit Informasi Akun**
<img src="screenshots\planka11_4.png">

# Pembahasan
[`^ kembali ke atas ^`](#)

**Pendapat anda tentang aplikasi web ini:**

<!-- Create table wuth 2 column in readme  -->


| Kelebihan | Kekurangan |
|:---------:|:------:|
|Aplikasi web ini mudah digunakan, pengguna cukup login saja dengan email/username.   | Tidak ada fitur sign-up sehingga jika ingin login harus meminta dibuatkan akun atau dapat menggunakan akun guest jika disediakan.|
|Dapat digunakan secara gratis   |Keterbatasan fitur|
|Desain yang sederhana. UI yang minimalist membolehkan user untuk navigasi secara intuitif | Desainnya terkesan polos dan kurang menarik |
|Tidak mempunyai pemilihan template yang berlebihan. |Kustomisasi design template terbatas|
|Tidak ada batasan untuk membuat board, web app ini tidak membutuhkan pembayaran untuk menikmati semua fiturnya |Kurang responsive pada device seperti smartphone|



**Aplikasi web ini mengambil inspirasi dari Trello, berikut adalah perbandingannya:**

<img src="screenshots\planka12.png">

Pada homepage trello, terdapat banyak fitur yang dapat dipakai sesuai keinginan user. 
- Templates: user dapat menyesuaikan kanban board dengan kebutuhannya atau skala projectnya
- Pada sisi kiri, terletak list untuk menavigasi boards yang telah dibuat untuk suatu project oleh usernya, sekaligus informasi terkait board-nya, seperti Highlights, Views, Members, and Settings. 
- Pada navbar yang terletak di atas, terdapat drop-down beberapa navigation tools untuk membolehkan user untuk mengatur projects maupun boards yang ada.
- Search bar: user dapat mencari suatu board secara spesifik. 
- Settings: User dapat mengubah preferensi dari account settings, email notifications, accessibility, dll. 

<img src="screenshots\planka13.png">

Pada Planka, dapat dilihat bahwa UI dari website tersebut lebih minimalist. Fitur-fitur seperti navbar, search bar, dan templates tidak ada. Project yang telah di-assign oleh admin kepada suatu user akan tampil pada homepage Planka. Pada navbar Planka, ada notification icon yang akan memberikan user notifikasi atas interaksi yang terjadi pada board suatu user, seperti penyelesaian suatu task, assignment kepada suatu task baru, dll. User dapat mengubah akun details dengan memencet nama user tersendiri pada pojok kanan atas. 


<img src="screenshots\planka14.png">

Untuk mengubah account details, user akan diarahkan ulang kepada Atlassian account.

<img src="screenshots\planka15.png">

Pada page tersebut, user dapat mengubah beberapa hal terkait dengan akunnya, seperti profile details, email, security, account preferences, dll. 

<img src="screenshots\planka16.png">

Dibandingkan dengan Trello, account details yang ada pada Planka cukup minim. 

<img src="screenshots\planka17.png">

Pada suatu board, page akan menampilkan list-list yang telah dibuat oleh user. Pada suatu list, user dapat menambahkan suatu card. 


<img src="screenshots\planka18.png">

Pada card tersebut, ada beberapa fitur yang dapat digunakan oleh user:
- User dapat memilih untuk mendapatkan notifikasi jika ada aksi yang dilakukan kepada card tersebut
- User dapat menambahkan deskripsi pada card tersebut
- User dapat menambahkan comment pada card tersebut untuk menunjukkan progress dari setiap user terlibat pada card tersebut
- User dapat menambahkan member lain pada card tersebut
- User dapat menambahkan checklist pada card tersebut, dan checklist tersebut akan tampil pada card tersebut
- User dapat menambahkan deadline pada card tersebut
- User dapat menambahkan attachments pada card tersebut, seperti foto, dokumen, link, dll.

Ada beberapa fitur yang hanya dimiliki oleh Trello, seperti:
- Automation: user dapat membuat card tersebut untuk mengeluarkan suatu output/melakukan suatu aksi dengan input atau ketentuan tertentu. 
- Power-ups: user dapat menambahkan suatu power-up kepada suatu card untuk menambahkan suatu fungsionalitas tertentu yang tidak ada pada Trello

<img src="screenshots\planka19.png">

Pada suatu board di Planka, page akan menampilkan list-list yang telah dibuat oleh user. Pada suatu list, user dapat menambahkan suatu card. Namun, dibandingkan dengan Trello, ada beberapa fungsionalitas yang tidak terdapat pada Planka, seperti Automation, Filtering, Power-ups, dan Share. Dapat dilihat bahwa tampilan kanban board yang ada pada Trello dan Planka hampir sama. 


<img src="screenshots\planka20.png">

Pada tampilan card di Planka, ada beberapa fitur yang dapat digunakan oleh user:
- User dapat memilih untuk mendapatkan notifikasi jika ada aksi yang dilakukan kepada card tersebut
- User dapat menambahkan deskripsi pada card tersebut
- User dapat menambahkan comment pada card tersebut untuk menunjukkan progress dari setiap user terlibat pada card tersebut
- User dapat menambahkan member lain pada card tersebut
- User dapat menambahkan label pada card, agar user dapat mengklasifikasikannya
- User dapat menambahkan deadline atau due date pada card tersebut
- User dapat menambahkan attachments pada card tersebut, seperti foto, dokumen, link, dll

# Referensi
[`^ kembali ke atas ^`](#)

- [About Planka](https://github.com/plankanban/planka) - Plankanban
- [How to create Droplets(digital ocean VM's)](https://docs.digitalocean.com/products/droplets/how-to/create/) - Digital Ocean
- [How to log into a VPS with ssh on Windows](https://www.digitalocean.com/community/tutorials/how-to-log-into-a-vps-with-putty-windows-users) - Digital Ocean
- [Installing planka with Docker](https://docs.planka.cloud/docs/installl-planka/Docker%20Compose/) - Plankanban
- [What is trello](https://trello.com/tour)- Trello
