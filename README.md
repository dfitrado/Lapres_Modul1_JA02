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


### NO2
Tampilkan paket yang hanya berasal dari IP 10.151.36 81 dan menuju web "mb.its.ac.id"
#### Jawab:
```
ip.src == 10.151.36.81 && http.host == "mb.its.ac.id"
```
#### Screenshot:


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

### NO7
Sebutkan versi PHP dan yang digunakan pada "riset.ajk.if.its.ac.id"
#### Jawab:
```
http.host == riset.ajk.if.its.ac.id
```
kemudian, follow TCP stream.

#### Screenshot:

### NO8
Filter pada wireshark kalian sehingga menampilkan hasil ping
#### Jawab:
```
icmp
```

#### Screenshot:

### NO9
Dapatkan semua metode GET yang mengakses "monta.if.its.ac.id"
#### Jawab:
```
http.request.method == GET && http.host == monta.if.its.ac.id
```

#### Screenshot:

### NO10
Tunjukkan username dan password yang dimasukkan ketika login FTP
#### Jawab:
```
ftp.request.command == USER || ftp.request.command == PASS
```

#### Screenshot:

### NO11
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika upload file 
#### Jawab:
```
ftp.request.command == STOR && ftp.request.arg == qwpeaspojdasjfpasjfpaosuhuy.jpg
```

#### Screenshot:

### NO12
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika menghapus file 
#### Jawab:
```
ftp.request.command == DELE && ftp.request.arg == qwpeaspojdasjfpasjfpaos.jpg
```
Tapi tidak muncul, karena nama file-nya salah.

#### Screenshot:


### NO13
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika mengganti nama file "sutlin.png"
#### Jawab:

#### Screenshot:

### NO14
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika download file "sutlun.png"
#### Jawab:

#### Screenshot:

### NO15
Cari file .zip di wireshark lalu download dan extract file tersebut <br />
clue: "50 4B 03 04"
#### Jawab:
```
ftp-data
```
Cari "50 4B 03 04" dengan Hex value.
Follow TCP Stream, ganti ASCII dengan Raw.

Save as folder berformat zip.

Buka folder

#### Screenshot:



