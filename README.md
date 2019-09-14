# Laporan Praktikum Modul 1 Jarkom 2019

### Oleh:
- Donny Fitrado (05111740000171)
- Faqih Fathan Irfani (05111740000175)

## Capture Filter
### NO1
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21
#### Jawab:
```
port 21
```
##### Screenshot:

### NO2
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80 (ajk.if.its.ac.id)
#### Jawab:
```
src port 80 && host ajk.if.its.ac.id
```
##### Screenshot:

### NO3
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443 (google.com)
#### Jawab:
````
dst port 443 && host google.com
````
##### Screenshot:

### NO4
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian
#### Jawab:
```
src ip <ip kalian>
```
##### Screenshot:

### NO5
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id
#### Jawab:
````
dst host monta.if.its.ac.id
````
##### Screenshot:

<br />

## Display Filter
### NO1
Tampilkan semua paket yang hostnya mengandung www.ne.its.ac.id
#### Jawab:
```
http.host == ne.its.ac.id
```
#### Screenshot:
<img src="Display%20Filter/no1.png" width="600">

### NO2
Tampilkan paket yang hanya berasal dari IP 10.151.36 81 dan menuju web "mb.its.ac.id"
#### Jawab:
```
ip.src == 10.151.36.81 && http.host == "mb.its.ac.id"
```
#### Screenshot:
<img src="Display%20Filter/no2.png" width="600">


### NO3
Simpan gambar ckedokteran.png
#### Jawab:
Tidak bisa dikerjakan karena gambar ckedokteran.png tidak ada.

#### Screenshot:
Tidak ada.

### NO4
Cari charset dari halaman "ajk.if.its.ac.id"
#### Jawab:
Charset tidak muncul pada saat follow TCP stream.

#### Screenshot:

### NO5
Cari username dan password ketika login di "freeshare.lp.if.its ac.id"
#### Jawab:
```
http.host == freeshare.lp.if.its.ac.id && frame contains login
```

#### Screenshot:

### NO6
Sebutkan web server yang digunakan pada "www.ne.its.ac.id"
#### Jawab:
```
http.host == ne.its.ac.id
```
kemudian, follow TCP stream

#### Screenshot:
<img src="Display%20Filter/no6.png" width="600">

### NO7
Sebutkan versi PHP dan yang digunakan pada "riset.ajk.if.its.ac.id"
#### Jawab:
```
http.host == riset.ajk.if.its.ac.id
```
kemudian, follow TCP stream.

#### Screenshot:
<img src="Display%20Filter/no7.png" width="600">

### NO8
Filter pada wireshark kalian sehingga menampilkan hasil ping
#### Jawab:
```
icmp
```

#### Screenshot:
<img src="Display%20Filter/no8.png" width="600">

### NO9
Dapatkan semua metode GET yang mengakses "monta.if.its.ac.id"
#### Jawab:
```
http.request.method == GET && http.host == monta.if.its.ac.id
```

#### Screenshot:
<img src="Display%20Filter/no9.png" width="600">

### NO10
Tunjukkan username dan password yang dimasukkan ketika login FTP
#### Jawab:
```
ftp.request.command == USER || ftp.request.command == PASS
```

#### Screenshot:
<img src="Display%20Filter/no10.png" width="600">

### NO11
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika upload file 
#### Jawab:
```
ftp.request.command == STOR && ftp.request.arg == qwpeaspojdasjfpasjfpaosuhuy.jpg
```

#### Screenshot:
<img src="Display%20Filter/no11.png" width="600">

### NO12
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika menghapus file 
#### Jawab:
```
ftp.request.command == DELE && ftp.request.arg == qwpeaspojdasjfpasjfpaos.jpg
```
Tapi tidak muncul, karena nama file-nya salah.

#### Screenshot:
<img src="Display%20Filter/no12.png" width="600">


### NO13
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika mengganti nama file "sutlin.png"
#### Jawab:
```
ftp.request.command == RNFR && ftp.request.arg == sutlin.png
```

#### Screenshot:
<img src="Display%20Filter/no13.png" width="600">

### NO14
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika download file "sutlun.png"
#### Jawab:
```
ftp.request.command == RETR && ftp.request.arg == sutlun.png
```

#### Screenshot:
<img src="Display%20Filter/no14.png" width="600">

### NO15
Cari file .zip di wireshark lalu download dan extract file tersebut <br />
clue: "50 4B 03 04"
#### Jawab:
```
ftp-data
```
1. Cari "50 4B 03 04" dengan Hex value.
2. Follow TCP Stream, ganti ASCII dengan Raw.
3. Save as folder berformat zip.
4. Buka folder

#### Screenshot:
1. <img src="Display%20Filter/no15-1.png" width="600">
2. <img src="Display%20Filter/no15-2.png" width="600">
3. <img src="Display%20Filter/no15-3.png" width="600">
4. <img src="Display%20Filter/no15-4.png" width="600">
5. <img src="Display%20Filter/no15-5.png" width="600">

<br />
Terima kasih dan mohon maaf apabila ada kesalahan.
